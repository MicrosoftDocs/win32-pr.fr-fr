---
description: Informations de référence sur les commandes COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Informations de référence sur les commandes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544565"
---
# <a name="copp-command-reference"></a><span data-ttu-id="c2be0-103">Informations de référence sur les commandes COPP</span><span class="sxs-lookup"><span data-stu-id="c2be0-103">COPP Command Reference</span></span>

<span data-ttu-id="c2be0-104">Cette section décrit les commandes COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="c2be0-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="c2be0-105">Les commandes suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="c2be0-105">The following commands are defined.</span></span>



| <span data-ttu-id="c2be0-106">Commande</span><span class="sxs-lookup"><span data-stu-id="c2be0-106">Command</span></span>              | <span data-ttu-id="c2be0-107">GUID</span><span class="sxs-lookup"><span data-stu-id="c2be0-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="c2be0-108">Définir le niveau de protection</span><span class="sxs-lookup"><span data-stu-id="c2be0-108">Set Protection Level</span></span> | <span data-ttu-id="c2be0-109">**\_COPPSETPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="c2be0-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="c2be0-110">Définir la signalisation</span><span class="sxs-lookup"><span data-stu-id="c2be0-110">Set Signaling</span></span>        | <span data-ttu-id="c2be0-111">**\_COPPSETSIGNALING DXVA**</span><span class="sxs-lookup"><span data-stu-id="c2be0-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="c2be0-112">Définir le niveau de protection, commande</span><span class="sxs-lookup"><span data-stu-id="c2be0-112">Set Protection Level Command</span></span>

<span data-ttu-id="c2be0-113">Définit le niveau de protection pour un mécanisme de protection de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2be0-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="c2be0-114">Selon le connecteur, il peut être possible d’appliquer plusieurs mécanismes de protection sur le même connecteur, avec des paramètres différents pour chaque mécanisme.</span><span class="sxs-lookup"><span data-stu-id="c2be0-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="c2be0-115">**GUID**: DXVA \_ COPPSetProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="c2be0-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="c2be0-116">**Données d’entrée**: une structure [**\_ COPPSetProtectionLevelCmdData DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .</span><span class="sxs-lookup"><span data-stu-id="c2be0-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="c2be0-117">Définir la commande de signalisation</span><span class="sxs-lookup"><span data-stu-id="c2be0-117">Set Signaling Command</span></span>

<span data-ttu-id="c2be0-118">Spécifie des informations sur le signal vidéo autre que le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="c2be0-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="c2be0-119">Pour CGMS-A, certaines normes de protection requièrent que le signal televsion contient des informations sur les proportions et d’autres informations dans les mêmes paquets de forme d’onde VBI que les bits CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="c2be0-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="c2be0-120">Les télévisions peuvent s’afficher mal si les informations sur les proportions ne sont pas cohérentes avec le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c2be0-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="c2be0-121">L’application peut utiliser cette commande pour spécifier les proportions afin que le pilote Graphics puisse générer les paquets VBI appropriés.</span><span class="sxs-lookup"><span data-stu-id="c2be0-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="c2be0-122">Cette commande est également conçue pour être extensible si des informations de signal supplémentaires sont requises dans les normes futures.</span><span class="sxs-lookup"><span data-stu-id="c2be0-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="c2be0-123">**GUID**: DXVA \_ COPPSetSignaling</span><span class="sxs-lookup"><span data-stu-id="c2be0-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="c2be0-124">**Données d’entrée**: une structure [**\_ COPPSetSignalingCmdData DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="c2be0-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2be0-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2be0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2be0-126">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="c2be0-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



