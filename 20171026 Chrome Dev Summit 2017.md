# Chrome Dev Summit 2017
https://developer.chrome.com/devsummit/

## The future of loading on the web
By Sam Saccone

* window.navigator.connection API
* cache digest for http2 push
    * "overpush"ed assets
    * cache digest tells what's in the local cache
    * https://goo.gl/wMiWfJ
* asset priority hints
    * explict priorities vs inferred priorities
    * browser inference engine
    * link rel and img tag hacks for hacking higher priorities
    * gituhb.com/WICG/priority-hints
    * group attribute ["critical", "late" etc.]
    * const controller = new FetchController(); controller.signal; controller.setPriority()
* async images
    * large image, followed by script
    * image download, image decode blocks main thread. so the script gets blocked
    * new async attribute on the img tag
* Runtime perf
    * move work out of the critical path. without impacting UX
    * web workers keeps the main thread free
        * no access to DOM. DOMChangeList proposal. enables contruction of DOM opterations
        * https://github.com/whatwg/dom/issues/270
        * SharedArrayBuffer()
        * https://goo.gl/B725QT
        * preact-worker-demo.surge.sh
        * https://github.com/GoogleChromeLabs/comlink
        * https://github..com/robwormald/ng-webworker-demo

## V8 today and in the future
By Thomas Nattestad

* https://twitter.com/V8js
* https://vsproject.blogspot.com
