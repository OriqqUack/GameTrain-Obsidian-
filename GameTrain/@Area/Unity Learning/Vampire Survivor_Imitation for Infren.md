---
태그: 공부
설명: 인프런 2d게임 공부
작성 날짜: "[[2023-09-24]]"
수정된 날짜: "[[2023-09-24]]"
---

---

	## 무한맵 생성

```c#
private void OnTriggerExit2D(Collider2D collision)
    {
        Camera camera = collision.gameObject.GetComponent<Camera>();
        if (camera == null)
            return;

        Vector3 dir = camera.transform.position - transform.position;

        float dirX = dir.x < 0 ? -1 : 1;
        float dirY = dir.y < 0 ? -1 : 1;

        if (Mathf.Abs(dir.x) > Mathf.Abs(dir.y))
            transform.Translate(Vector3.right * dirX * 200);
        else
            transform.Translate(Vector3.up * dirY * 200);
    }
```