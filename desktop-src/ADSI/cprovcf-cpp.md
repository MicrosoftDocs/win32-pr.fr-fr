---
title: CPROVCF. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461994"
---
# <a name="cprovcfcpp"></a><span data-ttu-id="947ab-103">CPROVCF. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="947ab-103">CPROVCF.CPP</span></span>

<span data-ttu-id="947ab-104">Dans l’exemple de composant fournisseur, un exemple de code du code de fabrique de classe d’objet du fournisseur ADs se trouve dans cprovcf. cpp.</span><span class="sxs-lookup"><span data-stu-id="947ab-104">In the example provider component, one code example of the ADs provider object class factory code is in cprovcf.cpp.</span></span> <span data-ttu-id="947ab-105">Le composant fournisseur ne crée jamais directement une instance de cet objet à un moment autre que lorsque l’objet est créé automatiquement pendant les opérations de liaison dans [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou dans la fonction interne de la méthode Visual Basic **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="947ab-105">The provider component never directly creates an instance of this object at any time other than when the object is created automatically during the binding operations in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or the internal function in the Visual Basic method **GetObject**.</span></span> <span data-ttu-id="947ab-106">La méthode prise en charge est présentée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="947ab-106">The supported method is listed in the following table.</span></span>



| <span data-ttu-id="947ab-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="947ab-107">Method</span></span>                                  | <span data-ttu-id="947ab-108">Description</span><span class="sxs-lookup"><span data-stu-id="947ab-108">Description</span></span>                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="947ab-109">**CSampleDSProviderCF :: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="947ab-109">**CSampleDSProviderCF::CreateInstance**</span></span> | <span data-ttu-id="947ab-110">Crée une instance de la fabrique de classes pour l’objet fournisseur ADS.</span><span class="sxs-lookup"><span data-stu-id="947ab-110">Creates an instance of the class factory for the ADS provider object.</span></span> |



 

 

 




