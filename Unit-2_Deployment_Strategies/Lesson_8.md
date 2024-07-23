# Rolling Deployments

## Definition

- Strategy to deploy a new version of an application without causing **downtime**.
- They work by creating a single instance of the new version of an application, then shutting off one instance of the old version until all instances have been upgraded.

## Algorithm

1. Create an instance of the new version of the backend
2. Wait until new copy is up ("healthy")
3. Delete an instance of the old version of the backend
4. If any instance of the old version still exist, go back to step 1

## Benefits

- Well supported
- No huge bursts
- Easily reverted

## Cons

- Speed
- API Compatability
