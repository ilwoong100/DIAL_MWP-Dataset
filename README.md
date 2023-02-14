# DIAL_MWP-Dataset
Korean math word problem dataset for AGC-3

## 목표
본 연구에서는 한글로 이루어진 수학 서술형 문제(MWP)를 푸는 심층신경망 모델 개발을 위한 한국어 MWP 데이터셋 입니다.

## 데이터 구성
데이터는 json 형식의 dictionary로 이루어져 있습니다.
한국어 수학 서술형 문제와 해당 문제에 대한 본 연구진이 제안한 equation으로 이루어져 있습니다.
데이터 예시
--------
```
    "1": {
        "question": "윤기, 정국, 유나, 유정 4명의 학생은 각각 7, 6, 9, 8번을 가지고있다. 2번째로 작은 숫자는 누구입니까?",
        "equation_op": "[OP_LIST_SOL] 윤기 정국 유나 유정 [OP_LIST_EOL] [OP_LIST_SOL] 7 6 9 8 [OP_LIST_EOL] 2 [OP_LIST_MIN] [OP_LIST_INDEX] [OP_LIST_POP] [OP_LIST_GET]",
        "answer": "",
        "qtype": "6"
    },
    "2": {
        "question": "1부터 9까지의 숫자는 한 번만 사용하여 9자리 숫자를 형성합니다. 그 숫자가 55로 나누어 떨어지면 가장 작은 9자리 숫자를 찾으십시오.",
        "equation_op": "1 9 1 [OP_LIST_ARANGE] 9 [OP_LIST_GET_PERM] 55 [OP_LIST_DIVISIBLE] 1 [OP_LIST_MIN]",
        "answer": "",
        "qtype": "5"
    },
    "3": {
        "question": "가로 10 센티미터(cm), 세로 8 센티미터(cm), 높이 5 센티미터(cm)의 직육면체 모서리 길이의 합계는 몇 센티미터(cm)입니까?",
        "equation_op": "10 4 [OP_MUL] 8 4 [OP_MUL] [OP_ADD] 5 4 [OP_MUL] [OP_ADD]",
        "answer": "",
        "qtype": ""
    }
```
