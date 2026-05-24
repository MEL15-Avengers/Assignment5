
# Section 3.4 – Operating System Platform Testing

This section records operating system platform testing carried out for Moonlight Warehouse Management System (Moonlight WMS). The purpose of this testing is to confirm that the application remains functional across supported desktop operating systems and that core workflows such as login, dashboard access, page navigation, and main module loading operate correctly.

The main workflows checked during platform testing were login, Dashboard, Products, Inventory, and Alerts. Where available, the browser used during each operating system test is also recorded.

| Who | Operating System | Test Objective | Steps Taken | Expected Result | Actual Result | Pass / Fail |
|-----|------------------|----------------|-------------|-----------------|---------------|-------------|
| Marc Martin | Windows 11 | Verify that Moonlight WMS can be opened and used correctly on a Windows desktop environment. | Open supported browser on Windows 11 → access Moonlight WMS → log in with valid account → open Dashboard, Products, Inventory, and Alerts pages → verify normal page loading and navigation. | Login should succeed, dashboard should load, and major modules should open without critical layout or script errors. | Testing on Windows 11 completed successfully. Login worked correctly, the dashboard loaded, and Products, Inventory, and Alerts pages opened and remained usable during navigation. | Pass |
| Ashima Basnet | macOS | Verify that Moonlight WMS can be opened and used correctly on a macOS desktop environment. | Open supported browser on macOS → access Moonlight WMS → log in → navigate across core modules. | Login should succeed and main modules should remain functional. | Pending team member test result. | Pending |
| Anil / Team | Linux | Verify that Moonlight WMS can be opened and used correctly on a Linux desktop environment. | Open supported browser on Linux → access Moonlight WMS or local server → log in → navigate across core modules. | Login should succeed and main modules should remain functional. | Pending team member test result. | Pending |
