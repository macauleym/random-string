;;;;;;;;;;;;;;;;;;;;
;; Language Definition
;;;;;;;;;;;;;;;;;;;;
#lang racket/base

;;;;;;;;;;;;;;;;;;;;
;; Requires
;;;;;;;;;;;;;;;;;;;;
[require racket/cmdline]
[require racket/list]

;;;;;;;;;;;;;;;;;;;;
;; Data Properties
;;;;;;;;;;;;;;;;;;;;
{define str-length (make-parameter 10)}

;;;;;;;;;;;;;;;;;;;;
;; Functions
;;;;;;;;;;;;;;;;;;;;
(define random-string
  (command-line
   #:usage-help
   "Creates a string of random characters, with the specified length."
   "If no length is specified, the default value of 10 is used."
   #:args (len) ;; put calls here??
   (str-length (string->number len))))

(define (rand-chars n)
  (for/list ([i (in-range n)])
    {define ascii-start 32  }
    {define ascii-end   120 }
    ; Could also use this, to open it up to _all_ of the Unicode codes.
    ;;{define ranges (make-known-char-range-list))}
    (string (integer->char (random ascii-start ascii-end)))))

(define (rndstr)
  (apply string-append (rand-chars  (str-length))))

(println (rndstr))
                    
