<p align=center>
<img src="https://github.com/user-attachments/assets/6f2dd264-8498-43c9-bf1f-ef2254fd9790">
</p>

실행 파일
app.py - Streamlit 체스판 분석기 - 이미지를 업로드하면 CNN을 인식해 Stockfish가 다음 수를 추천
ai_chess.py - AI vs AI 자동 대국 GUI (tkinter)
ai_human_chess.py - 사람 vs AI 대국 GUI (tkinter)
train.py - CNN 기물 인식 모델 학습
chess_dataset.py - PGN 데이터 수집 스크립트 (AI 자동 대국 기보 저장)


core/패키지 (공통 파일, 실행 X)
core/engine.py - Stockfish 엔진 로딩, OS별 경로 자동 감지
core/board.py - PIECE_SYMBOLS · PIECE_VALUES · 좌표 변환 유틸리티
core/fen.py - FEN 생성, 턴/캐슬링/앙파상 복원 및 유효성 검사
core/model.py - ChessPieceCNN 정의, 모델 로딩, 추론
core/interface.py - 하드웨어↔소프트웨어 JSON 메시지 규격 (GameState · MoveCommand · RobotResult · SafetyEvent)
core/session.py - Game Session Turn FSM — auto / human_vs_robot / approval 3가지 모드 관리
core/__init__.py - 패키지 공개 API 정리


기타 파일
chess_model_pure.pth - 학습된 CNN 가중치 파일
stockfish-windows-x86-64.exe - Stockfish 체스 엔진 실행 파일
images/ - 기물 이미지 12개 (tkinter GUI용)
ai_games.pgn - AI 자동 대국으로 수집된 기보 데이터
core/__pycache__/ - Python 컴파일 캐시 (자동 생성)
