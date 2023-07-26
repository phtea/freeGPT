# fork of freeGPT that makes picture generations random
# 🍴

## Example:

**Text Completion: (instead of gpt3 you can try using another model names)**
```python
import freeGPT
import asyncio


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await getattr(freeGPT, "gpt3").Completion.create(prompt)
            print(f"🤖: {resp}")
        except Exception as e:
            print(f"🤖: {e}")


asyncio.run(main())
```

**Image Generation: (instead of prodia you can try using another model names)**
```python
import freeGPT
import asyncio
from PIL import Image


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await getattr(freeGPT, "prodia").Generation.create(prompt)
            Image.open(resp).show()
            print(f"🤖: Image shown.")
        except Exception as e:
            print(f"🤖: {e}")


asyncio.run(main())
```
