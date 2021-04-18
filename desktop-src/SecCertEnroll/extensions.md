---
description: Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions (API d’inscription de certificat)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536179"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="92dcd-103">Extensions (API d’inscription de certificat)</span><span class="sxs-lookup"><span data-stu-id="92dcd-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="92dcd-104">Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat.</span><span class="sxs-lookup"><span data-stu-id="92dcd-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="92dcd-105">Les extensions fournissent des informations améliorées sur l’utilisation de la clé, les stratégies de certificat et les contraintes, les autres formats de nom, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="92dcd-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="92dcd-106">Vous pouvez utiliser l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) pour définir une valeur d’extension.</span><span class="sxs-lookup"><span data-stu-id="92dcd-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="92dcd-107">La plupart des extensions courantes peuvent être créées à l’aide d’interfaces prédéfinies dérivées de **IX509Extension**.</span><span class="sxs-lookup"><span data-stu-id="92dcd-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="92dcd-108">Une collection d’extensions est ajoutée à une demande de certificat en incluant la collection dans les attributs de la demande.</span><span class="sxs-lookup"><span data-stu-id="92dcd-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="92dcd-109">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="92dcd-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="92dcd-110">Extensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="92dcd-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="92dcd-111">\#Extensions PKCS 10</span><span class="sxs-lookup"><span data-stu-id="92dcd-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="92dcd-112">Extensions CMC</span><span class="sxs-lookup"><span data-stu-id="92dcd-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



