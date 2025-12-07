<?php
// Simple "Number Pattern Fun Lab" - index.php

// Helper function: parse user input into an array of digits 0–9
function parse_sequence($input) {
    // Replace anything that's not a digit with a space
    $cleaned = preg_replace('/[^0-9]+/', ' ', $input);
    $parts = preg_split('/\s+/', trim($cleaned));

    $numbers = [];
    foreach ($parts as $p) {
        if ($p === '') continue;
        // Only accept 0–9
        $n = intval($p);
        if ($n >= 0 && $n <= 9) {
            $numbers[] = $n;
        }
    }
    return $numbers;
}

// Helper: compute frequency of digits 0–9
function frequency_table($numbers) {
    $freq = array_fill(0, 10, 0);
    foreach ($numbers as $n) {
        if ($n >= 0 && $n <= 9) {
            $freq[$n]++;
        }
    }
    return $freq;
}

// Helper: choose a "fun guess" = random digit among the least-frequent ones
function fun_guess($freq) {
    $min = min($freq);
    $candidates = [];
    foreach ($freq as $digit => $count) {
        if ($count === $min) {
            $candidates[] = $digit;
        }
    }
    if (empty($candidates)) {
        // Should never happen, but fallback to random 0–9
        return rand(0, 9);
    }
    // Pick one candidate randomly
    $idx = array_rand($candidates);
    return $candidates[$idx];
}

// Initialize variables
$input_sequence = '';
$numbers = [];
$freq = array_fill(0, 10, 0);
$guess = null;
$error = '';

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $input_sequence = isset($_POST['sequence']) ? trim($_POST['sequence']) : '';

    if ($input_sequence === '') {
        $error = 'Please enter some numbers first.';
    } else {
        $numbers = parse_sequence($input_sequence);
        if (empty($numbers)) {
            $error = 'No valid digits (0–9) were found in your input.';
        } else {
            $freq = frequency_table($numbers);
            $guess = fun_guess($freq);
        }
    }
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Number Pattern Fun Lab</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        :root {
            font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
            background: #0f172a;
            color: #e5e7eb;
        }
        body {
            margin: 0;
            padding: 0;
            display: flex;
            min-height: 100vh;
            justify-content: center;
            align-items: center;
        }
        .container {
            background: #020617;
            border-radius: 18px;
            padding: 24px 20px;
            max-width: 700px;
            width: 100%;
            box-shadow: 0 20px 40px rgba(15, 23, 42, 0.9);
            border: 1px solid #1e293b;
        }
        h1 {
            margin-top: 0;
            font-size: 1.6rem;
            text-align: center;
            color: #e5e7eb;
        }
        p.subtitle {
            margin-top: 4px;
            margin-bottom: 16px;
            text-align: center;
            font-size: 0.9rem;
            color: #9ca3af;
        }
        textarea {
            width: 100%;
            min-height: 100px;
            border-radius: 12px;
            border: 1px solid #1f2937;
            background: #020617;
            color: #e5e7eb;
            padding: 10px 12px;
            font-size: 0.95rem;
            resize: vertical;
            outline: none;
        }
        textarea:focus {
            border-color: #38bdf8;
            box-shadow: 0 0 0 1px #38bdf8;
        }
        .label {
            font-size: 0.9rem;
            margin-bottom: 6px;
            color: #d1d5db;
        }
        .button-row {
            margin-top: 12px;
            display: flex;
            justify-content: flex-end;
            gap: 8px;
        }
        button {
            border-radius: 999px;
            padding: 8px 18px;
            border: none;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: 500;
        }
        .btn-primary {
            background: linear-gradient(135deg, #38bdf8, #6366f1);
            color: white;
        }
        .btn-secondary {
            background: transparent;
            border: 1px solid #4b5563;
            color: #e5e7eb;
        }
        .section {
            margin-top: 18px;
            padding-top: 12px;
            border-top: 1px solid #111827;
        }
        .section-title {
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 8px;
            color: #e5e7eb;
        }
        .error {
            background: #7f1d1d;
            border-radius: 10px;
            padding: 8px 10px;
            font-size: 0.9rem;
            color: #fecaca;
            margin-top: 10px;
        }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(5, minmax(0, 1fr));
            gap: 6px;
            font-size: 0.85rem;
        }
        .stat-item {
            background: #020617;
            border-radius: 10px;
            padding: 8px 8px;
            text-align: center;
            border: 1px solid #1f2937;
        }
        .stat-digit {
            font-size: 0.95rem;
            font-weight: 600;
            color: #e5e7eb;
        }
        .stat-count {
            font-size: 0.8rem;
            color: #9ca3af;
        }
        .badge {
            display: inline-block;
            padding: 2px 8px;
            border-radius: 999px;
            font-size: 0.75rem;
            margin-top: 4px;
        }
        .badge-hot {
            background: rgba(248, 113, 113, 0.15);
            color: #fecaca;
        }
        .badge-cold {
            background: rgba(52, 211, 153, 0.15);
            color: #bbf7d0;
        }
        .guess-box {
            margin-top: 8px;
            padding: 12px;
            border-radius: 12px;
            background: radial-gradient(circle at top left, #1d283a, #020617);
            border: 1px solid #1f2937;
            text-align: center;
        }
        .guess-label {
            font-size: 0.9rem;
            color: #9ca3af;
        }
        .guess-value {
            font-size: 2rem;
            font-weight: 700;
            margin-top: 4px;
        }
        .helper-text {
            font-size: 0.8rem;
            color: #6b7280;
            margin-top: 4px;
        }
        .footer-note {
            margin-top: 14px;
            font-size: 0.75rem;
            color: #6b7280;
            text-align: center;
        }
        @media (max-width: 640px) {
            .container {
                margin: 12px;
                padding: 18px 14px;
            }
            .stats-grid {
                grid-template-columns: repeat(5, 1fr);
            }
        }
    </style>
</head>
<body>
<div class="container">
    <h1>Number Pattern Fun Lab</h1>
    <p class="subtitle">
        Enter any sequence of digits 0–9 (comma, space, or line break separated).<br>
        This tool will show basic stats and generate a <strong>just-for-fun guess</strong>.
    </p>

    <form method="post">
        <div class="label">Your sequence</div>
        <textarea name="sequence" placeholder="Example: 0, 2, 6, 5, 5, 0, 5, 8, 0, 3"><?php
            echo htmlspecialchars($input_sequence, ENT_QUOTES | ENT_SUBSTITUTE, 'UTF-8');
        ?></textarea>
        <div class="helper-text">
            You can paste a long history. Only digits 0–9 are used; everything else is ignored.
        </div>

        <div class="button-row">
            <button type="submit" class="btn-primary">Analyze &amp; Guess</button>
            <button type="button" class="btn-secondary" onclick="document.querySelector('textarea[name=sequence]').value=''">
                Clear
            </button>
        </div>
    </form>

    <?php if ($error): ?>
        <div class="error">
            <?php echo htmlspecialchars($error, ENT_QUOTES | ENT_SUBSTITUTE, 'UTF-8'); ?>
        </div>
    <?php endif; ?>

    <?php if (!$error && !empty($numbers)): ?>
        <div class="section">
            <div class="section-title">Digit frequency (0–9)</div>
            <div class="stats-grid">
                <?php
                $maxFreq = max($freq);
                $minFreq = min($freq);
                foreach ($freq as $digit => $count):
                    ?>
                    <div class="stat-item">
                        <div class="stat-digit"><?php echo $digit; ?></div>
                        <div class="stat-count"><?php echo $count; ?> time<?php echo $count === 1 ? '' : 's'; ?></div>
                        <?php if ($count === $maxFreq && $maxFreq > 0): ?>
                            <div class="badge badge-hot">hot</div>
                        <?php endif; ?>
                        <?php if ($count === $minFreq): ?>
                            <div class="badge badge-cold">cold</div>
                        <?php endif; ?>
                    </div>
                <?php endforeach; ?>
            </div>
        </div>

        <?php if ($guess !== null): ?>
            <div class="section">
                <div class="section-title">Fun guess</div>
                <div class="guess-box">
                    <div class="guess-label">Suggested next digit (just for fun):</div>
                    <div class="guess-value"><?php echo $guess; ?></div>
                    <div class="helper-text">
                        Chosen randomly from the least-frequent digits in your sequence.
                        This is <strong>not</strong> a prediction engine, just a toy pattern tool.
                    </div>
                </div>
            </div>
        <?php endif; ?>
    <?php endif; ?>

    <div class="footer-note">
        This page is for entertainment and pattern visualization only. It does not predict or influence any real system.
    </div>
</div>
</body>
</html>
