
import streamlit as st
import pandas as pd

st.set_page_config(page_title="TruckIQ", layout="centered")

# ---- HEADER ----
st.title("🚛 TruckIQ – Smarter Loads. Bigger Profits.")
st.markdown("Connect your truck, track your numbers, and let TruckIQ optimize your hauls.")

# ---- TRUCK PROFILE ----
st.header("🔧 Truck Profile Setup")
mpg = st.number_input("Miles Per Gallon (MPG)", min_value=4.0, max_value=12.0, value=6.5)
fuel_cost = st.number_input("Fuel Cost per Gallon ($)", min_value=2.00, max_value=7.00, value=4.50)
driver_percent = st.slider("Driver Pay Percentage (%)", min_value=0, max_value=100, value=30)
dispatch_fee = st.slider("Dispatch Fee Percentage (%)", min_value=0, max_value=100, value=8)
monthly_fixed_cost = st.number_input("Monthly Fixed Costs ($)", min_value=500, value=3000)

# ---- LOAD INPUT ----
st.header("📦 Load Details")
load_pay = st.number_input("Load Pay ($)", min_value=100, value=1800)
miles = st.number_input("Total Miles", min_value=50, value=600)
deadhead = st.number_input("Deadhead Miles", min_value=0, value=50)

# ---- CALCULATIONS ----
if miles > 0:
    total_miles = miles + deadhead
    fuel_used = total_miles / mpg
    fuel_cost_total = fuel_used * fuel_cost
    driver_cut = load_pay * (driver_percent / 100)
    dispatch_cut = load_pay * (dispatch_fee / 100)
    total_expense = fuel_cost_total + driver_cut + dispatch_cut + (monthly_fixed_cost / 21)
    net_profit = load_pay - total_expense
    rpm = load_pay / miles
    truckiq_score = round((net_profit / total_miles) * 10, 1)  # Simple scoring logic

    # ---- OUTPUT ----
    st.subheader("📊 TruckIQ Summary")
    st.write(f"**Rate per Mile (RPM):** ${rpm:.2f}")
    st.write(f"**Estimated Fuel Cost:** ${fuel_cost_total:.2f}")
    st.write(f"**Driver Pay:** ${driver_cut:.2f}")
    st.write(f"**Dispatch Fee:** ${dispatch_cut:.2f}")
    st.write(f"**Net Profit:** ${net_profit:.2f}")
    st.markdown(f"### 🧠 TruckIQ Score: **{truckiq_score}/10**")
