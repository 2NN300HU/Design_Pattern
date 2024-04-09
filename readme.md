# 디자인패턴
## 필요성
> 디자인 패턴 그거 굳이 공부 안해도 코드 짜다보면 다 아는거 아니에요?
* 구조가 잘 정제되어 있기에 시행착오 없이 좋은 구조를 짤 수 있게 된다
* 모두에게 합의된 이름이기에 쉽게 코드의 구조를 명명하고 남에게 나의 아이디어를 명확하게 전달할 수 있게 된다
## 패턴들
### 전략 패턴
> * object
>     * strategy
>     * setStartegy() // strategy를 넘겨받아 저장한다
>     * doStrategy() // startegy 의 행동을 실행한다
> * strategy1
>     * doSth() // 적당한 행동을 한다
> * strategy2
>     * doSth()

* 특정 전략을 상속한 전략군 중에서 적당한 전략을 저장해서 사용하는 방식
* 전략을 쉽게 추가,변경 가능함

### 옵저버 패턴
> * subject
>     * observers
>     * addObserver() // observers 에 observer 를 추가한다
>     * removeObserver() 
>     * notifyObserver() // observers 들의 update를 불러준다
> * observer
>     * observer() // subject 를 받아 addObserver를 실행
>     * update() 

* subject에 옵저버들을 등록하고 필요할 때 전부 update해주는 방식
* update떄 모든 정보를 넘겨도 되고, subject의 게터를 불러와도 된다
* observer 의 생성자에서 subject를 받아 addObserver를 실행한다
* 같은 방법으로 remove를 하기위해 observer 에 subject를 저장해두자

### 데코레이터 패턴
> * origin
>     * doSth()
> * decorator // origin을 상속
>     * decorator() // origin 혹은 decorator를 받아 저장한다
>     * doSth() // origin 의 doSth 를 이용하여 뭔가를 한다

* 연쇄적으로 decorator로 감싸주는 방식
* 기본 형태에 다양한 옵션들을 추가하는 것이 간단해짐