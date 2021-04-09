---
description: La bibliothèque de Xenroll.dll a été supprimée du système d’exploitation et remplacée par CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mappage de Xenroll.dll à CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758061"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="55480-103">Mappage de Xenroll.dll à CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="55480-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="55480-104">Avant Windows Vista, le contrôle d’inscription de certificat était implémenté dans Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="55480-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="55480-105">La bibliothèque de Xenroll.dll a été supprimée du système d’exploitation et remplacée par CertEnroll.dll.</span><span class="sxs-lookup"><span data-stu-id="55480-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="55480-106">Xenroll a tenté d’implémenter deux jeux d’interfaces parallèles.</span><span class="sxs-lookup"><span data-stu-id="55480-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="55480-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)et [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) étaient conformes à Automation et compatibles avec les langages de script.</span><span class="sxs-lookup"><span data-stu-id="55480-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="55480-108">Les interfaces correspondantes ([**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)et [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)) n’ont pas pu être scriptées, mais étaient plus pratiques pour les programmeurs C++.</span><span class="sxs-lookup"><span data-stu-id="55480-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="55480-109">Au fur et à mesure qu’elles ont évolué, les deux jeux d’interfaces n’étaient pas synchronisés.</span><span class="sxs-lookup"><span data-stu-id="55480-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="55480-110">En particulier, l’ensemble des interfaces doubles représentées par **ICEnroll4** ne définit qu’un sous-ensemble des fonctionnalités définies par **IEnroll4**.</span><span class="sxs-lookup"><span data-stu-id="55480-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="55480-111">CertEnroll.dll implémente un ensemble plus étendu et plus structuré d’interfaces COM conformes à Automation.</span><span class="sxs-lookup"><span data-stu-id="55480-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="55480-112">Les rubriques suivantes expliquent comment Xenroll.dll est mappé à CertEnroll.dll pour différents types de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="55480-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="55480-113">Fonctions de demande de certificat</span><span class="sxs-lookup"><span data-stu-id="55480-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="55480-114">Fonctions de réponse de certificat</span><span class="sxs-lookup"><span data-stu-id="55480-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="55480-115">Fonctions d’attribut</span><span class="sxs-lookup"><span data-stu-id="55480-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="55480-116">Fonctions d’extension</span><span class="sxs-lookup"><span data-stu-id="55480-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="55480-117">Fonctions de propriété externes</span><span class="sxs-lookup"><span data-stu-id="55480-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="55480-118">Fonctions de clés privées et publiques</span><span class="sxs-lookup"><span data-stu-id="55480-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="55480-119">Fonctions du fournisseur de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="55480-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="55480-120">Fonctions du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="55480-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="55480-121">Fonctions d’échange d’informations personnelles</span><span class="sxs-lookup"><span data-stu-id="55480-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="55480-122">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="55480-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="55480-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55480-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55480-124">Utilisation de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="55480-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
