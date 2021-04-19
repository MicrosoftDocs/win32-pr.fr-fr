---
title: Mappage du code d’Visual Basic ADSI au code C++
description: ADSI est constitué de plus de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510385"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="40554-103">Mappage du code d’Visual Basic ADSI au code C++</span><span class="sxs-lookup"><span data-stu-id="40554-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="40554-104">ADSI est constitué de plus de 50 interfaces.</span><span class="sxs-lookup"><span data-stu-id="40554-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="40554-105">La plupart des opérations d’annuaire peuvent être effectuées à l’aide de cinq interfaces uniquement.</span><span class="sxs-lookup"><span data-stu-id="40554-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="40554-106">Les voici :</span><span class="sxs-lookup"><span data-stu-id="40554-106">They are:</span></span>

-   [<span data-ttu-id="40554-107">**IADsOpenDSObject**</span><span class="sxs-lookup"><span data-stu-id="40554-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="40554-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="40554-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="40554-109">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="40554-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="40554-110">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="40554-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="40554-111">**Rubrique IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="40554-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="40554-112">Le tableau suivant répertorie les mappages du code ADSI VB/VBS au code C++.</span><span class="sxs-lookup"><span data-stu-id="40554-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="40554-113">N’oubliez pas qu’il ne s’agit pas d’une liste complète.</span><span class="sxs-lookup"><span data-stu-id="40554-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="40554-114">Code VBS</span><span class="sxs-lookup"><span data-stu-id="40554-114">VBS Code</span></span>                           | <span data-ttu-id="40554-115">Code VC</span><span class="sxs-lookup"><span data-stu-id="40554-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="40554-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="40554-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="40554-117">HR = AdsGetObject ()</span><span class="sxs-lookup"><span data-stu-id="40554-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="40554-118">obj. Placez obj. Obtient obj. Parent</span><span class="sxs-lookup"><span data-stu-id="40554-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="40554-119">IADs ou IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="40554-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="40554-120">obj. Créez un obj. Supprimez obj. MoveHere</span><span class="sxs-lookup"><span data-stu-id="40554-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="40554-121">IADsContainer</span><span class="sxs-lookup"><span data-stu-id="40554-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="40554-122">For each...</span><span class="sxs-lookup"><span data-stu-id="40554-122">For each…</span></span> <span data-ttu-id="40554-123">dans...</span><span class="sxs-lookup"><span data-stu-id="40554-123">in…</span></span>                      | <span data-ttu-id="40554-124">AdsBuildEnumerator() ADsEnumerateNext()</span><span class="sxs-lookup"><span data-stu-id="40554-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="40554-125">Connexion, commande, Recordset</span><span class="sxs-lookup"><span data-stu-id="40554-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="40554-126">Rubrique IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="40554-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="40554-127">Descripteur de sécurité, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="40554-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="40554-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="40554-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




