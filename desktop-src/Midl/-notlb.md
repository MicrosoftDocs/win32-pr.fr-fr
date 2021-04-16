---
title: commutateur/notlb
description: Le commutateur/notlb empêche le compilateur MIDL de générer un fichier de bibliothèque de types (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL du commutateur/notlb
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462570"
---
# <a name="notlb-switch"></a><span data-ttu-id="0da73-104">commutateur/notlb</span><span class="sxs-lookup"><span data-stu-id="0da73-104">/notlb switch</span></span>

<span data-ttu-id="0da73-105">Le commutateur **/notlb** empêche le compilateur MIDL de générer un fichier de bibliothèque de types (TLB).</span><span class="sxs-lookup"><span data-stu-id="0da73-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="0da73-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="0da73-106">Switch Options</span></span>

<span data-ttu-id="0da73-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0da73-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da73-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0da73-108">Remarks</span></span>

<span data-ttu-id="0da73-109">Par défaut, le compilateur MIDL génère un fichier TLB chaque fois qu’il rencontre une instruction [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="0da73-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="0da73-110">Ce commutateur remplace le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="0da73-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="0da73-111">Quand l’option **/notlb** est spécifiée, tous les autres stubs, en-têtes, etc. sont générés comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="0da73-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="0da73-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da73-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da73-113">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="0da73-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




