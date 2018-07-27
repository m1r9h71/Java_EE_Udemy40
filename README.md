# Java_EE_Udemy40
Reading a list of all Passengers
Created a new Servlet calledd "Passengers" that mirrors the Servlet "FLights". This will be used in the next tutorial.

Passengers: 

      List<Passenger> pList = (List<Passenger>) ps.getPassengers();
		
		  request.setAttribute("passenger_list", pList);
		
		  PrintWriter out = response.getWriter();
		  out.println("The Passenger List will be displayed here: ");


PassengerService:

    public List<Passenger> getPassengers() {
    	
    		TypedQuery<Passenger> query = em.createQuery("SELECT p FROM Passenger p", Passenger.class);
    	
    		List<Passenger> pList = query.getResultList();
    			
    		return null;
    	
    }
