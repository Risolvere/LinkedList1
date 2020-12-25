public class LinkedList {
    Node head;



    public void insert(int data){
        Node node = new Node();
        node.data = data;

        if(head == null ){
            head = node;
        }
        else{
            Node n = head;
            while(n.next != null){
                n = n.next;
            }
            n.next = node;
        }
    }

    public void insertFront(int data){
        Node newNode = new Node();
        newNode.data = data;
        newNode.next = head;
        head = newNode;
    }

    public void insertMiddle(int data){
        Node slow = head;
        Node fast = head;
        while(fast !=null && fast.next !=null){
            slow = slow.next;
            fast = fast.next.next;
        }
        slow.data= data;
    }

    public void insertToTheEnd(int data){
        Node endNode = head;
        while(endNode.next != null){
            endNode = endNode.next;
        }
        endNode.data = data;
    }

    public void display(){
        Node node = head;
        while(node.next != null){
            System.out.println(node.data);
            node = node.next;
        }
        System.out.println(node.data);

    }
}
