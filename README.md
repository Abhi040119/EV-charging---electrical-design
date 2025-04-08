# EV-charging---electrical-design
def calculate_total_load(ev_list):
    total_power = 0
    for ev in ev_list:
        total_power += ev['charging_power']
    return total_power

def generate_ev_list(count, power_per_ev):
    return [{'id': i+1, 'charging_power': power_per_ev} for i in range(count)]

# Example usage
if __name__ == "__main__":
    evs = generate_ev_list(5, 7.2)  # 5 EVs, 7.2 kW each
    total = calculate_total_load(evs)
    print(f"Total Load: {total} kW")
