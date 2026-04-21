---
layout: post
title: "Machine Unlearning: The Right to Be Forgotten Is Harder Than It Sounds"
date: 2025-03-02 09:00:00 +1100
description: >
  AI systems are now legally required to delete personal data on request. But deletion
  is more complicated than it sounds — the knowledge lives in the weights, distributed,
  entangled and invisible.
tags: [machine-learning, trustworthy-ai, federated-learning, privacy]
categories: [research]
featured: false
---

AI systems are now legally required to delete personal data on request. But deletion is more complicated than it sounds.

You could assume the fix is straightforward — find the source data, remove it, done. But by the time you delete the source file, the model has already learned from it. The knowledge lives in the weights, distributed, entangled and invisible. Deleting the source changes nothing.

This is one of the problems that **machine unlearning** is trying to solve.

With regulations like GDPR's *right to erasure* — commonly known as the "right to be forgotten" — and the EU AI Act creating new compliance obligations, the ability to selectively remove information from a trained model is no longer a theoretical curiosity. It's becoming a practical requirement in healthcare, in legal AI, and in fact anything trained on personal data.

## The Naive Fix Doesn't Scale

The obvious solution is simple: retrain from scratch without the offending data. But at production scale, retraining can cost millions of dollars and take weeks. You can't do that every time someone requests deletion.

So one approach researchers have developed is **approximate unlearning** — methods that modify existing weights to make a model behave *as if* it never saw certain data, without needing a full retrain.

## The Verification Problem

But here is the part that is a key concern: how do you verify it worked?

With approximate methods, standard accuracy metrics often look completely normal even when unlearning has failed. The model's overall performance is fine. But look more carefully at specific subpopulations, at individual nodes in distributed systems, and the forgotten data isn't gone at all — it's just hidden.

This gap between *"the numbers look good"* and *"the model has actually forgotten"* is one of the most important open problems in trustworthy AI right now.

## The Decentralised Case

It gets harder still when you move beyond a single centralised model.

In decentralised systems — where there is no single authority, no single model, and knowledge propagates across nodes through communication — unlearning becomes a fundamentally different problem that the field is only beginning to address.

We're building systems that need to forget on demand. We don't yet have reliable ways to verify they have.

This is something I'm working on directly. More to come.
