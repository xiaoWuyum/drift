# Scene Recommender

`sceneRecommender.ts` is the current recommendation layer behind Create Screen's "AI" button.

It is intentionally rule-based for now:

1. Read the user's text input.
2. Match scene keywords such as city, rain, space, beach, or snow.
3. Return a structured `SceneRecommendation`.
4. `CreateScreen` applies that recommendation to background, tag, song, ambience, title, and prompt.

Expected output shape:

```ts
{
  backgroundId: string;
  tag: string;
  title: string;
  prompt: string;
  songId: string;
  activeSounds: Record<string, number>;
  reason: string;
}
```

When replacing this with a real AI call, keep the same output shape so the UI does not need to change.
