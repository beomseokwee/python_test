# python_Lecture


p = ' \t abc   \t  '
print(p)
print(p.strip())

#replace

u = 'spam and han'
print(u.replace('spam','spam,egg'))
t = u.replace('spam','spam,egg')
print(t)

# 영구적으로 바꿀려면 다른 변수에 넣어서 프린트

u= 'spam and ham'
print(u.split())

#join
u1 = u.split()
t2 = ':'.join(u1)
print(t2)   # split()으로 인해 리스트단위로 :이 조인이 된다
print(':'.join(u)) # 조인을 쓸때는 .앞에 조인 시킬 문자 같은것들 적고 함수 사용

# splitiness
u3 = u"스팸 햄 계란 치즈"
t2 = u3.split()
print(t2)
print(t2[0],t2[1],t2[2],t2[3])

# splitlines() > line 기준으로 분리하여 리스트 반환
lines = '''first line
second line
third line'''
print(type(lines))
lines2 = lines.splitlines()
print(lines2)

# 정렬 center(),ljust(),rjust() << (첫번째인자 자리 확보 후 센터 왼,오 출력)(두번째에서 공백 말고 다른걸로 채우기 가능)
print(u)
c = u.center(60)
print(type(c))
print(c)
print(u.ljust(60))
print(u.rjust(60))

print(u.rjust(60,':'))

#is() << 문자열 내 정보 판단
print('abc'.isalpha())

#zfill() <자리 확보 후 남은 자리 0으로 채움
a = 'abc'
print(a.zfill(5))

# 문자열 포멧팅
name = '홍길동'
letter = '''
안녕하세요 %s님,
오늘 밤 파티에 참석해 주실 수 있나요?
'''
names = ['위범석', '권다예', '윈터']
for name in names:
    print(letter % name)
    print('-' * 40)

# str(),repr() = 모두 문자열을 반환해주는 함수

# dictionary를 활용한 포멧팅 << 딕셔너리기 때문에 순서는 상관이 없다.
print(('%(이름)s -- %(전화번호)s')%{'이름':'홍길동','전화번호':5284})
print(('%(이름)s -- %(전화번호)s')%{'전화번호':5284,'이름':'홍길동'})

