# AOA-based-physical-layer-authentication-in-Analog-arrays

This project investigates physical layer authentication (PLA) using Angle of Arrival (AoA) in analog array multiple-input multiple-output (MIMO) systems. We analyzed how a base station (BS) can authenticate users by estimating the AoA from pilot signals and identifying vulnerabilities to impersonation attacks.

We developed and analyzed system models for each of the three configurations, considering the signal received at the BS and the array steering vectors for both legitimate users (Alice) and attackers (Eve).

**1) Uniform Linear Array (ULA)**: A foundational model with a single BS and a ULA, using Maximum Likelihood Estimation (MLE) for AoA.

**2) Uniform Planar Array (UPA)**: An extension to 3D space, providing a finer spatial resolution by estimating both azimuth and elevation angles.

**3) Two-Base Station System**: A cooperative model where two geographically separated BSs work together to authenticate users, leveraging spatial diversity to counter spoofing.

**Impersonation Attacks**

The project analyzed several adversarial scenarios to test the robustness of the authentication systems:

**1) Random Attack**: The attacker transmits a random signal, which is easily detected.

**2) Code-Based Attack**: The attacker has some knowledge of the system and manipulates their signal to partially mimic the legitimate user.

**3) Location-Based Attack**: The most sophisticated attack, where the attacker knows the legitimate user's location and manipulates their signal to make it appear as if it's coming from the legitimate user's direction, effectively masking their true location.

**Simulations and Results**

Simulations were performed to evaluate the effectiveness of the proposed systems and the impact of the different attacks. The negative log-likelihood cost function was used to visualize the AoA estimation.

**Log Likelihood Plots for UPA**

<img width="1441" height="583" alt="Screenshot 2025-09-11 180756" src="https://github.com/user-attachments/assets/69b98a1a-e954-4fec-92cc-6d9f9fa6d7cd" />

This plot shows that with a UPA provides a more complex spatial signature, making it more robust. However, the location-based attack can still be successful, as the attacker can force the minimum of the likelihood function to shift to the legitimate user's azimuth and elevation angles.

**Log Likelihood Plot for Two Base Station**

<img width="691" height="387" alt="Screenshot 2025-09-11 180833" src="https://github.com/user-attachments/assets/51f8e430-6f45-4eb2-b9fb-c0c9853f775e" />

This plot shows the log-likelihood for a two-base station system. Even under a location-based attack ("Loc Attack"), the two plots do not align, demonstrating how the dual-BS system can detect inconsistencies and successfully thwart the attack.

**Conclusion**

The project successfully demonstrated that both the 3D AoA extension and the cooperative multi-BS architecture significantly enhance the security of physical layer authentication. The combined use of these strategies offers a robust defense against advanced impersonation attempts by leveraging increased spatial resolution and diversity.

Single Base Station with UPA code : https://colab.research.google.com/drive/1bo8pQVG6bhUuwIZ2iO4iZOdkn7aIew5G

Two base station code : https://colab.research.google.com/drive/1mI3k40P49Vl68pW16RolZadfQ5aixhNX
