FROM nginx:alpine

# Ensure nogroup exists (Alpine may not ship it)
RUN addgroup -S nogroup || true

COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf

# Remove the stock default server if present
RUN rm -f /etc/nginx/conf.d/default.conf.bak 2>/dev/null || true
