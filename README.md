# fork of freeGPT that makes picture generations random
# 🍴

## Example:

**Text Completion:**
```python
import freeGPT
import asyncio


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await getattr(freeGPT, "MODEL NAME").Completion.create(prompt)
            print(f"🤖: {resp}")
        except Exception as e:
            print(f"🤖: {e}")


asyncio.run(main())
```

**Image Generation:**
```python
import freeGPT
import asyncio
from PIL import Image


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await getattr(freeGPT, "MODEL NAME").Generation.create(prompt)
            Image.open(resp).show()
            print(f"🤖: Image shown.")
        except Exception as e:
            print(f"🤖: {e}")


asyncio.run(main())
```
