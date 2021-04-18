---
description: Illustre l’utilisation des fonctions de base de gestion de réseau sans fil.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemple d’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519093"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="1b896-103">Exemple d’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="1b896-103">Native Wifi API Sample</span></span>

<span data-ttu-id="1b896-104">Un exemple d’API WiFi native qui illustre l’utilisation des fonctions de gestion de réseau sans fil de base est inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1b896-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1b896-105">La dernière version du SDK Windows est disponible à partir du [Centre de téléchargement](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="1b896-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="1b896-106">Par défaut, l’exemple de code source wifi natif est installé dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="1b896-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="1b896-107">**C : \\ Program Files \\ Microsoft SDK \\ \\ <version number> \\ exemples Windows \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="1b896-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="1b896-108">L’exemple d’API WiFi Native se trouve dans le dossier suivant :</span><span class="sxs-lookup"><span data-stu-id="1b896-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="1b896-109">**autoconfig**</span><span class="sxs-lookup"><span data-stu-id="1b896-109">**autoconfig**</span></span>

<span data-ttu-id="1b896-110">L’exemple WiFi natif peut être compilé et exécuté sur Windows Vista et versions ultérieures, Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="1b896-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="1b896-111">Certaines fonctionnalités de l’exemple ne sont pas prises en charge sur Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="1b896-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="1b896-112">Pour obtenir la liste des fonctions prises en charge par Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2, consultez [prise en charge de l’API WiFi native sur Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span><span class="sxs-lookup"><span data-stu-id="1b896-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="1b896-113">L’exemple WiFi natif montre comment effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b896-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="1b896-114">Énumérer les interfaces sans fil.</span><span class="sxs-lookup"><span data-stu-id="1b896-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="1b896-115">Consultez [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="1b896-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="1b896-116">Obtient les fonctionnalités d’une interface.</span><span class="sxs-lookup"><span data-stu-id="1b896-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="1b896-117">Consultez [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="1b896-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="1b896-118">\* \* Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 : \* \* cette fonctionnalité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1b896-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="1b896-119">Interrogez une interface.</span><span class="sxs-lookup"><span data-stu-id="1b896-119">Query an interface.</span></span> <span data-ttu-id="1b896-120">Consultez [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="1b896-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="1b896-121">Définissez les paramètres d’une interface réseau.</span><span class="sxs-lookup"><span data-stu-id="1b896-121">Set parameters for a network interface.</span></span> <span data-ttu-id="1b896-122">Consultez [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="1b896-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="1b896-123">Cette fonction peut être utilisée pour activer et désactiver la radio sans fil (et, par conséquent, activer ou désactiver la connectivité de réseau sans fil).</span><span class="sxs-lookup"><span data-stu-id="1b896-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="1b896-124">Recherchez les réseaux sans fil disponibles.</span><span class="sxs-lookup"><span data-stu-id="1b896-124">Scan for available wireless networks.</span></span> <span data-ttu-id="1b896-125">Consultez [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="1b896-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="1b896-126">Obtient la liste des réseaux sans fil disponibles ou visibles.</span><span class="sxs-lookup"><span data-stu-id="1b896-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="1b896-127">Consultez [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="1b896-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="1b896-128">Obtenir, enregistrer ou supprimer un profil.</span><span class="sxs-lookup"><span data-stu-id="1b896-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="1b896-129">Consultez [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)et [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="1b896-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="1b896-130">Se connecter ou se déconnecter d’un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="1b896-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="1b896-131">Consultez [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) et [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="1b896-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b896-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b896-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b896-133">Utilisation de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="1b896-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="1b896-134">Forum du kit de développement logiciel sans fil Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b896-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="1b896-135">[Résolution des problèmes de connexions sans fil Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="1b896-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 
