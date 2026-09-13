# booking-k8s

Interactive, English-language introduction to distributed systems and Kubernetes through a simulated Booking.com request.

Follow a request from Baku through DNS, CDN, region routing, a load balancer, Kubernetes, Redis, databases and asynchronous payment processing. The architecture, locations and timings are illustrative, not a verified description of Booking.com's infrastructure.

## Run locally

```sh
python -m http.server 4173 --directory dist
```

Open http://localhost:4173. No package installation or build is required.

## Deploy on Render

Create a Blueprint in Render and connect this repository. The root `render.yaml` configures a Static Site publishing `dist` with automatic deployments on commits.

For manual Static Site setup, leave Root Directory empty, use `echo "Static presentation is ready"` for Build Command and `dist` for Publish Directory.

## Source

- `dist/index.html`: page shell.
- `dist/story.js`: tutorial, diagrams, request simulations and explanations.
- `dist/story.css`: responsive layout and animations.
- `render.yaml`: Render deployment configuration.

Searches, bookings, payments and failure switches are local simulations. No requests are sent to Booking.com or a payment provider.
