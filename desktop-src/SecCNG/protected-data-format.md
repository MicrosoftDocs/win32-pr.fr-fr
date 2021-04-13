---
description: Les données protégées sont stockées sous la forme d’un objet BLOB encodé ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Format de données protégées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115183"
---
# <a name="protected-data-format"></a><span data-ttu-id="b1906-103">Format de données protégées</span><span class="sxs-lookup"><span data-stu-id="b1906-103">Protected Data Format</span></span>

<span data-ttu-id="b1906-104">Les données protégées sont stockées sous la forme d’un objet BLOB encodé ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="b1906-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="b1906-105">Les données sont mises en forme en tant que contenu associé à CMS (Certificate Message Syntax).</span><span class="sxs-lookup"><span data-stu-id="b1906-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="b1906-106">L’enveloppe numérique contient du contenu chiffré, des informations de destinataire qui contiennent une clé de chiffrement de contenu chiffrée (clé CEK) et un en-tête qui contient des informations sur le contenu, y compris la chaîne de règle du descripteur de protection non chiffré.</span><span class="sxs-lookup"><span data-stu-id="b1906-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="b1906-107">Cela est illustré par le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b1906-107">This is shown by the following diagram.</span></span>

![données enveloppées protégées](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="b1906-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1906-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1906-110">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="b1906-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="b1906-111">Descripteurs de protection</span><span class="sxs-lookup"><span data-stu-id="b1906-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="b1906-112">Fournisseurs de protection</span><span class="sxs-lookup"><span data-stu-id="b1906-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



