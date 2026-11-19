<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cookie Empire AAA v1.5 | אימפריית העוגיות</title>
    <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;500;700;900&display=swap" rel="stylesheet">

    <style>
        :root {
            --bg-espresso: #140b07;
            --bg-chocolate: #26140c;
            --panel-glass: rgba(36, 19, 11, 0.84);
            --card-surface: rgba(54, 29, 17, 0.92);
            --card-hover: rgba(74, 41, 24, 0.98);
            --gold-primary: #f5c249;
            --gold-bright: #ffe082;
            --gold-dark: #b8860b;
            --caramel: #d97724;
            --cream-text: #fff7e8;
            --muted-cocoa: #d4b8a3;
            --border-subtle: rgba(245, 194, 73, 0.22);
            --border-gold: rgba(245, 194, 73, 0.68);
            --danger: #d32f2f;
        }

        * {
            box-sizing: border-box;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            margin: 0;
            padding: 0;
            min-height: 100vh;
            font-family: 'Rubik', sans-serif;
            color: var(--cream-text);
            background:
                radial-gradient(circle at 50% 18%, rgba(217, 119, 36, 0.22) 0%, rgba(184, 134, 11, 0.08) 34%, transparent 62%),
                radial-gradient(circle at 18% 85%, rgba(120, 58, 20, 0.25) 0%, transparent 48%),
                linear-gradient(175deg, #22120a 0%, #160c07 55%, #0d0704 100%);
            display: flex;
            flex-direction: column;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* תאורת אווירה חמה ומרקם קטיפה עדין ללא רקע אוקיינוס */
        body::before {
            content: "";
            position: fixed;
            inset: 0;
            pointer-events: none;
            background:
                radial-gradient(ellipse 80% 45% at 50% 42%, rgba(245, 194, 73, 0.09) 0%, transparent 72%),
                radial-gradient(circle at 85% 20%, rgba(217, 119, 36, 0.1) 0%, transparent 42%);
            z-index: 0;
        }

        body::after {
            content: none;
        }

        /* סרגל עליון יוקרתי (HUD) */
        .top-hud {
            width: 100%;
            max-width: 1200px;
            margin: 16px auto 12px;
            padding: 12px 22px;
            background: var(--panel-glass);
            backdrop-filter: blur(14px);
            -webkit-backdrop-filter: blur(14px);
            border: 1px solid var(--border-subtle);
            border-radius: 20px;
            box-shadow: 0 12px 35px rgba(0, 0, 0, 0.55), inset 0 1px 0 rgba(255, 255, 255, 0.06);
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 16px;
            z-index: 10;
        }

        .bakery-identity {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .brand-emblem {
            width: 44px;
            height: 44px;
            border-radius: 14px;
            background: linear-gradient(135deg, #f5c249, #b8860b);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(245, 194, 73, 0.35);
            flex-shrink: 0;
        }

        .bakery-name-wrapper {
            display: flex;
            flex-direction: column;
        }

        .bakery-name {
            font-size: 1.25rem;
            font-weight: 800;
            color: var(--gold-bright);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: color 0.2s;
            padding: 2px 6px;
            border-radius: 8px;
            margin-right: -6px;
        }

        .version-pill {
            font-size: 0.72rem;
            font-weight: 800;
            color: #101b24;
            background: linear-gradient(135deg, var(--gold-bright), var(--gold-primary));
            padding: 2px 8px;
            border-radius: 999px;
            line-height: 1.2;
        }

        .bakery-name:hover {
            background: rgba(245, 194, 73, 0.12);
            color: #ffffff;
        }

        .edit-hint {
            font-size: 0.72rem;
            color: var(--muted-cocoa);
            font-weight: 400;
        }

        /* מד רמה ו-XP */
        .level-progress-area {
            flex: 1;
            min-width: 220px;
            max-width: 380px;
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        .level-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
        }

        .level-badge {
            background: linear-gradient(90deg, rgba(245, 194, 73, 0.2), rgba(217, 119, 36, 0.2));
            border: 1px solid var(--border-gold);
            color: var(--gold-bright);
            padding: 2px 10px;
            border-radius: 12px;
            font-weight: 700;
        }

        .xp-text {
            color: var(--muted-cocoa);
            font-size: 0.78rem;
        }

        .xp-bar-track {
            width: 100%;
            height: 8px;
            background: rgba(0, 0, 0, 0.55);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .xp-bar-fill {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, var(--caramel), var(--gold-primary), var(--gold-bright));
            border-radius: 10px;
            transition: width 0.35s cubic-bezier(0.22, 1, 0.36, 1);
            box-shadow: 0 0 10px rgba(245, 194, 73, 0.6);
        }

        /* כפתורי פעולה בסרגל */
        .hud-actions {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .hud-btn {
            background: rgba(255, 255, 255, 0.06);
            border: 1px solid var(--border-subtle);
            color: var(--cream-text);
            height: 40px;
            padding: 0 14px;
            border-radius: 12px;
            font-family: inherit;
            font-size: 0.85rem;
            font-weight: 600;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: all 0.2s;
        }

        .hud-btn:hover {
            background: rgba(245, 194, 73, 0.16);
            border-color: var(--border-gold);
            transform: translateY(-1px);
        }

        .hud-btn.danger-confirm {
            background: var(--danger);
            border-color: #ff5252;
            color: #fff;
        }

        /* פריסת הבמה המרכזית */
        .main-stage {
            width: 100%;
            max-width: 1200px;
            padding: 0 16px 28px;
            display: grid;
            grid-template-columns: 1fr 1.25fr;
            gap: 24px;
            z-index: 5;
        }

        @media (max-width: 880px) {
            .main-stage {
                grid-template-columns: 1fr;
            }
            .top-hud {
                width: calc(100% - 32px);
            }
        }

        /* תיבת המאפייה המרכזית */
        .bakery-chamber {
            background: linear-gradient(165deg, rgba(48, 28, 18, 0.85) 0%, rgba(24, 13, 8, 0.92) 100%);
            backdrop-filter: blur(16px);
            border: 1px solid var(--border-subtle);
            border-radius: 28px;
            padding: 28px 24px;
            min-height: 540px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            position: relative;
            overflow: hidden;
            box-shadow: 0 24px 60px rgba(0, 0, 0, 0.65), inset 0 1px 0 rgba(255, 255, 255, 0.08);
            transition: border-color 0.4s ease, box-shadow 0.4s ease;
        }

        /* אפקט טירוף זהב על תיבת המאפייה */
        .bakery-chamber.frenzy-mode {
            border: 2px solid var(--gold-primary);
            box-shadow: 0 0 45px rgba(245, 194, 73, 0.35), inset 0 0 35px rgba(245, 194, 73, 0.14);
        }

        /* תצוגת מונה העוגיות */
        .counter-display {
            width: 100%;
            background: rgba(14, 8, 5, 0.6);
            border: 1px solid rgba(245, 194, 73, 0.15);
            border-radius: 22px;
            padding: 18px 20px;
            text-align: center;
            position: relative;
            z-index: 6;
            box-shadow: inset 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        .cookie-total {
            font-size: clamp(2.4rem, 5vw, 3.4rem);
            font-weight: 900;
            background: linear-gradient(180deg, #ffffff 10%, var(--gold-bright) 55%, var(--gold-primary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 0;
            line-height: 1.1;
            filter: drop-shadow(0 4px 12px rgba(245, 194, 73, 0.25));
        }

        .cookie-label {
            font-size: 0.9rem;
            color: var(--muted-cocoa);
            letter-spacing: 1px;
            margin-top: 2px;
            font-weight: 500;
        }

        .metrics-row {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin-top: 12px;
            flex-wrap: wrap;
        }

        .metric-pill {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.07);
            padding: 6px 14px;
            border-radius: 14px;
            font-size: 0.88rem;
            color: var(--cream-text);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .metric-pill strong {
            color: var(--gold-primary);
            font-weight: 800;
        }

        /* סרגל טירוף זהב (Frenzy Bar) */
        .frenzy-hud {
            display: none;
            width: 100%;
            margin-top: 12px;
            background: rgba(245, 194, 73, 0.14);
            border: 1px solid var(--gold-primary);
            border-radius: 14px;
            padding: 8px 12px;
            animation: frenzyGlow 1s infinite alternate;
        }

        @keyframes frenzyGlow {
            from { box-shadow: 0 0 8px rgba(245, 194, 73, 0.25); }
            to { box-shadow: 0 0 18px rgba(245, 194, 73, 0.6); }
        }

        .frenzy-label {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            font-weight: 800;
            color: var(--gold-bright);
            margin-bottom: 5px;
        }

        .frenzy-track {
            width: 100%;
            height: 6px;
            background: rgba(0, 0, 0, 0.6);
            border-radius: 6px;
            overflow: hidden;
        }

        .frenzy-fill {
            height: 100%;
            width: 100%;
            background: linear-gradient(90deg, #ff9800, #ffe082);
            transition: width 0.1s linear;
        }

        /* במת העוגייה התלת-ממדית */
        .cookie-pedestal {
            position: relative;
            width: 280px;
            height: 280px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 14px 0;
        }

        .light-rays {
            position: absolute;
            width: 340px;
            height: 340px;
            border-radius: 50%;
            background: repeating-conic-gradient(
                from 0deg,
                rgba(245, 194, 73, 0.11) 0deg 12deg,
                transparent 12deg 24deg
            );
            mask-image: radial-gradient(circle, rgba(0,0,0,1) 20%, rgba(0,0,0,0) 68%);
            -webkit-mask-image: radial-gradient(circle, rgba(0,0,0,1) 20%, rgba(0,0,0,0) 68%);
            animation: rotateSlow 24s linear infinite;
            pointer-events: none;
            z-index: 1;
        }

        @keyframes rotateSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .ambient-aura {
            position: absolute;
            width: 240px;
            height: 240px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(217, 119, 36, 0.35) 0%, transparent 70%);
            pointer-events: none;
            animation: auraBreathe 3.2s ease-in-out infinite;
            z-index: 1;
        }

        @keyframes auraBreathe {
            0%, 100% { transform: scale(0.95); opacity: 0.7; }
            50% { transform: scale(1.12); opacity: 1; }
        }

        #hero-cookie-btn {
            background: none;
            border: none;
            padding: 0;
            width: 235px;
            height: 235px;
            border-radius: 50%;
            cursor: pointer;
            position: relative;
            z-index: 4;
            transition: transform 0.09s cubic-bezier(0.2, 1.4, 0.4, 1);
            filter: drop-shadow(0 22px 28px rgba(0, 0, 0, 0.75));
        }

        #hero-cookie-btn:hover {
            transform: scale(1.045);
        }

        #hero-cookie-btn:active {
            transform: scale(0.91) rotate(-3deg);
        }

        #hero-cookie-btn svg {
            width: 100%;
            height: 100%;
            display: block;
            overflow: visible;
        }

        /* עוגיית זהב אוטומטית (מופיעה אך ורק בתוך .bakery-chamber) */
        #golden-cookie-entity {
            position: absolute;
            width: 84px;
            height: 84px;
            border: none;
            background: radial-gradient(circle, rgba(255, 224, 130, 0.42) 0%, transparent 72%);
            border-radius: 50%;
            padding: 0;
            cursor: pointer;
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 25;
            animation: goldenFloat 1.4s ease-in-out infinite alternate;
        }

        #golden-cookie-entity svg {
            width: 68px;
            height: 68px;
            filter: drop-shadow(0 0 16px rgba(255, 215, 0, 0.95));
            transition: transform 0.15s ease;
        }

        #golden-cookie-entity:hover svg {
            transform: scale(1.16) rotate(8deg);
        }

        @keyframes goldenFloat {
            0% { transform: translateY(0) scale(0.95) rotate(-6deg); }
            100% { transform: translateY(-12px) scale(1.08) rotate(6deg); }
        }

        /* שורת הישגים מהירה בתחתית תיבת המאפייה */
        .achievements-strip {
            width: 100%;
            background: rgba(0, 0, 0, 0.35);
            border: 1px solid rgba(255, 255, 255, 0.06);
            border-radius: 16px;
            padding: 10px 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            z-index: 6;
        }

        .ach-title {
            font-size: 0.82rem;
            color: var(--muted-cocoa);
            font-weight: 600;
            white-space: nowrap;
        }

        .ach-icons {
            display: flex;
            gap: 6px;
            flex-wrap: wrap;
            justify-content: flex-end;
        }

        .ach-pip {
            width: 28px;
            height: 28px;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.08);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9rem;
            filter: grayscale(100%) opacity(0.35);
            transition: all 0.3s ease;
            position: relative;
        }

        .ach-pip.unlocked {
            filter: none;
            background: linear-gradient(135deg, rgba(245, 194, 73, 0.25), rgba(217, 119, 36, 0.2));
            border-color: var(--gold-primary);
            box-shadow: 0 0 10px rgba(245, 194, 73, 0.3);
        }

        /* אזור החנות היוקרתית */
        .store-chamber {
            background: linear-gradient(165deg, rgba(44, 25, 16, 0.85) 0%, rgba(22, 12, 7, 0.92) 100%);
            backdrop-filter: blur(16px);
            border: 1px solid var(--border-subtle);
            border-radius: 28px;
            padding: 24px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 24px 60px rgba(0, 0, 0, 0.65), inset 0 1px 0 rgba(255, 255, 255, 0.08);
        }

        .store-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 14px;
            margin-bottom: 16px;
            border-bottom: 1px solid rgba(245, 194, 73, 0.16);
        }

        .store-header h2 {
            margin: 0;
            font-size: 1.35rem;
            font-weight: 800;
            color: var(--gold-bright);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .autosave-indicator {
            font-size: 0.78rem;
            color: var(--muted-cocoa);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .pulse-dot {
            width: 7px;
            height: 7px;
            border-radius: 50%;
            background: #4caf50;
            box-shadow: 0 0 8px #4caf50;
        }

        /* כרטיסיית שדרוג יוקרתית - תיקון תצוגת שורה עליונה ושורה תחתונה */
        .upgrade-item {
            background: var(--card-surface);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 18px;
            padding: 14px 16px;
            min-height: 82px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 14px;
            cursor: pointer;
            transition: all 0.2s cubic-bezier(0.22, 1, 0.36, 1);
            position: relative;
            overflow: visible;
        }

        .upgrade-item:hover:not(.locked) {
            background: var(--card-hover);
            border-color: var(--gold-primary);
            transform: translateY(-2px);
            box-shadow: 0 10px 24px rgba(0, 0, 0, 0.45), 0 0 15px rgba(245, 194, 73, 0.15);
        }

        .upgrade-item:active:not(.locked) {
            transform: scale(0.985);
        }

        .upgrade-item.locked {
            opacity: 0.48;
            cursor: not-allowed;
            filter: grayscale(35%);
        }

        .upgrade-left {
            display: flex;
            align-items: center;
            gap: 14px;
            flex: 1 1 auto;
            min-width: 0;
        }

        .upgrade-emblem {
            width: 54px;
            height: 54px;
            border-radius: 15px;
            background: linear-gradient(145deg, rgba(255, 255, 255, 0.1), rgba(0, 0, 0, 0.42));
            border: 1px solid rgba(245, 194, 73, 0.24);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.9rem;
            flex-shrink: 0;
            box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
        }

        .upgrade-meta {
            display: flex;
            flex-direction: column;
            justify-content: center;
            gap: 5px;
            flex: 1 1 auto;
            min-width: 0;
        }

        .upgrade-meta h3 {
            margin: 0;
            font-size: 1.05rem;
            line-height: 1.3;
            font-weight: 700;
            color: var(--cream-text);
            display: block;
            white-space: normal;
            overflow: visible;
        }

        .upgrade-meta p {
            margin: 0;
            font-size: 0.84rem;
            line-height: 1.35;
            color: var(--muted-cocoa);
            display: block;
            white-space: normal;
            overflow: visible;
        }

        .upgrade-right {
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            justify-content: center;
            gap: 6px;
            flex-shrink: 0;
        }

        .upgrade-cost {
            font-size: 1.02rem;
            font-weight: 800;
            color: var(--gold-bright);
            background: rgba(0, 0, 0, 0.35);
            padding: 4px 10px;
            border-radius: 10px;
            border: 1px solid rgba(245, 194, 73, 0.25);
        }

        .upgrade-item.locked .upgrade-cost {
            color: #ef9a9a;
            border-color: rgba(239, 154, 154, 0.2);
        }

        .upgrade-owned {
            font-size: 0.78rem;
            color: var(--muted-cocoa);
            font-weight: 600;
        }

        /* חלקיקים ומספרים מרחפים */
        .floating-gain {
            position: fixed;
            pointer-events: none;
            font-weight: 900;
            font-size: 1.55rem;
            color: var(--gold-bright);
            text-shadow: 0 3px 10px rgba(0, 0, 0, 0.9);
            z-index: 1500;
            animation: floatGain 0.9s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        @keyframes floatGain {
            0% { opacity: 1; transform: translateY(0) scale(0.8); }
            35% { transform: translateY(-30px) scale(1.2); }
            100% { opacity: 0; transform: translateY(-95px) scale(0.95); }
        }

        .crumb-drop {
            position: fixed;
            pointer-events: none;
            z-index: 1400;
            border-radius: 50%;
            animation: crumbPhysics 0.75s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
        }

        @keyframes crumbPhysics {
            0% { opacity: 1; transform: translate(0, 0) scale(1); }
            100% { opacity: 0; transform: translate(var(--dx), var(--dy)) scale(0.3); }
        }

        /* התראות הישגים ובונוסים (Toast) */
        #toast-rack {
            position: fixed;
            bottom: 22px;
            left: 22px;
            z-index: 2500;
            display: flex;
            flex-direction: column;
            gap: 10px;
            pointer-events: none;
            max-width: 360px;
            width: calc(100% - 44px);
        }

        .aaa-toast {
            background: linear-gradient(135deg, rgba(56, 32, 20, 0.96), rgba(24, 13, 8, 0.98));
            backdrop-filter: blur(12px);
            border: 1px solid var(--gold-primary);
            border-right: 5px solid var(--gold-primary);
            border-radius: 16px;
            padding: 14px 16px;
            box-shadow: 0 14px 36px rgba(0, 0, 0, 0.75);
            display: flex;
            align-items: center;
            gap: 12px;
            animation: slideToastIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }

        @keyframes slideToastIn {
            from { opacity: 0; transform: translateX(-30px) scale(0.95); }
            to { opacity: 1; transform: translateX(0) scale(1); }
        }

        .toast-icon {
            font-size: 1.7rem;
            flex-shrink: 0;
        }

        .toast-body {
            display: flex;
            flex-direction: column;
            gap: 2px;
        }

        .toast-title {
            font-size: 0.78rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--gold-primary);
            font-weight: 800;
        }

        .toast-msg {
            font-size: 0.92rem;
            color: var(--cream-text);
            font-weight: 600;
        }

        /* חלונית עריכת שם מאפייה */
        .modal-backdrop {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.75);
            backdrop-filter: blur(6px);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 3000;
            padding: 20px;
        }

        .modal-card {
            background: #2b180e;
            border: 1px solid var(--gold-primary);
            border-radius: 22px;
            padding: 24px;
            width: 100%;
            max-width: 380px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.85);
            text-align: center;
        }

        .modal-card h3 {
            margin: 0 0 14px 0;
            color: var(--gold-bright);
        }

        .modal-input {
            width: 100%;
            padding: 12px 14px;
            border-radius: 12px;
            border: 1px solid var(--border-gold);
            background: rgba(0, 0, 0, 0.45);
            color: #fff;
            font-family: inherit;
            font-size: 1rem;
            text-align: center;
            margin-bottom: 16px;
            outline: none;
        }

        .modal-actions {
            display: flex;
            gap: 10px;
            justify-content: center;
        }

        .btn-gold {
            background: linear-gradient(135deg, var(--gold-primary), var(--caramel));
            color: #1a0e07;
            border: none;
            padding: 10px 20px;
            border-radius: 12px;
            font-family: inherit;
            font-weight: 800;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <!-- סרגל עליון יוקרתי -->
    <header class="top-hud">
        <div class="bakery-identity">
            <div class="brand-emblem" aria-hidden="true">
                <svg width="26" height="26" viewBox="0 0 100 100">
                    <circle cx="50" cy="50" r="44" fill="#4a2810"/>
                    <circle cx="35" cy="35" r="7" fill="#1f0f05"/>
                    <circle cx="65" cy="40" r="8" fill="#1f0f05"/>
                    <circle cx="48" cy="68" r="7" fill="#1f0f05"/>
                </svg>
            </div>
            <div class="bakery-name-wrapper">
                <div class="bakery-name" onclick="openNameModal()" title="לחץ לשינוי שם המאפייה">
                    <span id="bakery-title-text">המאפייה המלכותית</span>
                    <span class="version-pill">1.5</span>
                    <span style="font-size: 0.85rem; opacity: 0.75;">✏️</span>
                </div>
                <span class="edit-hint">גרסה 1.5 • לחץ על השם להתאמה אישית</span>
            </div>
        </div>

        <!-- מד רמה ו-XP -->
        <div class="level-progress-area">
            <div class="level-header">
                <span class="level-badge">דרגה <span id="level-num">1</span></span>
                <span class="xp-text"><span id="xp-current">0</span> / <span id="xp-next">80</span> XP</span>
            </div>
            <div class="xp-bar-track">
                <div id="xp-bar-fill" class="xp-bar-fill"></div>
            </div>
        </div>

        <!-- כפתורי פעולה בסרגל -->
        <div class="hud-actions">
            <button class="hud-btn" onclick="toggleSound()" title="השתקה / הפעלת סאונד">
                <span id="sound-icon">🔊</span>
                <span>סאונד</span>
            </button>
            <button id="reset-btn" class="hud-btn" onclick="handleReset()" title="אפס את התקדמות המשחק">
                <span>🗑️</span>
                <span>איפוס</span>
            </button>
        </div>
    </header>

    <!-- במה מרכזית -->
    <main class="main-stage">
        <!-- תיבת המאפייה המרכזית -->
        <section id="bakery-chamber" class="bakery-chamber">
            <!-- עוגיית זהב אוטומטית (מופיעה אך ורק בתוך תיבת המאפייה) -->
            <button id="golden-cookie-entity" onclick="collectGoldenCookie(event)" title="עוגיית זהב נדירה! לחץ לתפיסה" aria-label="עוגיית זהב">
                <svg viewBox="0 0 100 100">
                    <defs>
                        <radialGradient id="goldCookieGrad" cx="35%" cy="30%" r="70%">
                            <stop offset="0%" stop-color="#fff9c4"/>
                            <stop offset="45%" stop-color="#ffd54f"/>
                            <stop offset="85%" stop-color="#ffa000"/>
                            <stop offset="100%" stop-color="#c67100"/>
                        </radialGradient>
                    </defs>
                    <circle cx="50" cy="50" r="44" fill="url(#goldCookieGrad)" stroke="#fff59d" stroke-width="2.5"/>
                    <circle cx="34" cy="34" r="6.5" fill="#7c4700"/>
                    <circle cx="64" cy="36" r="7.5" fill="#7c4700"/>
                    <circle cx="42" cy="63" r="6" fill="#7c4700"/>
                    <circle cx="66" cy="62" r="5.5" fill="#7c4700"/>
                </svg>
            </button>

            <!-- מונה עוגיות ונתונים -->
            <div class="counter-display">
                <p id="cookie-count" class="cookie-total">0</p>
                <div class="cookie-label">עוגיות נאפו</div>

                <div class="metrics-row">
                    <div class="metric-pill">
                        <span>⚡</span>
                        <span>קצב: <strong id="cps-display">0</strong> / שניה</span>
                    </div>
                    <div class="metric-pill">
                        <span>👆</span>
                        <span>ללחיצה: <strong id="click-display">1</strong></span>
                    </div>
                </div>

                <!-- סרגל טירוף זהב (Frenzy Bar) -->
                <div id="frenzy-hud" class="frenzy-hud">
                    <div class="frenzy-label">
                        <span>🔥 טירוף זהב פעיל (x2 ייצור!)</span>
                        <span id="frenzy-seconds">12.0s</span>
                    </div>
                    <div class="frenzy-track">
                        <div id="frenzy-fill" class="frenzy-fill"></div>
                    </div>
                </div>
            </div>

            <!-- העוגייה המרכזית (SVG מפוסל ומתאבן ברמת פרימיום) -->
            <div class="cookie-pedestal">
                <div class="light-rays"></div>
                <div class="ambient-aura"></div>
                <button id="hero-cookie-btn" onclick="pressMainCookie(event)" aria-label="אפה עוגייה">
                    <svg viewBox="0 0 260 260">
                        <defs>
                            <!-- הצללת בצק אפוי עשירה עם שוליים מקורמלים -->
                            <radialGradient id="cookieDoughGrad" cx="40%" cy="34%" r="66%">
                                <stop offset="0%" stop-color="#f8ca8e"/>
                                <stop offset="36%" stop-color="#df9147"/>
                                <stop offset="72%" stop-color="#b46322"/>
                                <stop offset="92%" stop-color="#8b4310"/>
                                <stop offset="100%" stop-color="#5e2907"/>
                            </radialGradient>

                            <!-- ברק אפייה חם בחלק העליון -->
                            <radialGradient id="cookieWarmSheen" cx="35%" cy="22%" r="58%">
                                <stop offset="0%" stop-color="rgba(255, 248, 224, 0.48)"/>
                                <stop offset="55%" stop-color="rgba(255, 214, 145, 0.14)"/>
                                <stop offset="100%" stop-color="rgba(255, 214, 145, 0)"/>
                            </radialGradient>

                            <!-- עומק פנימי אפוי -->
                            <radialGradient id="cookieInnerDepth" cx="55%" cy="62%" r="60%">
                                <stop offset="0%" stop-color="rgba(255, 232, 185, 0)"/>
                                <stop offset="78%" stop-color="rgba(92, 39, 9, 0.16)"/>
                                <stop offset="100%" stop-color="rgba(56, 20, 3, 0.44)"/>
                            </radialGradient>

                            <!-- פצפוצי שוקולד מריר מבריקים -->
                            <radialGradient id="darkChunkGrad" cx="32%" cy="28%" r="72%">
                                <stop offset="0%" stop-color="#6e3b23"/>
                                <stop offset="42%" stop-color="#3b1b0c"/>
                                <stop offset="85%" stop-color="#1e0c05"/>
                                <stop offset="100%" stop-color="#120602"/>
                            </radialGradient>

                            <!-- פצפוצי שוקולד חלב קרמלי -->
                            <radialGradient id="milkChunkGrad" cx="30%" cy="26%" r="72%">
                                <stop offset="0%" stop-color="#9a562d"/>
                                <stop offset="48%" stop-color="#5c2c12"/>
                                <stop offset="100%" stop-color="#2e1306"/>
                            </radialGradient>

                            <!-- צל רך מתחת לכל נתז שוקולד -->
                            <filter id="chunkShadow" x="-25%" y="-25%" width="150%" height="150%">
                                <feDropShadow dx="1.5" dy="2.5" stdDeviation="1.6" flood-color="#2c0f03" flood-opacity="0.65"/>
                            </filter>
                        </defs>

                        <!-- צל מגש עמוק ומדורג -->
                        <ellipse cx="130" cy="142" rx="112" ry="108" fill="rgba(0, 0, 0, 0.42)"/>
                        <ellipse cx="130" cy="136" rx="108" ry="105" fill="rgba(24, 10, 4, 0.35)"/>

                        <!-- שוליים מקורמלים ואורגניים של העוגייה -->
                        <path d="M130,14
                                 C146,14 159,21 173,24
                                 C188,28 201,39 212,51
                                 C223,63 227,78 233,93
                                 C239,108 242,123 239,139
                                 C236,155 231,170 222,184
                                 C213,198 202,211 188,220
                                 C174,229 158,236 142,238
                                 C126,240 110,239 94,234
                                 C78,229 63,221 50,210
                                 C37,199 28,185 22,169
                                 C16,153 15,136 17,119
                                 C19,102 22,85 30,70
                                 C38,55 50,43 64,33
                                 C78,23 93,19 109,16
                                 C116,15 123,14 130,14 Z"
                              fill="url(#cookieDoughGrad)" stroke="#7a380c" stroke-width="3.2"/>

                        <!-- שכבות תאורה ועומק על פני הבצק -->
                        <circle cx="130" cy="130" r="106" fill="url(#cookieInnerDepth)"/>
                        <circle cx="130" cy="130" r="104" fill="url(#cookieWarmSheen)"/>

                        <!-- חריצי אפייה עדינים וסדקים טבעיים בבצק -->
                        <g stroke="#7c3a0e" stroke-linecap="round" fill="none" opacity="0.55">
                            <path d="M74,66 Q84,74 92,70" stroke-width="1.6"/>
                            <path d="M166,62 Q158,74 165,84" stroke-width="1.5"/>
                            <path d="M188,128 Q176,133 172,143" stroke-width="1.6"/>
                            <path d="M132,192 Q122,182 111,188" stroke-width="1.6"/>
                            <path d="M62,134 Q72,126 68,115" stroke-width="1.5"/>
                            <path d="M98,44 Q108,52 118,48" stroke-width="1.4"/>
                        </g>

                        <!-- נקבוביות בצק ובועות אפייה זעירות -->
                        <g fill="#7a360b" opacity="0.45">
                            <circle cx="96" cy="58" r="2.2"/>
                            <circle cx="104" cy="53" r="1.4"/>
                            <circle cx="152" cy="54" r="2.4"/>
                            <circle cx="182" cy="88" r="2.1"/>
                            <circle cx="194" cy="116" r="2.5"/>
                            <circle cx="174" cy="178" r="2.3"/>
                            <circle cx="145" cy="198" r="2.0"/>
                            <circle cx="88" cy="186" r="2.4"/>
                            <circle cx="52" cy="162" r="2.2"/>
                            <circle cx="44" cy="102" r="2.1"/>
                            <circle cx="122" cy="88" r="1.8"/>
                            <circle cx="146" cy="116" r="1.9"/>
                            <circle cx="96" cy="136" r="2.0"/>
                        </g>

                        <!-- נתזי ופצפוצי שוקולד מריר וחלב מגוונים עם ברק ועומק תלת-ממדי -->
                        <g filter="url(#chunkShadow)">
                            <!-- נתח שוקולד מרכזי גדול ומפוסל -->
                            <path d="M114,112 C124,104 140,107 146,118 C151,128 145,141 133,144 C120,147 107,140 106,128 C105,121 108,116 114,112 Z"
                                  fill="url(#darkChunkGrad)"/>
                            <ellipse cx="122" cy="117" rx="6.5" ry="3.2" transform="rotate(-16 122 117)" fill="rgba(255,248,235,0.28)"/>

                            <!-- פצפוצי שוקולד מריר נוספים -->
                            <path d="M74,82 C83,75 96,78 100,88 C104,97 97,107 86,108 C76,109 68,101 69,91 C70,87 71,84 74,82 Z"
                                  fill="url(#darkChunkGrad)"/>
                            <ellipse cx="81" cy="85" rx="5" ry="2.4" transform="rotate(-20 81 85)" fill="rgba(255,248,235,0.25)"/>

                            <path d="M154,76 C163,70 175,74 178,84 C181,93 174,102 163,102 C153,102 146,94 148,85 C149,81 151,78 154,76 Z"
                                  fill="url(#darkChunkGrad)"/>
                            <ellipse cx="160" cy="80" rx="4.6" ry="2.2" transform="rotate(14 160 80)" fill="rgba(255,248,235,0.24)"/>

                            <path d="M156,146 C166,140 179,144 182,155 C185,165 177,175 166,175 C155,175 148,166 150,156 C151,152 153,148 156,146 Z"
                                  fill="url(#darkChunkGrad)"/>
                            <ellipse cx="163" cy="150" rx="5" ry="2.3" transform="rotate(18 163 150)" fill="rgba(255,248,235,0.24)"/>

                            <path d="M68,154 C77,148 89,152 92,162 C95,171 88,180 77,180 C67,180 61,172 62,163 C63,159 65,156 68,154 Z"
                                  fill="url(#darkChunkGrad)"/>
                            <ellipse cx="74" cy="158" rx="4.5" ry="2.1" transform="rotate(-15 74 158)" fill="rgba(255,248,235,0.22)"/>

                            <!-- פצפוצי שוקולד חלב להשלמת המראה העשיר -->
                            <ellipse cx="124" cy="54" rx="11" ry="8.5" transform="rotate(8 124 54)" fill="url(#milkChunkGrad)"/>
                            <ellipse cx="120" cy="51" rx="3.8" ry="1.8" transform="rotate(8 120 51)" fill="rgba(255,250,240,0.26)"/>

                            <ellipse cx="192" cy="126" rx="10.5" ry="8" transform="rotate(28 192 126)" fill="url(#milkChunkGrad)"/>
                            <ellipse cx="189" cy="123" rx="3.5" ry="1.6" transform="rotate(28 189 123)" fill="rgba(255,250,240,0.25)"/>

                            <ellipse cx="122" cy="176" rx="11.5" ry="8.5" transform="rotate(-10 122 176)" fill="url(#milkChunkGrad)"/>
                            <ellipse cx="118" cy="173" rx="3.8" ry="1.8" transform="rotate(-10 118 173)" fill="rgba(255,250,240,0.25)"/>

                            <ellipse cx="54" cy="118" rx="10" ry="7.8" transform="rotate(-24 54 118)" fill="url(#milkChunkGrad)"/>
                            <ellipse cx="51" cy="115" rx="3.4" ry="1.6" transform="rotate(-24 51 115)" fill="rgba(255,250,240,0.24)"/>
                        </g>
                    </svg>
                </button>
            </div>

            <!-- רצועת הישגים -->
            <div class="achievements-strip">
                <span class="ach-title">🏆 הישגים (<span id="ach-count">0</span>/<span id="ach-total">6</span>)</span>
                <div id="ach-icons" class="ach-icons"></div>
            </div>
        </section>

        <!-- חנות השדרוגים היוקרתית -->
        <section class="store-chamber">
            <div class="store-header">
                <h2>🏛️ קונדיטוריית השדרוגים</h2>
                <div class="autosave-indicator">
                    <span class="pulse-dot"></span>
                    <span>נשמר אוטומטית</span>
                </div>
            </div>
            <div id="store-list" class="store-list"></div>
        </section>
    </main>

    <!-- מיכל התראות Toast -->
    <div id="toast-rack"></div>

    <!-- חלונית שינוי שם מאפייה -->
    <div id="name-modal" class="modal-backdrop">
        <div class="modal-card">
            <h3>✨ שם המאפייה שלך</h3>
            <input id="bakery-name-input" class="modal-input" type="text" maxlength="26" placeholder="הכנס שם למאפייה...">
            <div class="modal-actions">
                <button class="btn-gold" onclick="saveBakeryName()">שמור שם</button>
                <button class="hud-btn" onclick="closeNameModal()">ביטול</button>
            </div>
        </div>
    </div>

    <script>
        // הגדרות מבנים ושדרוגים
        const UPGRADE_CATALOG = [
            { id: 'rolling_pin', name: 'מערוך עץ אלון', desc: '+1 עוגייה לכל לחיצה ידנית', icon: '🥖', baseCost: 15, type: 'click', power: 1 },
            { id: 'robo_finger', name: 'אצבע רובוטית', desc: '+1 עוגייה בכל שנייה', icon: '🦾', baseCost: 50, type: 'cps', power: 1 },
            { id: 'grandma', name: 'סבתא קונדיטורית', desc: '+6 עוגיות בכל שנייה', icon: '👵', baseCost: 260, type: 'cps', power: 6 },
            { id: 'boutique', name: 'מאפיית בוטיק', desc: '+28 עוגיות בכל שנייה', icon: '🥐', baseCost: 1200, type: 'cps', power: 28 },
            { id: 'factory', name: 'מפעל שוקולד', desc: '+130 עוגיות בכל שנייה', icon: '🏭', baseCost: 6500, type: 'cps', power: 130 },
            { id: 'sugar_mine', name: 'מכרה סוכר זהוב', desc: '+600 עוגיות בכל שנייה', icon: '⛏️', baseCost: 32000, type: 'cps', power: 600 },
            { id: 'alchemy_lab', name: 'מעבדת אלכימיה', desc: '+2,800 עוגיות בכל שנייה', icon: '⚗️', baseCost: 150000, type: 'cps', power: 2800 },
            { id: 'portal', name: 'פורטל בין-ממדי', desc: '+14,000 עוגיות בכל שנייה', icon: '🌀', baseCost: 750000, type: 'cps', power: 14000 }
        ];

        // הגדרות הישגים
        const ACHIEVEMENTS_LIST = [
            { id: 'first_bake', title: 'העוגייה הראשונה', desc: 'אפית את העוגייה הראשונה שלך!', icon: '🍪', check: s => s.totalBaked >= 1 },
            { id: 'hundred_club', title: 'אופה מתחיל', desc: 'צברת 100 עוגיות במצטבר', icon: '🥉', check: s => s.totalBaked >= 100 },
            { id: 'thousand_club', title: 'אומן הבצק', desc: 'צברת 1,000 עוגיות במצטבר', icon: '🥈', check: s => s.totalBaked >= 1000 },
            { id: 'first_building', title: 'יזם קולינרי', desc: 'רכשת 5 שדרוגים בחנות', icon: '🏪', check: s => getTotalOwned() >= 5 },
            { id: 'golden_hunter', title: 'צייד הזהב', desc: 'תפסת עוגיית זהב נדירה!', icon: '✨', check: s => s.goldenCaught >= 1 },
            { id: 'tycoon', title: 'טייקון העוגיות', desc: 'צברת 50,000 עוגיות במצטבר', icon: '👑', check: s => s.totalBaked >= 50000 }
        ];

        // מצב המשחק
        let state = {
            bakeryName: 'המאפייה המלכותית',
            cookies: 0,
            totalBaked: 0,
            clickPower: 1,
            goldenCaught: 0,
            owned: {},
            unlockedAchievements: []
        };

        // אתחול כמויות
        UPGRADE_CATALOG.forEach(u => state.owned[u.id] = 0);

        let soundOn = true;
        let audioCtx = null;
        let frenzyMultiplier = 1;
        let frenzyEndTime = 0;
        const FRENZY_DURATION_MS = 12000;
        let resetConfirmTimer = null;

        // מנוע סאונד פרימיום (Web Audio API)
        function playAudio(kind) {
            if (!soundOn) return;
            try {
                if (!audioCtx) {
                    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
                }
                if (audioCtx.state === 'suspended') audioCtx.resume();

                const now = audioCtx.currentTime;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.connect(gain);
                gain.connect(audioCtx.destination);

                if (kind === 'click') {
                    osc.type = 'triangle';
                    osc.frequency.setValueAtTime(340 + Math.random() * 80, now);
                    osc.frequency.exponentialRampToValueAtTime(120, now + 0.07);
                    gain.gain.setValueAtTime(0.16, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.07);
                    osc.start(now);
                    osc.stop(now + 0.07);
                } else if (kind === 'buy') {
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(523.25, now);
                    osc.frequency.setValueAtTime(659.25, now + 0.06);
                    osc.frequency.setValueAtTime(783.99, now + 0.12);
                    gain.gain.setValueAtTime(0.14, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.26);
                    osc.start(now);
                    osc.stop(now + 0.26);
                } else if (kind === 'golden') {
                    osc.type = 'sine';
                    [587.33, 739.99, 880, 1174.66, 1479.98].forEach((f, i) => {
                        osc.frequency.setValueAtTime(f, now + i * 0.07);
                    });
                    gain.gain.setValueAtTime(0.2, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.48);
                    osc.start(now);
                    osc.stop(now + 0.48);
                } else if (kind === 'achievement') {
                    osc.type = 'triangle';
                    [440, 554.37, 659.25, 880].forEach((f, i) => {
                        osc.frequency.setValueAtTime(f, now + i * 0.09);
                    });
                    gain.gain.setValueAtTime(0.18, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.5);
                    osc.start(now);
                    osc.stop(now + 0.5);
                }
            } catch (e) {}
        }

        function toggleSound() {
            soundOn = !soundOn;
            document.getElementById('sound-icon').innerText = soundOn ? '🔊' : '🔇';
            showToast('מערכת שמע', soundOn ? 'האפקטים הקוליים הופעלו' : 'האפקטים הקוליים הושתקו', soundOn ? '🔊' : '🔇');
        }

        // חישובים
        function getUpgradeCost(upg) {
            const count = state.owned[upg.id] || 0;
            return Math.floor(upg.baseCost * Math.pow(1.18, count));
        }

        function getBaseCPS() {
            return UPGRADE_CATALOG
                .filter(u => u.type === 'cps')
                .reduce((sum, u) => sum + (state.owned[u.id] || 0) * u.power, 0);
        }

        function getEffectiveCPS() {
            return getBaseCPS() * frenzyMultiplier;
        }

        function getEffectiveClick() {
            return state.clickPower * frenzyMultiplier;
        }

        function getTotalOwned() {
            return Object.values(state.owned).reduce((a, b) => a + b, 0);
        }

        function formatNum(n) {
            return Math.floor(n).toLocaleString('he-IL');
        }

        // לחיצה על העוגייה הראשית
        function pressMainCookie(e) {
            const gained = getEffectiveClick();
            state.cookies += gained;
            state.totalBaked += gained;
            playAudio('click');

            const rect = document.getElementById('hero-cookie-btn').getBoundingClientRect();
            const cx = e.clientX || (rect.left + rect.width / 2);
            const cy = e.clientY || (rect.top + rect.height / 2);

            spawnFloatingGain(cx, cy, `+${formatNum(gained)}`);
            spawnCrumbs(cx, cy, 7);
            checkAchievements();
            updateUI();
        }

        function spawnFloatingGain(x, y, text) {
            const el = document.createElement('div');
            el.className = 'floating-gain';
            el.innerText = text;
            el.style.left = `${x + (Math.random() - 0.5) * 40}px`;
            el.style.top = `${y - 24}px`;
            document.body.appendChild(el);
            setTimeout(() => el.remove(), 900);
        }

        function spawnCrumbs(x, y, count) {
            const colors = ['#d2833c', '#9e531b', '#3a1a0c', '#f5c249'];
            for (let i = 0; i < count; i++) {
                const crumb = document.createElement('div');
                crumb.className = 'crumb-drop';
                const size = 5 + Math.random() * 6;
                crumb.style.width = `${size}px`;
                crumb.style.height = `${size}px`;
                crumb.style.background = colors[Math.floor(Math.random() * colors.length)];

                const angle = Math.random() * Math.PI * 2;
                const dist = 45 + Math.random() * 85;
                crumb.style.left = `${x}px`;
                crumb.style.top = `${y}px`;
                crumb.style.setProperty('--dx', `${Math.cos(angle) * dist}px`);
                crumb.style.setProperty('--dy', `${Math.sin(angle) * dist + 35}px`);

                document.body.appendChild(crumb);
                setTimeout(() => crumb.remove(), 750);
            }
        }

        // רכישת שדרוג בחנות
        function purchaseUpgrade(id) {
            const upg = UPGRADE_CATALOG.find(u => u.id === id);
            if (!upg) return;
            const cost = getUpgradeCost(upg);

            if (state.cookies >= cost) {
                state.cookies -= cost;
                state.owned[id] = (state.owned[id] || 0) + 1;
                if (upg.type === 'click') {
                    state.clickPower += upg.power;
                }
                playAudio('buy');
                checkAchievements();
                updateUI();
                saveState();
            }
        }

        // עוגיית זהב אוטומטית לחלוטין (בתוך תיבת המאפייה בלבד)
        function scheduleNextGoldenCookie() {
            // מופיעה אוטומטית כל 22 עד 38 שניות
            const delay = 22000 + Math.random() * 16000;
            setTimeout(() => {
                appearGoldenCookie();
                scheduleNextGoldenCookie();
            }, delay);
        }

        function appearGoldenCookie() {
            const chamber = document.getElementById('bakery-chamber');
            const golden = document.getElementById('golden-cookie-entity');
            if (!chamber || !golden) return;

            const w = chamber.clientWidth;
            const h = chamber.clientHeight;
            const size = 84;
            const pad = 18;

            const minX = pad;
            const maxX = Math.max(pad, w - size - pad);
            const minY = 145; // מתחת לתיבת המונה
            const maxY = Math.max(minY + 20, h - size - 65);

            golden.style.left = `${minX + Math.random() * (maxX - minX)}px`;
            golden.style.top = `${minY + Math.random() * (maxY - minY)}px`;
            golden.style.display = 'flex';

            clearTimeout(golden.despawnTimer);
            golden.despawnTimer = setTimeout(() => {
                golden.style.display = 'none';
            }, 8000);
        }

        function collectGoldenCookie(e) {
            e.stopPropagation();
            const golden = document.getElementById('golden-cookie-entity');
            const rect = golden.getBoundingClientRect();
            golden.style.display = 'none';
            clearTimeout(golden.despawnTimer);

            state.goldenCaught += 1;
            playAudio('golden');
            spawnCrumbs(rect.left + rect.width / 2, rect.top + rect.height / 2, 16);

            const instantBonus = Math.max(100, Math.floor(state.cookies * 0.25) + getBaseCPS() * 15);
            state.cookies += instantBonus;
            state.totalBaked += instantBonus;

            // הפעלת טירוף זהב ל-12 שניות
            frenzyMultiplier = 2;
            frenzyEndTime = Date.now() + FRENZY_DURATION_MS;
            document.getElementById('frenzy-hud').style.display = 'block';
            document.getElementById('bakery-chamber').classList.add('frenzy-mode');

            showToast('עוגיית זהב נדירה!', `+${formatNum(instantBonus)} עוגיות + ייצור כפול (x2) ל-12 שניות!`, '✨');
            checkAchievements();
            updateUI();
            saveState();
        }

        // מערכת הישגים
        function checkAchievements() {
            let newlyUnlocked = false;
            ACHIEVEMENTS_LIST.forEach(ach => {
                if (!state.unlockedAchievements.includes(ach.id) && ach.check(state)) {
                    state.unlockedAchievements.push(ach.id);
                    newlyUnlocked = true;
                    playAudio('achievement');
                    showToast('הישג חדש נפתח!', `${ach.title} — ${ach.desc}`, ach.icon);
                }
            });
            if (newlyUnlocked) renderAchievementsStrip();
        }

        function renderAchievementsStrip() {
            const container = document.getElementById('ach-icons');
            container.innerHTML = '';
            document.getElementById('ach-count').innerText = state.unlockedAchievements.length;
            document.getElementById('ach-total').innerText = ACHIEVEMENTS_LIST.length;

            ACHIEVEMENTS_LIST.forEach(ach => {
                const isUnlocked = state.unlockedAchievements.includes(ach.id);
                const pip = document.createElement('div');
                pip.className = `ach-pip ${isUnlocked ? 'unlocked' : ''}`;
                pip.innerText = ach.icon;
                pip.title = isUnlocked ? `${ach.title}: ${ach.desc}` : 'הישג נעול — המשך לאפות!';
                container.appendChild(pip);
            });
        }

        // התראות Toast מעוצבות
        function showToast(title, msg, icon = '🍪') {
            const rack = document.getElementById('toast-rack');
            const toast = document.createElement('div');
            toast.className = 'aaa-toast';
            toast.innerHTML = `
                <div class="toast-icon">${icon}</div>
                <div class="toast-body">
                    <div class="toast-title">${title}</div>
                    <div class="toast-msg">${msg}</div>
                </div>
            `;
            rack.appendChild(toast);

            setTimeout(() => {
                toast.style.opacity = '0';
                toast.style.transform = 'translateX(-20px)';
                toast.style.transition = 'all 0.3s ease';
                setTimeout(() => toast.remove(), 300);
            }, 3800);
        }

        // בניית חנות השדרוגים
        function buildStore() {
            const list = document.getElementById('store-list');
            list.innerHTML = '';

            UPGRADE_CATALOG.forEach(upg => {
                const item = document.createElement('div');
                item.id = `store-item-${upg.id}`;
                item.className = 'upgrade-item locked';
                item.onclick = () => purchaseUpgrade(upg.id);

                item.innerHTML = `
                    <div class="upgrade-left">
                        <div class="upgrade-emblem">${upg.icon}</div>
                        <div class="upgrade-meta">
                            <h3>${upg.name}</h3>
                            <p>${upg.desc}</p>
                        </div>
                    </div>
                    <div class="upgrade-right">
                        <span class="upgrade-cost" id="cost-${upg.id}">${formatNum(getUpgradeCost(upg))} 🍪</span>
                        <span class="upgrade-owned" id="owned-${upg.id}">בבעלותך: ${state.owned[upg.id] || 0}</span>
                    </div>
                `;
                list.appendChild(item);
            });
        }

        // עדכון UI ודרגת המאפייה
        function updateUI() {
            const setText = (id, value) => {
                const el = document.getElementById(id);
                if (el) el.innerText = value;
            };

            setText('bakery-title-text', state.bakeryName);
            setText('cookie-count', formatNum(state.cookies));
            setText('cps-display', formatNum(getEffectiveCPS()));
            setText('click-display', formatNum(getEffectiveClick()));

            // חישוב רמה ו-XP מתוך סך העוגיות שנאפו
            const xp = Math.floor(state.totalBaked);
            const level = Math.floor(Math.sqrt(xp / 80)) + 1;
            const prevLevelXP = Math.pow(level - 1, 2) * 80;
            const nextLevelXP = Math.pow(level, 2) * 80;
            const progressPct = Math.min(100, Math.max(0, ((xp - prevLevelXP) / (nextLevelXP - prevLevelXP)) * 100));

            setText('level-num', level);
            setText('xp-current', formatNum(xp - prevLevelXP));
            setText('xp-next', formatNum(nextLevelXP - prevLevelXP));
            const xpBarFill = document.getElementById('xp-bar-fill');
            if (xpBarFill) xpBarFill.style.width = `${progressPct}%`;

            // עדכון פריטי החנות
            UPGRADE_CATALOG.forEach(upg => {
                const cost = getUpgradeCost(upg);
                const el = document.getElementById(`store-item-${upg.id}`);
                const costEl = document.getElementById(`cost-${upg.id}`);
                const ownedEl = document.getElementById(`owned-${upg.id}`);

                if (el && costEl && ownedEl) {
                    el.classList.toggle('locked', state.cookies < cost);
                    costEl.innerText = `${formatNum(cost)} 🍪`;
                    ownedEl.innerText = `בבעלותך: ${state.owned[upg.id] || 0}`;
                }
            });
        }

        // עריכת שם המאפייה
        function openNameModal() {
            const modal = document.getElementById('name-modal');
            const input = document.getElementById('bakery-name-input');
            input.value = state.bakeryName;
            modal.style.display = 'flex';
            input.focus();
        }

        function closeNameModal() {
            document.getElementById('name-modal').style.display = 'none';
        }

        function saveBakeryName() {
            const val = document.getElementById('bakery-name-input').value.trim();
            if (val) {
                state.bakeryName = val;
                updateUI();
                saveState();
                showToast('שם המאפייה עודכן', `ברוכים הבאים אל "${val}"!`, '🏛️');
            }
            closeNameModal();
        }

        // שמירה וטעינה
        function saveState() {
            try {
                localStorage.setItem('cookieEmpireAAA_v1_5', JSON.stringify(state));
            } catch (e) {}
        }

        function loadState() {
            try {
                const raw = localStorage.getItem('cookieEmpireAAA_v1_5')
                    || localStorage.getItem('cookieEmpireAAA_v1_4')
                    || localStorage.getItem('cookieEmpireAAA_v1');
                if (raw) {
                    const parsed = JSON.parse(raw);
                    state = { ...state, ...parsed };
                }
            } catch (e) {}
        }

        // איפוס דו-שלבי דיסקרטי
        function handleReset() {
            const btn = document.getElementById('reset-btn');
            if (!btn.classList.contains('danger-confirm')) {
                btn.classList.add('danger-confirm');
                btn.innerHTML = '<span>⚠️</span><span>אשר איפוס</span>';
                resetConfirmTimer = setTimeout(() => {
                    btn.classList.remove('danger-confirm');
                    btn.innerHTML = '<span>🗑️</span><span>איפוס</span>';
                }, 3500);
            } else {
                clearTimeout(resetConfirmTimer);
                localStorage.removeItem('cookieEmpireAAA_v1_5');
                localStorage.removeItem('cookieEmpireAAA_v1_4');
                localStorage.removeItem('cookieEmpireAAA_v1');
                state = {
                    bakeryName: 'המאפייה המלכותית',
                    cookies: 0,
                    totalBaked: 0,
                    clickPower: 1,
                    goldenCaught: 0,
                    owned: {},
                    unlockedAchievements: []
                };
                UPGRADE_CATALOG.forEach(u => state.owned[u.id] = 0);
                frenzyMultiplier = 1;
                frenzyEndTime = 0;
                document.getElementById('frenzy-hud').style.display = 'none';
                document.getElementById('bakery-chamber').classList.remove('frenzy-mode');
                btn.classList.remove('danger-confirm');
                btn.innerHTML = '<span>🗑️</span><span>איפוס</span>';
                buildStore();
                renderAchievementsStrip();
                updateUI();
                showToast('איפוס הושלם', 'המאפייה אופסה להתחלה חדשה.', '🔄');
            }
        }

        // לולאת משחק ראשית (10 פריימים לשנייה לחישובים חלקים)
        setInterval(() => {
            const cps = getEffectiveCPS();
            if (cps > 0) {
                const tickGain = cps / 10;
                state.cookies += tickGain;
                state.totalBaked += tickGain;
                checkAchievements();
            }

            // ניהול טיימר טירוף זהב
            if (frenzyMultiplier > 1) {
                const remaining = frenzyEndTime - Date.now();
                if (remaining <= 0) {
                    frenzyMultiplier = 1;
                    document.getElementById('frenzy-hud').style.display = 'none';
                    document.getElementById('bakery-chamber').classList.remove('frenzy-mode');
                } else {
                    const pct = (remaining / FRENZY_DURATION_MS) * 100;
                    document.getElementById('frenzy-fill').style.width = `${pct}%`;
                    document.getElementById('frenzy-seconds').innerText = `${(remaining / 1000).toFixed(1)}s`;
                }
            }

            updateUI();
        }, 100);

        // שמירה אוטומטית כל 5 שניות
        setInterval(saveState, 5000);

        // הפעלה בטעינת החלון
        window.onload = function () {
            loadState();
            buildStore();
            renderAchievementsStrip();
            updateUI();
            scheduleNextGoldenCookie();
            showToast('גרסה 1.5 עלתה', 'העוגייה המרכזית שודרגה למראה שוקולד-קרמל מפוסל.', '🍪');
        };
    </script>
</body>
</html>
