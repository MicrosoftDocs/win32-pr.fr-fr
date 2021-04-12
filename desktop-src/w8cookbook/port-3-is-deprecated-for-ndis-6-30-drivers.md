---
title: Le port 3 est déconseillé pour les pilotes NDIS 6,30
description: Le port 3 est déconseillé pour les pilotes NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463834"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="61172-103">Le port 3 est déconseillé pour les pilotes NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="61172-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="61172-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="61172-104">Platforms</span></span>

<span data-ttu-id="61172-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="61172-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="61172-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61172-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="61172-107">Description</span><span class="sxs-lookup"><span data-stu-id="61172-107">Description</span></span>

<span data-ttu-id="61172-108">Windows 8 supprime la prise en charge de la plateforme pour les pilotes WLAN miniport NDIS pour créer ou démarrer le port d’extensibilité IHV (également appelé troisième port).</span><span class="sxs-lookup"><span data-stu-id="61172-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="61172-109">Cette fonctionnalité a été introduite dans Windows 7 en tant que mesure dépannage, tandis que l’Alliance d' Wi-Fi (WFA) a développé la spécification Wi-Fi directe.</span><span class="sxs-lookup"><span data-stu-id="61172-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="61172-110">La spécification est maintenant terminée, les produits qui utilisent Wi-Fi direct sont certifiés et Windows 8 introduit une pile Native Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="61172-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="61172-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="61172-111">Manifestation</span></span>

<span data-ttu-id="61172-112">Rien, car le troisième port est une fonctionnalité de plateforme que les pilotes de miniport WLAN démarrent s’ils ont besoin de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="61172-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="61172-113">Solution</span><span class="sxs-lookup"><span data-stu-id="61172-113">Solution</span></span>

<span data-ttu-id="61172-114">Nous conservons la fonctionnalité de port d’extensibilité disponible pour les pilotes existants qui ne signalent pas NDIS 6,30 pour assurer la compatibilité des appareils.</span><span class="sxs-lookup"><span data-stu-id="61172-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="61172-115">Toutefois, les nouveaux pilotes WLAN qui signalent NDIS 6,30 ne pourront pas démarrer ce port. au lieu de cela, les développeurs de ces pilotes doivent utiliser Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="61172-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




