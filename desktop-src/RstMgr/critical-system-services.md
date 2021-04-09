---
title: Services système critiques
description: Les services système critiques ne peuvent pas être arrêtés et redémarrés par le gestionnaire de redémarrage sans redémarrage du système. Les mises à jour d’un fichier ou d’une ressource en cours d’utilisation par l’un de ces services nécessitent un redémarrage du système.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029903"
---
# <a name="critical-system-services"></a><span data-ttu-id="28180-104">Services système critiques</span><span class="sxs-lookup"><span data-stu-id="28180-104">Critical System Services</span></span>

<span data-ttu-id="28180-105">Les services système critiques ne peuvent pas être arrêtés et redémarrés par le gestionnaire de redémarrage sans redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="28180-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="28180-106">Les mises à jour d’un fichier ou d’une ressource en cours d’utilisation par l’un de ces services nécessitent un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="28180-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="28180-107">**Pour déterminer si un processus est un service système critique.**</span><span class="sxs-lookup"><span data-stu-id="28180-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="28180-108">Inscrivez le processus à l’aide de la fonction [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .</span><span class="sxs-lookup"><span data-stu-id="28180-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="28180-109">Appelez la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) pour accéder à la structure des informations sur le [**\_ processus \_ RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .</span><span class="sxs-lookup"><span data-stu-id="28180-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="28180-110">Le membre **ApplicationType** de la structure [**d' \_ \_ informations de processus RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) retournée contient une valeur d’énumération de [**\_ \_ type d’application RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="28180-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="28180-111">Cette valeur est définie sur **RmCriticial** pour un processus système critique.</span><span class="sxs-lookup"><span data-stu-id="28180-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="28180-112">Les services système critiques incluent smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe avec RPCSS et svchost.exe avec DCOM/PnP.</span><span class="sxs-lookup"><span data-stu-id="28180-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




