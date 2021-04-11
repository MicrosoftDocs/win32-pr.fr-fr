---
description: La certification croisée permet aux entités d’une infrastructure à clé publique (PKI) d’approuver les entités d’une autre infrastructure à clé publique.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certification croisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203998"
---
# <a name="cross-certification"></a><span data-ttu-id="60756-103">Certification croisée</span><span class="sxs-lookup"><span data-stu-id="60756-103">Cross Certification</span></span>

<span data-ttu-id="60756-104">La certification croisée permet aux entités d’une infrastructure à clé publique (PKI) d’approuver les entités d’une autre infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="60756-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="60756-105">Cette relation d’approbation mutuelle est généralement prise en charge par un accord de certification croisée entre les autorités de certification (ca) de chaque infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="60756-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="60756-106">L’accord établit les responsabilités et la responsabilité de chaque partie.</span><span class="sxs-lookup"><span data-stu-id="60756-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="60756-107">Une relation d’approbation mutuelle entre deux autorités de certification requiert que chaque autorité de certification émette un certificat à l’autre pour établir la relation dans les deux directions.</span><span class="sxs-lookup"><span data-stu-id="60756-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="60756-108">Le chemin d’accès de l’approbation n’est pas hiérarchique (aucune des autorités de certification gouvernementales n’est subordonnée à l’autre), bien que les infrastructures à clé publique distinctes soient des hiérarchies de certificats.</span><span class="sxs-lookup"><span data-stu-id="60756-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="60756-109">Une fois que deux autorités de certification ont établi et spécifié les conditions de confiance et les certificats émis entre eux, les entités dans les infrastructures à clé publique distinctes peuvent interagir selon les stratégies spécifiées dans les certificats.</span><span class="sxs-lookup"><span data-stu-id="60756-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![diagramme de certification croisée](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="60756-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60756-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60756-112">Modèles d’approbation</span><span class="sxs-lookup"><span data-stu-id="60756-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



