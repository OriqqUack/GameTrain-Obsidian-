
*SceneManager* 가 제공하는 *LoadScene* 을 호출하면 유니티는 해당 장면의 모든 정보를 메모리로 가져오기까지 다른 작업을 할 수 없다.

흔히 *렉* 이라고 하며 작업처리지연 현상을 일컫는다. 만일 불러오는 장면의 크기가 클 경우 이 상황이 더욱 심함. 

이를 위해 유니티에선 비동기 지연적인 연산을 위한 코루틴 제공 일명 *AsyncOperation*

```c#
AsyncOperation async = SceneManager.LoadSceneAsync("SceneName");
```
와 같이 쓰고

```c#
IEnumerator LoadScene(string sceneName){
	AsyncOperation async = SceneManager.LoadSceneAsync("SceneName");
	while(!async.isDone){
		yield return null;
		Debug.Log(async.progress);
	}
}
```
처럼 실제 로딩을 할때 이와 같이 사용

SceneManager.LoadSceneAsync("SceneName", *LoadSceneMode.Singe(Additive)*); 
single 혹은 additive가 들어가는데
*Single*은 현재 씬이 모두 종료가 된 뒤에 로드가 되는 것이고 *Additive*는 실행중에 로드를 하는 방식이다.

