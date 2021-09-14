---
description: cet article fournit un index de la documentation sur les api Win32 disponibles pour Windows les fonctionnalités et les technologies.
ms.assetid: FF115416-220F-4FCD-8690-F9C0890CD6CC
title: Technologies d’application de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd764c23b38e7239cea1d4d26d018ecbf9711b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916772"
---
# <a name="desktop-app-technologies"></a>Technologies d’application de bureau

cette section fournit des conseils détaillés et des exemples de code relatifs à Windows fonctionnalités disponibles pour les applications de bureau à l’aide de l’API Win32.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description  |  
|----------------------------------|---|
| [Accessibilité](accessibility/accessibility.md) | fournit des conseils pour les développeurs de Windows qui conçoivent des applications accessibles, les développeurs de technologie d’assistance qui créent des outils tels que les lecteurs d’écran et les loupes, et les ingénieurs de test de logiciels qui créent des scripts automatisés pour tester des applications Windows |
| [Interface utilisateur de bureau](windows-application-ui-development.md) | Fournit des informations qui vous permettent de développer des interfaces utilisateur graphiques pour vos applications, notamment des fonctionnalités telles que les fenêtres et les messages, les ressources et les contrôles. |
| [Environnement de bureau](user-interface.md) | fournit des conseils pour l’intégration et l’extension des fonctionnalités accessibles aux utilisateurs du bureau de Windows, y compris la barre des tâches, le bureau et l’explorateur de fichiers. |
| [Installation d’application et maintenance](application-installing-and-servicing.md) | fournit des informations sur l’utilisation des api et des services fournis par Windows pour installer, gérer et traiter vos applications de bureau. |
| [Audio et vidéo](audio-and-video.md) | Fournit des conseils sur l’utilisation des fonctionnalités audio et vidéo fournies par Windows. |
| [Accès aux données et stockage](data-access-and-storage.md) | Fournit des informations sur l’accès aux données et les fonctionnalités de stockage que vous pouvez utiliser dans vos applications de bureau, notamment la gestion du système de fichiers et les moteurs de synchronisation du Cloud.  |
| [Appareils](devices.md) | Décrit les API permettant d’interagir avec les appareils et les capteurs. |
| [Diagnostics](diagnostics.md) | Fournit des conseils sur le débogage et la gestion des erreurs, le profilage des performances, l’analyse du réseau et d’autres fonctionnalités de diagnostic. |
| [Documents et impression](printdocs/documents-and-printing.md) | décrit les documents et les fonctionnalités d’impression des Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.  |
| [Graphismes et jeux ](graphics-and-multimedia.md) | fournit des informations sur les fonctionnalités graphiques et de jeu de Windows, y compris DirectX et l’imagerie numérique.  |
| [Mise en réseau et Internet](networking.md) | fournit des conseils sur la mise en réseau et les fonctionnalités Internet de Windows, notamment la gestion du réseau, les api HTTP et l’appel de procédure distante (RPC). |
| [Sécurité et identité](security.md) | Fournit des informations sur l’authentification, l’autorisation, le chiffrement et d’autres fonctionnalités de sécurité de Windows. |
| [Services système](system-services.md) | Fournit des conseils sur les fonctionnalités fondamentales du système d’exploitation, telles que les processus et les threads, les services, les bibliothèques de liens dynamiques, COM, le registre, et bien plus encore. |
| [IA et Machine Learning](/windows/ai/) | Transformez votre application Windows en utilisant la puissance de l’intelligence artificielle. Windows IA vous permet à vous et à votre entreprise d’aller plus loin en fournissant des solutions intelligentes à des problèmes complexes. |

<!--
<br/>

| User Interface and accessibility | System services and fundamentals  |  Audio, video, and graphics  |
|----------------------------------|---|----|
| [Desktop User Interface](windows-application-ui-development.md)<br/>[Windows and messages](winmsg/windowing.md)<br/>[Desktop Window Manager](dwm/dwm-overview.md)<br/>[Menus and other resources](menurc/resources.md)<br/>[Dialog boxes](dlgbox/dialog-boxes.md)<br/>[Data exchange](dataxchg/data-exchange.md)<br/>[High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)<br/>[Windows controls (Win32)](controls/window-controls.md)<br/>[Desktop environment and shell](user-interface.md)<br/>[Windows Property System](properties/windows-properties-system.md)<br/>[Accessibility](accessibility.md) | [System services](system-services.md)<br/>[Component Object Model (COM)](com/component-object-model--com--portal.md)<br/>[COM+](cossdk/component-services-portal.md)<br/>[Structured storage](stg/structured-storage-start-page.md)<br/>[Dynamic-link libraries](dlls/dynamic-link-libraries.md)<br/>[Interprocess communications](ipc/interprocess-communications.md)<br/>[Memory management](memory/memory-management.md)<br/>[Power management](power/power-management-portal.md)<br/>[Processes and threads](procthread/processes-and-threads.md)<br/>[Services](services/services.md)<br/>[Synchronization](sync/synchronization.md)<br/>[Windows system information](sysinfo/windows-system-information.md) | [Audio and video technologies](audio-and-video.md)<br/>[Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)<br/>[DirectShow](directshow/directshow.md)<br/>[Windows Multimedia](multimedia/windows-multimedia-start-page.md)<br/>[Graphics and gaming technologies](graphics-and-multimedia.md)<br/>[DirectX](directx.md)<br/>[Direct2D](direct2d/direct2d-portal.md)<br/>[Direct3D](direct3d.md)<br/>[Windows GDI](gdi/windows-gdi.md)<br/>[GDI+](gdiplus/-gdiplus-gdi-start.md)<br/>[OpenGL](opengl/opengl.md)<br/>[Windows Imaging Component](wic/-wic-lh.md) |

<br/>

| Networking and Internet | Data access and storage  |  Devices, documents, and printing  |
|----------------------------------|---|----|
| [Networking and Internet overview](networking.md)<br/>[Remote Procedure Call](rpc/rpc-start-page.md)<br/>[Delivery optimization](delivery_optimization/delivery-optimization-portal.md)<br/>[Network interfaces](network-interfaces.md)<br/>[Network management](netmgmt/network-management.md)<br/>[Network share management](netshare/network-share-management.md)<br/>[Windows networking](wnet/windows-networking-wnet-.md)<br/>[Windows Sockets 2](winsock/windows-sockets-start-page-2.md)<br/>[Wireless networking](wireless-networking.md) | [Data access and storage overview](data-access-and-storage.md)<br/>[Local file systems](fileio/file-systems.md)<br/>[Distributed File System](dfs/distributed-file-system.md)<br/>[Projected File System](projfs/projected-file-system.md)<br/>[Cloud sync engines](cfapi/cloud-files-api-portal.md)<br/>[Virtual Storage](VStor/virtual-storage.md)<br/>[Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)<br/>[Backup](backup.md) | [Devices overview](devices.md)<br/>[Communications resources](devio/communications-resources.md)<br/>[Location API](locationapi/windows-location-api-portal.md)<br/>[Sensor API](sensorsapi/portal.md)<br/>[UPnP APIs](upnp/universal-plug-and-play-start-page.md)<br/>[Windows Portable Devices](windows-portable-devices.md)<br/>[Documents and printing](printdocs/documents-and-printing.md) |

<br/>

| Security and identity | Diagnostics and testing  |  Packaging and installation  |
|----------------------------------|---|----|
| [Security and identity overview](security.md)<br/>[Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)<br/>[Authentication](secauthn/authentication-portal.md)<br/>[Authorization](secauthz/authorization-portal.md)<br/>[Certificate Enrollment API](seccertenroll/certenroll-portal.md)<br/>[Cryptography (CNG)](seccng/cng-portal.md)<br/>[Rights Management](SrvNodes/rights-management.md)<br/>[Security Management](secmgmt/management-portal.md)<br/>[TPM Base Services](tbs/tpm-base-services-portal.md)<br/>[Windows Biometric Framework](secbiomet/biometric-service-api-portal.md) | [Diagnostics overview](diagnostics.md)<br/>[Debugging and error handling](debugging-and-error-handling.md)<br/>[Network Monitor](netmon2/network-monitor.md)<br/>[System Monitor](sysmon/system-monitor-portal.md)<br/>[Performance counters](perfctrs/performance-counters-portal.md)<br/>[Windows error reporting](wer/windows-error-reporting.md)<br/>[Windows events](events/windows-events.md)<br/>[TraceLogging](tracelogging/trace-logging-portal.md)<br/>[Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index) | [MSIX packaging](//docs.microsoft.com/windows/msix)<br/>[Application install and servicing](application-installing-and-servicing.md)<br/>[Side-by-side assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)<br/>[Packaging and query of UWP apps](appxpkg/appx-portal.md)<br/>[Windows Installer](msi/windows-installer-portal.md)<br/>[Desktop Application Program](appxpkg/windows-desktop-application-program.md)<br/>[Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/) |

-->

<!--
:::row:::
    :::column:::
        ![User Interface and accessibility](/media/illustrations/bcs-partner-advanced-management-add-user-1.svg?branch=master)
        ### User Interface and accessibility
        * [Desktop User Interface](windows-application-ui-development.md)
        * [Windows and messages](winmsg/windowing.md)
        * [Desktop Window Manager](dwm/dwm-overview.md)
        * [Dialog boxes](dlgbox/dialog-boxes.md)
        * [Menus and other resources](menurc/resources.md)
        * [Data exchange](dataxchg/data-exchange.md)
        * [High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)
        * [Windows controls (Win32)](controls/window-controls.md)
        * [Desktop environment and shell](user-interface.md)
        * [Windows Property System](properties/windows-properties-system.md)
        * [Accessibility](accessibility.md)
    :::column-end:::
    :::column:::
        ![System and fundamentals](/media/illustrations/biztalk-get-started-get-started.svg?branch=master)
        ### System services and fundamentals
        * [System services](system-services.md)
        * [Component Object Model (COM)](com/component-object-model--com--portal.md)
        * [COM+](cossdk/component-services-portal.md)
        * [Structured storage](stg/structured-storage-start-page.md)
        * [Dynamic-link libraries](dlls/dynamic-link-libraries.md)
        * [Interprocess communications](ipc/interprocess-communications.md)
        * [Memory management](memory/memory-management.md)
        * [Power management](power/power-management-portal.md)
        * [Processes and threads](procthread/processes-and-threads.md)
        * [Services](services/services.md)
        * [Synchronization](sync/synchronization.md)
        * [Windows system information](sysinfo/windows-system-information.md)
    :::column-end:::
    :::column:::
        ![Audio, video, and graphics](/media/illustrations/virtualization-containers-samples.svg?branch=master)
        ### Audio, video, and graphics
        * [Audio and video technologies](audio-and-video.md)
        * [Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)
        * [DirectShow](directshow/directshow.md)
        * [Windows Multimedia](multimedia/windows-multimedia-start-page.md)
        * [Graphics and gaming technologies](graphics-and-multimedia.md)
        * [DirectX](directx.md)
        * [Direct2D](direct2d/direct2d-portal.md)
        * [Direct3D](direct3d.md)
        * [Windows GDI](gdi/windows-gdi.md)
        * [GDI+](gdiplus/-gdiplus-gdi-start.md)
        * [OpenGL](opengl/opengl.md)
        * [Windows Imaging Component](wic/-wic-lh.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Networking and Internet](/media/illustrations/teams-voice-deployment.svg?branch=master)
        ### Networking and Internet
        * [Networking and Internet overview](networking.md)
        * [Remote Procedure Call](rpc/rpc-start-page.md)
        * [Delivery Optimization](delivery_optimization/delivery-optimization-portal.md)
        * [Network interfaces](network-interfaces.md)
        * [Network Management](netmgmt/network-management.md)
        * [Network Share Management](netshare/network-share-management.md)
        * [Windows Networking](wnet/windows-networking-wnet-.md)
        * [Windows Sockets 2](winsock/windows-sockets-start-page-2.md)
        * [Wireless Networking](wireless-networking.md)
    :::column-end:::
    :::column:::
        ![Data access and storage](/media/illustrations/azure-architecture-patterns.svg?branch=master)
        ### Data access and storage
        * [Data access and storage overview](data-access-and-storage.md)
        * [Local File Systems](fileio/file-systems.md)
        * [Distributed File System](dfs/distributed-file-system.md)
        * [Projected File System](projfs/projected-file-system.md)
        * [Cloud Sync Engines](cfapi/cloud-files-api-portal.md)
        * [Virtual Storage](VStor/virtual-storage.md)
        * [Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)
        * [Backup](backup.md)
    :::column-end:::
    :::column:::
        ![Devices, documents, and printing](/media/illustrations/virtualization-hperv-server-doc-archive.svg?branch=master)
        ### Devices, documents, and printing
        * [Devices overview](devices.md)
        * [Communications Resources](devio/communications-resources.md)
        * [Location API](locationapi/windows-location-api-portal.md)
        * [Sensor API](sensorsapi/portal.md)
        * [UPnP APIs](upnp/universal-plug-and-play-start-page.md)
        * [Windows Portable Devices](windows-portable-devices.md)
        * [Documents and Printing](printdocs/documents-and-printing.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Security and identity](/media/illustrations/bcs-partner-advanced-management-password-3.svg?branch=master)
        ### Security and identity
        * [Security and identity overview](security.md)
        * [Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)
        * [Authentication](secauthn/authentication-portal.md)
        * [Authorization](secauthz/authorization-portal.md)
        * [Certificate Enrollment API](seccertenroll/certenroll-portal.md)
        * [Cryptography (CNG)](seccng/cng-portal.md)
        * [Rights Management](SrvNodes/rights-management.md)
        * [Security Management](secmgmt/management-portal.md)
        * [TPM Base Services](tbs/tpm-base-services-portal.md)
        * [Windows Biometric Framework](secbiomet/biometric-service-api-portal.md)
    :::column-end:::
    :::column:::
        ![Diagnostics and testing](/media/illustrations/team-services-dev-ops-test.svg?branch=master)
        ### Diagnostics and testing
        * [Diagnostics overview](diagnostics.md)
        * [Debugging and error handling](debugging-and-error-handling.md)
        * [Network Monitor](netmon2/network-monitor.md)
        * [System Monitor](sysmon/system-monitor-portal.md)
        * [Performance counters](perfctrs/performance-counters-portal.md)
        * [Windows error reporting](wer/windows-error-reporting.md)
        * [Windows events](events/windows-events.md)
        * [TraceLogging](tracelogging/trace-logging-portal.md)
        * [Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index)
    :::column-end:::
    :::column:::
        ![Packaging and installation](/media/illustrations/biztalk-host-integration-install-configure.svg?branch=master)
        ### Packaging and installation
        * [MSIX packaging and deployment](//docs.microsoft.com/windows/msix)
        * [Application Installation and Servicing](application-installing-and-servicing.md)
        * [Isolated Applications and Side-by-side Assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
        * [Packaging, deployment, and query of UWP apps](appxpkg/appx-portal.md)
        * [Windows Installer](msi/windows-installer-portal.md)
        * [Windows Desktop Application Program](appxpkg/windows-desktop-application-program.md)
        * [Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/)
    :::column-end:::
:::row-end:::
-->
