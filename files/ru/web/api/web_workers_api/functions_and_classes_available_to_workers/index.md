---
title: Функции и классы доступные веб-воркерам
slug: Web/API/Web_Workers_API/Functions_and_classes_available_to_workers
---

{{DefaultAPISidebar("Web Workers API")}}

In addition to the standard [JavaScript](/ru/docs/Web/JavaScript) set of functions (such as {{jsxref("String")}}, {{jsxref("Array")}}, {{jsxref("Object")}}, {{jsxref("JSON")}}, etc.), there are a variety of functions available from the DOM to workers. This article provides a list of those.

## Worker Contexts & Functions

**Workers run in a different global context than the current window!** While {{domxref("Window")}} is not directly available to workers, many of the same methods are defined in a shared mixin (`WindowOrWorkerGlobalScope`), and made available to workers through their own {{domxref("WorkerGlobalScope")}}-derived contexts:

- {{domxref("DedicatedWorkerGlobalScope")}} for dedicated workers
- {{domxref("SharedWorkerGlobalScope")}} for shared workers
- {{domxref("ServiceWorkerGlobalScope")}} for [service workers](/ru/docs/Web/API/Service_Worker_API)

Some of the functions that are common to all workers and to the main thread (from `WindowOrWorkerGlobalScope`) are: {{domxref("atob", "atob()")}}, {{domxref("btoa", "btoa()")}}, {{domxref("clearInterval", "clearInterval()")}}, {{domxref("clearTimeout()")}}, {{domxref("Window.dump()", "dump()")}} {{non-standard_inline}}, {{domxref("setInterval()")}}, {{domxref("setTimeout()")}}.

The following functions are **only** available to workers:

- {{domxref("WorkerGlobalScope.importScripts", "WorkerGlobalScope.importScripts()")}} (all workers),
- {{domxref("DedicatedWorkerGlobalScope.postMessage")}} (dedicated workers only).

## Web APIs available in workers

> **Note:** If a listed API is supported by a platform in a particular version, then it can generally be assumed to work in web workers.

The following Web APIs are available to workers:

- {{domxref("Broadcast_Channel_API", "Broadcast Channel API")}}
- {{domxref("Cache", "Cache API")}}
- {{domxref("Channel_Messaging_API", "Channel Messaging API")}}
- {{domxref("Console API", "Console API")}}
- {{domxref("Crypto")}}
- {{domxref("CustomEvent")}}, `DOMRequest` and `DOMCursor`
- {{domxref("Fetch_API", "Fetch")}}
- {{domxref("FileReader")}}
- {{domxref("FileReaderSync")}} (only works in workers!)
- {{domxref("FormData")}}
- {{domxref("ImageData")}}
- {{domxref("IndexedDB_API", "IndexedDB")}}
- [Network Information API](/ru/docs/Web/API/Network_Information_API)
- {{domxref("Notifications_API", "Notifications")}}
- {{domxref("Performance")}}
- {{domxref("PerformanceEntry")}}
- {{domxref("PerformanceMeasure")}}
- {{domxref("PerformanceMark")}}
- {{domxref("PerformanceObserver")}}
- {{domxref("PerformanceResourceTiming")}}
- {{jsxref("Promise")}}
- [Server-sent events](/ru/docs/Web/API/Server-sent_events)
- {{domxref("ServiceWorkerRegistration")}}
- {{domxref("TextEncoder")}} and {{domxref("TextDecoder")}}
- {{ domxref("URL") }}
- [WebGL](/ru/docs/Web/API/WebGL_API) with {{domxref("OffscreenCanvas")}}
- {{domxref("WebSocket")}}
- {{domxref("XMLHttpRequest")}} (although the `responseXML` and `channel` attributes are always null).

Workers can also spawn other workers, so these APIs are also available:

- {{domxref("Worker")}}
- {{domxref("WorkerGlobalScope")}}
- {{domxref("WorkerLocation")}}
- {{domxref("WorkerNavigator")}}.

## Смотрите также

- [Using web workers](/ru/docs/Web/API/Web_Workers_API/Using_web_workers)
- {{domxref("Worker")}}
