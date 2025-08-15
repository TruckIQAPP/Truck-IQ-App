TruckIQ is a mobile-first, AI-powered dispatch and load optimization app built for owner-operators, hot shot drivers, and small trucking fleets. Developed in Streamlit, TruckIQ helps users find and evaluate profitable loads using real-time data from load boards, ELD systems, and truck-specific cost profiles.

At its core, TruckIQ is a smarter alternative to traditional load board browsing. Drivers input their real-world operating data — such as fuel cost, miles per gallon (MPG), driver pay percentage, and monthly fixed expenses — and the app calculates profitability for each load using a simple interface. The result is the TruckIQ Score: a 1–10 ranking that reflects the net profit per load, factoring in deadhead, fuel usage, RPM, and time.

TruckIQ is fully integrated with the Truckstop.com API for live load listings (OAuth-enabled per user) and is expanding support for Motive (formerly KeepTruckin) ELD systems. These integrations enable the app to auto-calculate true running costs based on actual fuel data, route efficiency, and available drive hours (HOS). Users can also track RPM, daily earnings, and per-truck efficiency.

What sets TruckIQ apart is its monetization model: it’s free to use, and it only takes a small percentage (“SmartCut”) from successful load matches. That means no subscriptions, no upfront fees — TruckIQ earns only when the driver does.

This repository contains the core Streamlit app (truckiq_app_mock.py), profit engine logic, and integration placeholders for Truckstop and Motive APIs. It’s designed for mobile deployment via Streamlit Cloud and will later scale to include Stripe for payout handling and Firebase for secure user authentication.

Whether you run one truck or a small fleet, TruckIQ is designed to give you the tools of a full dispatch operation — powered by your real data. Smarter loads, better profits, and full control of your haul decisions.
