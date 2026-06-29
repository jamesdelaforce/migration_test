Statsig
Remote Config 

openFeature route - this will be a different flow 

Native SDK route 
1. authenticate statsig account against the API
    For programmatic access, you can leverage Statsig's public APIs or Console API to fetch flag data
2. also input mixpanel details 
    mixpanel service account 
3. select and list all flags

what is included - in buildRuleset()
1. rollout splits
2. variant splits
3. basic structure

what is not included - Statsig rules like:
User attribute targeting (country, email, custom properties)
Segment/cohort conditions
Progressive rollouts
A/B test assignment rules
User ID overrides
Environment targeting
Custom conditions

{
  name: null,
  runtime_evaluation_rule: null,     // ❌ No targeting rules
  runtime_event_rule: null,          // ❌ No event-based triggers
  cohort_hash: null,                 // ❌ No cohort/segment targeting
  variant_override: null,            // ❌ No user overrides
  rollout_percentage: rolloutPct,    // ✅ Only this is migrated
  variant_splits: vs                 // ✅ Only even splits
}


todo
1. the migration html files are way too long, need to clean up and modularise
2. what is dry run?
3. test feature gate with stableID (device ID)
4. test feature gate with customIDs? (group analytics)
5. test experiment
6. test dynamic config

