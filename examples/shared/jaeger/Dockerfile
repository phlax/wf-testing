FROM jaegertracing/all-in-one@sha256:da557fdf0186416d43cafefa13f9bf86d941264269a850c40c33b352f9160f31
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
