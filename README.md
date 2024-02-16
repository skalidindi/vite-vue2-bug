# vite-vue2-bug

Run app with

```
npm run dev
```

Navigate to http://localhost:3000/src/App.vue?vue&type=style&index=0&lang.module.css

Note that the response is valid javascript i.e
```
import { createHotContext as __vite__createHotContext } from "/@vite/client";import.meta.hot = __vite__createHotContext("/src/App.vue?vue&type=style&index=0&lang.module.css");import { updateStyle as __vite__updateStyle, removeStyle as __vite__removeStyle } from "/@vite/client"
const __vite__id = "/Users/skalidindi/oss/vite-vue2-bug/src/App.vue?vue&type=style&index=0&lang.module.css"
const __vite__css = "\n.some-class {\n  color: red;\n}\n._main_3nzk9_6 {\n  background-color: #f0f0f0;\n}\n"
__vite__updateStyle(__vite__id, __vite__css)
export const main = "_main_3nzk9_6";
export default {
	main: main
};

import.meta.hot.prune(() => __vite__removeStyle(__vite__id))
```

However, switch the order of query params in the url such as
http://localhost:3000/src/App.vue?vue&type=style&lang.module.css&index=0

and the response is css

This behavior is not consistent


