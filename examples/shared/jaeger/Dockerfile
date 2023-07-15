FROM jaegertracing/all-in-one@sha256:adb3f3d974f536aed10ba951ac381c409e312d9dab4ed36f6c79e4b8074faa2f
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
