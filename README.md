xdef classify_ticket(ticket):
    ticket = ticket.lower()

    if "payment" in ticket or "bill" in ticket:
        return "Billing"
    elif "network" in ticket or "wifi" in ticket:
        return "Network"
    elif "error" in ticket or "bug" in ticket:
        return "Technical"
    else:
        return "General"

ticket = input("Enter ticket: ")
category = classify_ticket(ticket)

print("Ticket Category:", category)
