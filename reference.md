# Reference
## Brains
<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">list</a>() -> LivingBrain.Brain[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List every brain owned by the calling subject, most recently updated first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">create</a>({ ...params }) -> LivingBrain.Brain</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new brain for the calling subject. A brain is an isolated knowledge vault: every capture, page, and connection belongs to exactly one brain. The `x-subject-id` header determines who owns it.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.create({
    name: "Customer Memory"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.CreateBrainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">bulkStats</a>({ ...params }) -> Record&lt;string, LivingBrain.BrainStats&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Aggregate counts for many brains in one round trip. Pass a comma-separated `ids` list; brains the caller cannot access are omitted rather than erroring.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.bulkStats();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.BulkStatsBrainsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">get</a>({ ...params }) -> LivingBrain.Brain</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single brain by ID, including its name, description, and brief settings.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.get({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.GetBrainsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">remove</a>({ ...params }) -> LivingBrain.DeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a brain along with all of its pages, sources, connections, and change history. This cannot be undone.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.remove({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RemoveBrainsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">update</a>({ ...params }) -> LivingBrain.Brain</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a brain's mutable fields, such as its name or description. Omitted fields are left unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.update({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.UpdateBrainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">stats</a>({ ...params }) -> LivingBrain.BrainStats</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Aggregate counts for a single brain — pages, sources, connections, and unacknowledged changes. Useful for dashboard headline numbers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.stats({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.StatsBrainsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">updateBriefSettings</a>({ ...params }) -> LivingBrain.Brain</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the daily-brief schedule and delivery settings for a brain, including whether briefs are enabled and what time they are generated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.updateBriefSettings({
    brainId: "brainId",
    briefSettings: {
        enabled: true,
        hourLocal: 7,
        timezone: "Europe/Helsinki"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.UpdateBriefSettingsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.brains.<a href="/src/api/resources/brains/client/Client.ts">runBrief</a>({ ...params }) -> LivingBrain.BriefRunResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate this brain's daily brief immediately instead of waiting for its scheduled run. Returns the brief content once generation completes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.brains.runBrief({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RunBriefBrainsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BrainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Captures
<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">capture</a>({ ...params }) -> LivingBrain.IngestSource</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Push a single item into a brain for ingestion. Accepts notes, URLs, raw text, chat transcripts, and PDF/DOCX/PPTX documents. Capture is asynchronous: this returns an ingest source whose `status` you can poll or receive via webhook.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.captures.capture({
    brainId: "brainId",
    body: {
        kind: "note"
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.CaptureCapturesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">captureBatch</a>({ ...params }) -> LivingBrain.CaptureBatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Push many captures in a single request. Each item is processed independently, so a malformed entry fails on its own without rejecting the whole batch.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.captures.captureBatch({
    brainId: "brainId",
    items: [{
            kind: "note",
            content: "First note"
        }, {
            kind: "note",
            content: "Second note"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.CaptureBatchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">captureChatTurn</a>({ ...params }) -> LivingBrain.CaptureChatTurnResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Submit a single chat turn for worthiness classification. The service decides whether the turn contains durable knowledge and only captures it if so, which keeps conversational filler out of the brain.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.captures.captureChatTurn({
    brainId: "brainId",
    text: "I just closed the Series A, focus shifts to hiring engineers.",
    sender: "user"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.CaptureChatTurnRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">listSources</a>({ ...params }) -> core.Page&lt;LivingBrain.IngestSource, LivingBrain.SourceList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List ingest sources for a brain, optionally filtered by processing status. Use this to surface an ingestion queue or to find sources that failed to compile.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.captures.listSources({
    brainId: "brainId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.captures.listSources({
    brainId: "brainId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ListSourcesCapturesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">retrySource</a>({ ...params }) -> LivingBrain.SourceRetryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retry compiling an ingest source that previously failed. Only sources in a failed state can be retried.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.captures.retrySource({
    brainId: "brainId",
    sourceId: "sourceId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RetrySourceCapturesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.captures.<a href="/src/api/resources/captures/client/Client.ts">removeSource</a>({ ...params }) -> LivingBrain.DeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an ingest source. Pages already derived from the source are retained unless you delete them separately.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.captures.removeSource({
    brainId: "brainId",
    sourceId: "sourceId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RemoveSourceCapturesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CapturesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Workspace
<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">searchPages</a>({ ...params }) -> LivingBrain.SearchResult[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Search pages using combined semantic and keyword matching. Results are ranked by relevance and include a snippet showing why each page matched.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.searchPages({
    brainId: "brainId",
    query: "what does the customer care about?"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.SearchRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">index</a>({ ...params }) -> LivingBrain.IndexEntry[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a compact index of the brain's top pages, formatted for injection into an LLM prompt. This is the intended way to give an agent working context without sending the whole brain.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.index({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.IndexWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">graph</a>({ ...params }) -> LivingBrain.Graph</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a renderable subgraph of nodes and edges for visualizing how the brain's pages relate. Use `nodeLimit` to keep the payload small enough to draw.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.graph({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.GraphWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">listPages</a>({ ...params }) -> core.Page&lt;LivingBrain.Page, LivingBrain.PageList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List pages in a brain with offset pagination. Filter by bucket or status, and optionally include deprecated pages that are normally hidden.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.workspace.listPages({
    brainId: "brainId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.workspace.listPages({
    brainId: "brainId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ListPagesWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">buckets</a>({ ...params }) -> Record&lt;string, number&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return per-bucket page counts for the brain — the fastest way to render bucket navigation with badges.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.buckets({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.BucketsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">getPage</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read a single page by slug. This bumps the page's `lastReferencedAt`, which feeds the brain health score — use it when a human or agent actually consumes the content.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.getPage({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.GetPageWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">deletePermanently</a>({ ...params }) -> LivingBrain.PageDeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a page and every record that depends on it, including its versions and connections. This cannot be undone.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.deletePermanently({
    brainId: "brainId",
    slug: "slug",
    permanent: "true"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.DeletePermanentlyWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">pageVersions</a>({ ...params }) -> LivingBrain.PageVersion[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List a page's version history, newest first. Every content edit and automated recompile produces a version.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.pageVersions({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.PageVersionsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">pageConnections</a>({ ...params }) -> LivingBrain.PageConnections</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the connections attached to a single page, with the related page inlined on each connection.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.pageConnections({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.PageConnectionsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">editContent</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Manually overwrite a page's content. This creates a new version, so the previous content stays retrievable through the version history.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.editContent({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.UpdatePageContentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">moveBucket</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Move a page into a different bucket. Buckets are the brain's top-level organizational grouping.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.moveBucket({
    brainId: "brainId",
    slug: "slug",
    bucket: "inbox"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.MovePageBucketRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">pin</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Pin or unpin a page. Pinned pages are prioritized in the prompt index and are exempt from deprecation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.pin({
    brainId: "brainId",
    slug: "slug",
    pinned: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.PinPageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">rename</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Rename a page's title and slug. Existing connections follow the page, but any external references to the old slug will break.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.rename({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RenamePageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">recover</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Recover a deprecated page and return it to active status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.recover({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RecoverWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">resolve</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resolve a contested page. A page becomes contested when newly captured material contradicts what the page already asserts; resolving records which version wins.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.resolve({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ResolveContestedRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">reviewed</a>({ ...params }) -> LivingBrain.Page</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Legacy alias for recovering a deprecated page. Prefer `recover` in new code; this endpoint is retained for backwards compatibility.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.reviewed({
    brainId: "brainId",
    slug: "slug"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ReviewedWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">changes</a>({ ...params }) -> core.Page&lt;LivingBrain.ChangeEvent, LivingBrain.ChangeList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List change-feed events with offset pagination. This is the primary way to sync an external system: poll with `since`, or filter to `unackedOnly` to build an inbox.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.workspace.changes({
    brainId: "brainId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.workspace.changes({
    brainId: "brainId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ChangesWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">ackChange</a>({ ...params }) -> LivingBrain.ChangeEvent</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Acknowledge a single change event, removing it from unacknowledged views.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.ackChange({
    brainId: "brainId",
    changeId: "changeId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.AckChangeWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">ackAll</a>({ ...params }) -> LivingBrain.AckAllResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Acknowledge every outstanding change event in one call, and return how many were cleared.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.ackAll({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.AckAllWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">listConnections</a>({ ...params }) -> core.Page&lt;LivingBrain.Connection, LivingBrain.ConnectionList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List connections across the whole brain with offset pagination. Filter by strength, or restrict to connections the user has not yet dismissed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.workspace.listConnections({
    brainId: "brainId"
});
for await (const item of pageableResponse) {
    console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.workspace.listConnections({
    brainId: "brainId"
});
while (page.hasNextPage()) {
    page = page.getNextPage();
}

// You can also access the underlying response
const response = page.response;

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ListConnectionsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">ackConnection</a>({ ...params }) -> LivingBrain.Connection</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Dismiss a connection so it stops appearing in unacknowledged views. The connection itself is preserved.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.ackConnection({
    brainId: "brainId",
    connectionId: "connectionId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.AckConnectionWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">getScore</a>({ ...params }) -> LivingBrain.BrainScore</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the brain's health score with its contributing factors and metrics. The score reflects coverage, freshness, and connectedness.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.getScore({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.GetScoreWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">scoreHistory</a>({ ...params }) -> LivingBrain.ScoreHistory</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the score trend over a time range, including the delta versus the start of the period.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.scoreHistory({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ScoreHistoryWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">scoreSuggestions</a>({ ...params }) -> LivingBrain.ScoreSuggestions</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return concrete, ranked suggestions for raising the brain's health score, derived from whichever factors are currently weakest.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.scoreSuggestions({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ScoreSuggestionsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">getProfile</a>({ ...params }) -> LivingBrain.BrainProfile | null</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the brain profile — the standing directives and context that shape how the brain interprets and organizes new captures.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.getProfile({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.GetProfileWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">updateProfile</a>({ ...params }) -> LivingBrain.BrainProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the brain profile's directives. These take effect on subsequent captures, not retroactively.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.updateProfile({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.UpdateBrainProfileRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">profileSuggestions</a>({ ...params }) -> LivingBrain.ProfileSuggestions</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Suggest profile fields inferred from what the brain already contains. Best-effort: returns an empty set when there is not yet enough signal.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.profileSuggestions({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ProfileSuggestionsWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workspace.<a href="/src/api/resources/workspace/client/Client.ts">exportMarkdown</a>({ ...params }) -> LivingBrain.MarkdownExport</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export the entire brain as a single markdown bundle, suitable for backup or for handing to another tool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.workspace.exportMarkdown({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ExportMarkdownWorkspaceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WorkspaceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">list</a>() -> LivingBrain.WebhookSubscription[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all webhook subscriptions for the calling subject. Signing secrets are not included.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">create</a>({ ...params }) -> LivingBrain.CreateWebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register a webhook endpoint and receive its signing secret. The secret is returned only on creation — store it immediately, as it cannot be retrieved again.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.create({
    url: "https://your-app.com/webhooks/living-brain"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.CreateWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">remove</a>({ ...params }) -> LivingBrain.DeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a webhook subscription. Deliveries stop immediately.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.remove({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.RemoveWebhooksRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">update</a>({ ...params }) -> LivingBrain.WebhookSubscription</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a webhook subscription's URL or subscribed event types. The signing secret is unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.update({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.UpdateWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Telegram
<details><summary><code>client.telegram.<a href="/src/api/resources/telegram/client/Client.ts">status</a>({ ...params }) -> LivingBrain.TelegramConnection | null</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the current Telegram bot connection status for a brain, including the connected bot's username when one is linked.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.telegram.status({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.StatusTelegramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TelegramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.telegram.<a href="/src/api/resources/telegram/client/Client.ts">connect</a>({ ...params }) -> LivingBrain.TelegramConnection</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Connect a Telegram bot to a brain so messages sent to the bot are captured automatically.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.telegram.connect({
    brainId: "brainId",
    botToken: "123456:ABC-DEF..."
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.ConnectTelegramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TelegramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.telegram.<a href="/src/api/resources/telegram/client/Client.ts">disconnect</a>({ ...params }) -> LivingBrain.TelegramDisconnectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Disconnect the Telegram bot from a brain. Already-captured messages are retained.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.telegram.disconnect({
    brainId: "brainId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `LivingBrain.DisconnectTelegramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TelegramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

