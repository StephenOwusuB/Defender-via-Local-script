# Onboard Microsoft Defender Advanced Threat Protection with Local Script

To deploy using a local script:

1. Go to [security.microsoft.com](https://security.microsoft.com).
2. Navigate to **Settings** and select **Endpoints**.
![Select Endpoint](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/DGPO%20images/MDE%20onboard%202.png)
4. Scroll down to **Device management** and select **Onboarding**.
5. Choose the onboarding options with the deployment method set to **Group Policy**. Ensure to download the package for Group Policy as the scripts vary based on the deployment method.
![Select Local script](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/LocalScript/MDE%20onboard%203.png)
7. Once the download is complete, run the executable file (`.exe`).
![Double Click on Exe](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/LocalScript/MDE%20onboard%2029.png)
8. A command prompt will pop up. Enter `Y` to continue the deployment.
![Enter Y](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/LocalScript/MDE%20onboard%2030.png)
10. The deployment may take 5 to 8 minutes to appear in the portal.
11. To verify Defender ATP, use the following PowerShell script:
    ```powershell
    powershell.exe -NoExit -ExecutionPolicy Bypass -WindowStyle Hidden $ErrorActionPreference= 'silentlycontinue';(New-Object System.Net.WebClient).DownloadFile('http://127.0.0.1/1.exe', 'C:\\test-WDATP-test\\invoice.exe');Start-Process 'C:\\test-WDATP-test\\invoice.exe'
    ```
12. You will find an alert under Incidents & Alerts 
13. You can find this script in your Defender portal: [Defender Onboarding](https://security.microsoft.com/securitysettings/endpoints/onboarding?tid=d8b703ef-81f7-478a-96a2-298aca6e1a76).

Feel free to adjust the details as needed!
