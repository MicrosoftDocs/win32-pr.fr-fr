---
description: Envoi de commandes COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Envoi de commandes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516340"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="8b1e4-103">Envoi de commandes COPP</span><span class="sxs-lookup"><span data-stu-id="8b1e4-103">Sending COPP Commands</span></span>

<span data-ttu-id="8b1e4-104">Pour envoyer une commande COPP (Certified Output Protection Protocol), remplissez une structure [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) comme suit :</span><span class="sxs-lookup"><span data-stu-id="8b1e4-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="8b1e4-105">**guidCommandID**.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-105">**guidCommandID**.</span></span> <span data-ttu-id="8b1e4-106">GUID qui identifie la commande.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-106">The GUID that identifies the command.</span></span> <span data-ttu-id="8b1e4-107">Consultez les informations de référence sur les commandes COPP.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="8b1e4-108">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-108">**dwSequence**.</span></span> <span data-ttu-id="8b1e4-109">Numéro de séquence de la commande.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-109">The command sequence number.</span></span> <span data-ttu-id="8b1e4-110">Incrémentez cette valeur après chaque commande.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-110">Increment this value after each command.</span></span> <span data-ttu-id="8b1e4-111">(Cette valeur est indiquée en tant que **uCommandSeq** dans [le lancement d’une session Copp](initiating-a-copp-session.md).)</span><span class="sxs-lookup"><span data-stu-id="8b1e4-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="8b1e4-112">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-112">**cbSizeData**.</span></span> <span data-ttu-id="8b1e4-113">Taille, en octets, des données nécessaires pour la commande.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="8b1e4-114">**CommandData**.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-114">**CommandData**.</span></span> <span data-ttu-id="8b1e4-115">Données pour la commande.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-115">Data for the command.</span></span>

<span data-ttu-id="8b1e4-116">Une fois que vous avez rempli ces données, calculez le MAC pour la commande :</span><span class="sxs-lookup"><span data-stu-id="8b1e4-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="8b1e4-117">Calculez la balise OMAC-1 pour le bloc de données qui apparaît après le membre **macKDI** de la structure **AMCOPPCommand** .</span><span class="sxs-lookup"><span data-stu-id="8b1e4-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="8b1e4-118">Copiez cette valeur dans le membre **macKDI** de la structure.</span><span class="sxs-lookup"><span data-stu-id="8b1e4-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="8b1e4-119">À présent, transmettez la structure à la méthode [**IAMCertifiedOutputProtection ::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .</span><span class="sxs-lookup"><span data-stu-id="8b1e4-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b1e4-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b1e4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b1e4-121">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="8b1e4-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



