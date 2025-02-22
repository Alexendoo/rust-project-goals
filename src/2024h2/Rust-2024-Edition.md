# Rust 2024 Edition

| Metadata |                 |
| -------- | --------------- |
| Owner(s) | @traviscross    |
| Teams    | [Lang], [Types] |
| Status   | Flagship        |

## Summary

Feature complete status for Rust 2024, with final release to occur in early 2025.

## Motivation

[RFC #3501] confirmed the desire to ship a Rust edition in 2024, continuing the pattern of shipping a new Rust edition every 3 years. Our goal for 2024 H2 is to stabilize a new edition on nightly by the end of 2024.

### The status quo

Editions are a powerful tool for Rust but organizing them continues to be a "fire drill" each time. We have a preliminary set of 2024 features assembled but work needs to be done to marshal and drive (some subset of...) them to completion.

### The next six months

The major goal this year is to release the edition on nightly. Top priority items are as follows:

| Item                           | Tracking                                        | RFC                                           | More to do? |
| ------------------------------ | ----------------------------------------------- | --------------------------------------------- | ----------- |
| Reserve `gen` keyword          | https://github.com/rust-lang/rust/issues/123904 | https://github.com/rust-lang/rust/pull/116447 | No.         |
| Lifetime Capture Rules 2024    | https://github.com/rust-lang/rust/issues/117587 | https://github.com/rust-lang/rfcs/pull/3498   | Yes.        |
| Precise capturing (dependency) | https://github.com/rust-lang/rust/issues/123432 | https://github.com/rust-lang/rfcs/pull/3617   | Yes.        |
| Change fallback to `!`         | https://github.com/rust-lang/rust/issues/123748 | N/A                                           | Yes.        |

The full list of tracked items [can be found using the `A-edition-2024` label.](https://github.com/rust-lang/rust/issues?q=label%3AC-tracking-issue+label%3AA-edition-2024).

### The "shiny future" we are working towards

The Edition will be better integrated into our release train. Nightly users will be able to "preview" the next edition just like they would preview any other unstable feature. New features that require new syntax or edition-related changes will land throughout the edition period. Organizing the new edition will be rel

## Design axioms

The "Edition Axioms" were [laid out in RFC #3085](https://rust-lang.github.io/rfcs/3085-edition-2021.html#guide-level-explanation):

* **Editions do not split the ecosystem.** The most important rule for editions is that crates in one edition can interoperate seamlessly with crates compiled in other editions.
* **Edition migration is easy and largely automated.** Whenever we release a new edition, we also release tooling to automate the migration. The tooling is not necessarily perfect: it may not cover all corner cases, and manual changes may still be required. 
* **Users control when they adopt the new edition.** We recognize that many users, particularly production users, will need to schedule time to manage an Edition upgrade as part of their overall development cycle.
* **Rust should feel like “one language”.** We generally prefer uniform behavior across all editions of Rust, so long as it can be achieved without compromising other design goals. 
* **Editions are meant to be adopted.** We don’t force the edition on our users, but we do feel free to encourage adoption of the edition through other means.

## Ownership and team asks

**Owner:** @traviscross

| Subgoal                  | Owner(s) or team(s)      | Notes |
| ------------------------ | ------------------------ | ----- |
| Stabilization decision   | ![Team][] [Lang] [Types] |       |
| Top-level Rust blog post | ![Team][] [LC]           |       |

## Outputs and milestones

* *Owner:* @traviscross

### Outputs

* Edition release complete with
    * announcement blog post
    * edition migration guide

### Milestones

| Date       | Version       | Edition stage           |
| ---------- | ------------- | ----------------------- |
| 2024-10-11 | Branch  v1.83 | Go / no go on all items |
| 2024-10-17 | Release v1.82 | Rust 2024 nightly beta  |
| 2025-01-03 | Branch  v1.85 | Cut Rust 2024 to beta   |
| 2025-02-20 | Release v1.85 | Release Rust 2024       |

## Frequently asked questions

None yet.