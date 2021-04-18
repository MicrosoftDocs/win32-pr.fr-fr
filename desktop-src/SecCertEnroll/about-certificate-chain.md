---
description: Une chaîne de certificats est une collection hiérarchique de certificats qui amène l’utilisateur final ou l’ordinateur à se retrouver à la racine de confiance, en général l’autorité de certification racine d’une organisation.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Chaîne de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522829"
---
# <a name="certificate-chain"></a><span data-ttu-id="258fc-103">Chaîne de certificats</span><span class="sxs-lookup"><span data-stu-id="258fc-103">Certificate Chain</span></span>

<span data-ttu-id="258fc-104">Une chaîne de certificats est une collection hiérarchique de certificats qui amène l’utilisateur final ou l’ordinateur à se retrouver à la racine de confiance, en général l’autorité de certification racine d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="258fc-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="258fc-105">Étant donné que toutes les parties approuvent vraisemblablement le certificat racine, un tiers peut gagner en confiance dans un certificat d’entité finale en vérifiant la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="258fc-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="258fc-106">En général, la vérification requiert l’établissement de chaque certificat dans la chaîne :</span><span class="sxs-lookup"><span data-stu-id="258fc-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="258fc-107">Est signé par la clé publique dans le certificat précédent.</span><span class="sxs-lookup"><span data-stu-id="258fc-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="258fc-108">N’a pas expiré.</span><span class="sxs-lookup"><span data-stu-id="258fc-108">Has not expired.</span></span>
-   <span data-ttu-id="258fc-109">N’a pas été révoqué.</span><span class="sxs-lookup"><span data-stu-id="258fc-109">Has not been revoked.</span></span>
-   <span data-ttu-id="258fc-110">Conforme aux stratégies spécifiées par les certificats précédents.</span><span class="sxs-lookup"><span data-stu-id="258fc-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="258fc-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="258fc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="258fc-112">Hiérarchie des certificats</span><span class="sxs-lookup"><span data-stu-id="258fc-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="258fc-113">Certification croisée</span><span class="sxs-lookup"><span data-stu-id="258fc-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="258fc-114">Modèles d’approbation</span><span class="sxs-lookup"><span data-stu-id="258fc-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



