---
description: Illustre l’utilisation de fonctions de réseau hébergé sans fil.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Exemple de réseau hébergé sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514642"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="165b5-103">Exemple de réseau hébergé sans fil</span><span class="sxs-lookup"><span data-stu-id="165b5-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="165b5-104">Un exemple de réseau hébergé sans fil illustrant l’utilisation de fonctions de réseau hébergé sans fil est inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="165b5-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="165b5-105">La dernière version du SDK Windows est disponible à partir du [Centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="165b5-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="165b5-106">Par défaut, le code source de l’exemple de réseau hébergé sans fil est installé dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="165b5-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="165b5-107">**C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="165b5-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="165b5-108">L’exemple de réseau hébergé sans fil se trouve dans le dossier suivant :</span><span class="sxs-lookup"><span data-stu-id="165b5-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="165b5-109">**WirelessHostedNetwork**</span><span class="sxs-lookup"><span data-stu-id="165b5-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="165b5-110">L’exemple de réseau hébergé sans fil peut être compilé sur le SDK Windows pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="165b5-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="165b5-111">L’exemple de réseau hébergé sans fil peut être exécuté sur Windows 7 et sur Windows Server 2008 R2 avec le service de réseau local sans fil installé.</span><span class="sxs-lookup"><span data-stu-id="165b5-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="165b5-112">Sur Windows 7 et sur Windows Server 2008 R2 avec le service de réseau local sans fil installé, le système d’exploitation installe un appareil virtuel si une carte sans fil pouvant être hébergée sur un réseau hébergé est présente sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="165b5-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="165b5-113">Cet appareil virtuel s’affiche normalement dans le « dossier Connexions réseau » en tant que « connexion réseau sans fil 2 » avec le nom d’appareil « carte miniport Microsoft Virtual WiFi » si l’ordinateur possède une seule carte réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="165b5-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="165b5-114">Cet appareil virtuel est utilisé exclusivement pour effectuer des connexions de point d’accès logiciel (SoftAP).</span><span class="sxs-lookup"><span data-stu-id="165b5-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="165b5-115">La durée de vie de cet appareil virtuel est liée à la carte sans fil physique.</span><span class="sxs-lookup"><span data-stu-id="165b5-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="165b5-116">Si la carte sans fil physique est désactivée, cet appareil virtuel est également supprimé.</span><span class="sxs-lookup"><span data-stu-id="165b5-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="165b5-117">Les fonctions de réseau hébergé sans fil permettent de démarrer et d’arrêter le réseau hébergé sans fil, de configurer ou de modifier les paramètres ou de demander des informations.</span><span class="sxs-lookup"><span data-stu-id="165b5-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="165b5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="165b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="165b5-119">À propos du réseau hébergé sans fil</span><span class="sxs-lookup"><span data-stu-id="165b5-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="165b5-120">Utilisation du partage de connexion Internet et du réseau hébergé</span><span class="sxs-lookup"><span data-stu-id="165b5-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="165b5-121">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="165b5-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="165b5-122">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="165b5-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="165b5-123">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="165b5-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="165b5-124">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="165b5-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="165b5-125">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="165b5-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="165b5-126">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="165b5-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="165b5-127">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="165b5-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="165b5-128">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="165b5-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="165b5-129">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="165b5-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="165b5-130">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="165b5-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="165b5-131">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="165b5-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



