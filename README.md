    :root {
        --light-blue: #e6f7ff;
        --sky-blue: #b3e0ff;
        --soft-blue: #87ceeb;
        --medium-blue: #5dade2;
        --accent-blue: #3498db;
        --deep-blue: #2980b9;
        --text-dark: #2c3e50;
        --text-medium: #566573;
        --text-light: #f8f9fa;
        --card-bg: rgba(255, 255, 255, 0.9);
        --shadow: rgba(52, 152, 219, 0.2);
    }
    
    body {
        background: linear-gradient(135deg, var(--light-blue), var(--sky-blue));
        color: var(--text-dark);
        min-height: 100vh;
        line-height: 1.6;
    }
    
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
    }
    
    header {
        text-align: center;
        padding: 60px 0 40px;
        position: relative;
    }
    
    .logo {
        font-size: 1.2rem;
        color: var(--deep-blue);
        letter-spacing: 3px;
        margin-bottom: 10px;
        text-transform: uppercase;
    }
    
    h1 {
        font-size: 3.2rem;
        font-weight: 700;
        margin-bottom: 15px;
        background: linear-gradient(135deg, var(--deep-blue), var(--accent-blue));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        text-shadow: 0 2px 10px rgba(52, 152, 219, 0.2);
    }
    
    .subtitle {
        font-size: 1.3rem;
        color: var(--text-medium);
        max-width: 600px;
        margin: 0 auto 30px;
        line-height: 1.8;
    }
    
    .divider {
        width: 100px;
        height: 3px;
        background: linear-gradient(90deg, transparent, var(--accent-blue), transparent);
        margin: 30px auto;
    }
    
    .upload-section {
        background: var(--card-bg);
        border-radius: 16px;
        padding: 40px;
        margin-bottom: 50px;
        box-shadow: 0 10px 30px var(--shadow);
        border: 1px solid rgba(52, 152, 219, 0.2);
        backdrop-filter: blur(10px);
    }
    
    .section-title {
        text-align: center;
        font-size: 1.8rem;
        margin-bottom: 30px;
        color: var(--deep-blue);
        position: relative;
        display: inline-block;
        left: 50%;
        transform: translateX(-50%);
    }
    
    .section-title:after {
        content: '';
        position: absolute;
        bottom: -10px;
        left: 0;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, transparent, var(--accent-blue), transparent);
    }
    
    .upload-area {
        border: 2px dashed rgba(52, 152, 219, 0.5);
        border-radius: 12px;
        padding: 50px 20px;
        text-align: center;
        margin-bottom: 30px;
        transition: all 0.4s;
        cursor: pointer;
        background: rgba(255, 255, 255, 0.7);
    }
    
    .upload-area:hover {
        border-color: var(--accent-blue);
        background: rgba(255, 255, 255, 0.9);
        transform: translateY(-5px);
    }
    
    .upload-area i {
        font-size: 3.5rem;
        color: var(--accent-blue);
        margin-bottom: 20px;
        opacity: 0.8;
    }
    
    .upload-area p {
        color: var(--text-medium);
        font-size: 1.1rem;
    }
    
    .text-input {
        width: 100%;
        min-height: 150px;
        padding: 20px;
        border: 1px solid rgba(52, 152, 219, 0.3);
        border-radius: 10px;
        font-size: 1rem;
        resize: vertical;
        margin-bottom: 25px;
        background: rgba(255, 255, 255, 0.8);
        color: var(--text-dark);
        transition: all 0.3s;
    }
    
    .text-input:focus {
        outline: none;
        border-color: var(--accent-blue);
        box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.2);
    }
    
    .text-input::placeholder {
        color: var(--text-medium);
    }
    
    .submit-btn {
        background: linear-gradient(135deg, var(--accent-blue), var(--deep-blue));
        color: white;
        border: none;
        padding: 14px 40px;
        border-radius: 50px;
        font-size: 1.1rem;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.3s;
        display: block;
        margin: 0 auto;
        box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
        letter-spacing: 1px;
    }
    
    .submit-btn:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 20px rgba(52, 152, 219, 0.6);
    }
    
    .memories-section {
        margin-top: 30px;
    }
    
    .memories-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
        gap: 30px;
    }
    
    .memory-card {
        background: var(--card-bg);
        border-radius: 16px;
        overflow: hidden;
        box-shadow: 0 8px 25px var(--shadow);
        transition: all 0.4s;
        position: relative;
        border: 1px solid rgba(52, 152, 219, 0.2);
    }
    
    .memory-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 30px rgba(52, 152, 219, 0.3);
    }
    
    .memory-img {
        width: 100%;
        height: 220px;
        object-fit: cover;
        transition: transform 0.5s;
    }
    
    .memory-card:hover .memory-img {
        transform: scale(1.05);
    }
    
    .memory-content {
        padding: 25px;
    }
    
    .memory-text {
        margin-bottom: 20px;
        line-height: 1.7;
        color: var(--text-dark);
    }
    
    .memory-date {
        color: var(--accent-blue);
        font-size: 0.9rem;
        text-align: right;
        font-style: italic;
    }
    
    .memory-actions {
        position: absolute;
        top: 15px;
        right: 15px;
        display: flex;
        gap: 10px;
        opacity: 0;
        transition: opacity 0.3s;
    }
    
    .memory-card:hover .memory-actions {
        opacity: 1;
    }
    
    .memory-actions button {
        background: rgba(255, 255, 255, 0.9);
        border: none;
        border-radius: 50%;
        width: 40px;
        height: 40px;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: all 0.3s;
        backdrop-filter: blur(5px);
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
    
    .memory-actions button:hover {
        background: white;
        transform: scale(1.1);
    }
    
    .edit-btn {
        color: var(--accent-blue);
    }
    
    .delete-btn {
        color: #e74c3c;
    }
    
    .empty-state {
        text-align: center;
        padding: 60px 40px;
        color: var(--text-medium);
        grid-column: 1 / -1;
    }
    
    .empty-state i {
        font-size: 5rem;
        margin-bottom: 25px;
        color: rgba(52, 152, 219, 0.3);
    }
    
    .empty-state p {
        font-size: 1.2rem;
        max-width: 500px;
        margin: 0 auto;
        line-height: 1.8;
    }
    
    footer {
        text-align: center;
        margin-top: 80px;
        padding: 30px 0;
        color: var(--text-medium);
        font-size: 0.9rem;
        border-top: 1px solid rgba(52, 152, 219, 0.2);
    }
    
    .quote {
        font-style: italic;
        margin-top: 15px;
        color: var(--deep-blue);
        opacity: 0.8;
    }
    
    /* 模态框样式 */
    .modal {
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(230, 247, 255, 0.9);
        z-index: 1000;
        align-items: center;
        justify-content: center;
        backdrop-filter: blur(5px);
    }
    
    .modal-content {
        background: var(--card-bg);
        border-radius: 16px;
        padding: 40px;
        width: 90%;
        max-width: 650px;
        box-shadow: 0 20px 40px var(--shadow);
        border: 1px solid rgba(52, 152, 219, 0.3);
    }
    
    .modal-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 25px;
    }
    
    .modal-title {
        font-size: 1.6rem;
        color: var(--deep-blue);
    }
    
    .close-btn {
        background: none;
        border: none;
        font-size: 1.8rem;
        cursor: pointer;
        color: var(--text-medium);
        transition: color 0.3s;
    }
    
    .close-btn:hover {
        color: var(--accent-blue);
    }
    
    .modal-actions {
        display: flex;
        justify-content: flex-end;
        gap: 15px;
        margin-top: 25px;
    }
    
    .cancel-btn {
        background: rgba(179, 224, 255, 0.5);
        color: var(--text-dark);
        border: none;
        padding: 12px 25px;
        border-radius: 50px;
        cursor: pointer;
        transition: all 0.3s;
    }
    
    .cancel-btn:hover {
        background: rgba(179, 224, 255, 0.8);
    }
    
    .save-btn {
        background: linear-gradient(135deg, var(--accent-blue), var(--deep-blue));
        color: white;
        border: none;
        padding: 12px 25px;
        border-radius: 50px;
        cursor: pointer;
        font-weight: 600;
        transition: all 0.3s;
    }
    
    .save-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
    }
    
    @media (max-width: 768px) {
        h1 {
            font-size: 2.5rem;
        }
        
        .upload-section {
            padding: 25px;
        }
        
        .memories-grid {
            grid-template-columns: 1fr;
        }
        
        .modal-content {
            padding: 30px 20px;
        }
    }
    
    /* 动画效果 */
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    
    .memory-card {
        animation: fadeIn 0.5s ease-out;
    }
    
    /* 滚动条样式 */
    ::-webkit-scrollbar {
        width: 8px;
    }
    
    ::-webkit-scrollbar-track {
        background: var(--light-blue);
    }
    
    ::-webkit-scrollbar-thumb {
        background: var(--accent-blue);
        border-radius: 4px;
    }
    
    ::-webkit-scrollbar-thumb:hover {
        background: var(--deep-blue);
    }
</style>
