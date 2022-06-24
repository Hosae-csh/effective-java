아이템1. 핵심 정리 - 정적 팩터리 메서드의 장점
====================================

    public class Order {
    
        private boolean prime;
        
        private boolean urgent;

        private Product product;

        public Order(Product product, boolean prime){
            this.product = product;
            this.prime = prime;
        }

        public Order(boolean urgent, Product product){
            this.product = product;
            this.urgent = urgent;
        }

        public static Order primeOrder (Product product){
            Order order = new Order();
            order.prime = true;
            order.product = product;
            return order;
        }

        public static Order urgentOrder (Product product){
            Order order = new Order();
            order.urgent = true;
            order.product = product;
            return order;
        }

디자인 패턴과는 무관하다 ex)팩토리 패턴, 추상화 팩토리 패턴과 무관함
위와 같이하는게아니라 아래와 같이 하라는게 정적 팩터리 메서드를 고려하라는 뜻

