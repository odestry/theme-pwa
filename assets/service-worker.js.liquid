// Define a name for our cache
const CACHE_NAME = 'v1_cache';

const urlsToCache = [
  '/',
  // Add more URLs and assets that you want to cache...
];

// Installation event. This is triggered as soon as the worker executes,
// and it's only called once per service worker. This is the perfect time
// to cache our static assets.
self.addEventListener('install', event => {
  event.waitUntil(
    // Open the cache
    caches.open(CACHE_NAME)
      .then((cache) => {
        // Add all URLs to the cache
        return cache.addAll(urlsToCache)
          .then(() => {
            // Skip waiting forces the waiting service worker to become the active service worker.
            self.skipWaiting()
          });
      })
      // If something went wrong with the cache, log it.
      .catch(error => console.log('Failed to cache', error))
  );
});

// Activate event. This is a good time to clean up old caches.
self.addEventListener('activate', event => {
  const cacheWhitelist = [CACHE_NAME];

  event.waitUntil(
    // Get all cache keys (cache names)
    caches.keys()
      .then(cacheNames => {
        // Return a single promise that resolves when all old caches are deleted.
        return Promise.all(
          cacheNames.map(cacheName => {
            // If this cache name isn't present in the whitelist, delete it.
            if (cacheWhitelist.indexOf(cacheName) === -1) {
              return caches.delete(cacheName);
            }
          })
        );
      })
      .then(() => {
        // Enables the newly installed service worker to take control of the page
        // and start handling fetch events.
        self.clients.claim()
      })
  );
});

// Fetch event. This triggers every time a page controlled by this service worker makes a request.
self.addEventListener('fetch', event => {
  event.respondWith(
    // Check if the request is for something we have in our cache
    caches.match(event.request)
      .then(response => {
        // If the response is in the cache, return it, else fetch it from the network.
        if (response) {
          return response;
        }
        return fetch(event.request);
      })
  );
});
