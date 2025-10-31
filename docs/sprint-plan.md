gantt
    title Mini Bingo — Sprint Plan (Group 9)
    dateFormat  YYYY-MM-DD
    excludes    weekends
    axisFormat  %b %d

    section Sprint 1 — Core Mechanics
    Kickoff + Backlog Finalization        :milestone, m1, 2025-11-03, 1d
    Repo/CI Scaffolding (X-CI)            :active,   s1_ci, 2025-11-03, 1d
    US-1 Card Datamodel & Ranges          :         s1_card_impl, 2025-11-03, 3d
    US-1 Card Tests & Validations         :         s1_card_tests, after s1_card_impl, 2d
    US-2 Draw Pool (no-repeat, seedable)  :         s1_draw_impl, 2025-11-05, 3d
    US-2 Draw Tests (determinism/peek)    :         s1_draw_tests, after s1_draw_impl, 3d
    US-3 Marking & Win Detection (impl)   :         s1_rules_impl, 2025-11-10, 3d
    US-3 Rules Tests (rows/cols/diags)    :         s1_rules_tests, after s1_rules_impl, 2d
    Integration + Coverage >=80%          :         s1_int_cov, after s1_rules_tests, 1d
    Sprint 1 Review & Retro               :milestone, m2, 2025-11-14, 1d

    section Sprint 2 — CLI & Orchestration
    Sprint 2 Planning                     :milestone, m3, 2025-11-17, 1d
    GameState wiring (models->loop)       :         s2_gamestate, 2025-11-17, 2d
    CLI Command Handlers (draw/show/new/quit):     s2_cli_cmds, after s2_gamestate, 3d
    Output Formatting (card & history)    :         s2_fmt, overlap s2_cli_cmds, 2025-11-19, 2d
    README Run Instructions + Examples    :         s2_readme, after s2_cli_cmds, 2d
    Rules Edge Tests & Smoke Tests        :         s2_tests, 2025-11-17, 5d
    Packaging Touch-ups (__init__, pyproject) :    s2_pkg, after s2_readme, 1d
    Buffer/Polish (bug fixes)             :         s2_buffer, 2025-11-24, 2d
    Sprint 2 Review + Live Demo           :milestone, m4, 2025-11-26, 1d
    Release v0.1 tag + Submission         :milestone, m5, 2025-11-28, 1d
