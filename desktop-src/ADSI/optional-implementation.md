---
title: Implémentation facultative
description: Les fonctionnalités suivantes sont facultatives, mais recommandées
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implémentation facultative d’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507027"
---
# <a name="optional-implementation"></a><span data-ttu-id="4db92-104">Implémentation facultative</span><span class="sxs-lookup"><span data-stu-id="4db92-104">Optional Implementation</span></span>

<span data-ttu-id="4db92-105">Les fonctionnalités suivantes sont facultatives, mais recommandées :</span><span class="sxs-lookup"><span data-stu-id="4db92-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="4db92-106">Interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour les clients non-Automation.</span><span class="sxs-lookup"><span data-stu-id="4db92-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="4db92-107">Étant donné que le fournisseur d’OLE DB ADSI utilise **IDirectorySearch** pour présenter des requêtes et collecter les résultats du service d’annuaire sous-jacent, les fournisseurs qui implémentent cette interface fournissent automatiquement l’accès aux bases de données de style OLE DB sans avoir à implémenter d’interfaces supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4db92-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="4db92-108">Interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="4db92-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="4db92-109">Les fournisseurs de services d’annuaire qui prennent en charge la sécurité des objets basés sur les listes de contrôle d’accès sont encouragés à implémenter ces fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4db92-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




