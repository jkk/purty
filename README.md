# purty

Clojure library to perform basic image operations - read, write, scale, crop.

Relies on the [imgscalr](http://www.thebuzzmedia.com/software/imgscalr-java-image-scaling-library/) Java library.

## Usage

Leiningen:

```clj
[jkkramer/purty "0.1.0"]
```

REPL example:

```clj
(require '[jkkramer.purty :as purty])
(let [oolong (purty/read "http://jkkramer.com/oolong.jpg") ;or file, stream, etc
      avatar (purty/scale oolong :size 100 :fit :crop)]
  (purty/write thumb "/tmp/oolong_thumb.jpg" :quality 50))
```

## TODO

* Use Sanselan: http://commons.apache.org/imaging/
* Auto-detect output image type based on extension
* More docs?

## License

Copyright © 2012 Justin Kramer

Distributed under the Eclipse Public License, the same as Clojure.
