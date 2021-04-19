---
title: Type simple CSymbolType (Journal des événements Windows)
description: Définit un nom de symbole C/C++ valide.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Journal des types simples CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539010"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="76848-104">Type simple CSymbolType (Journal des événements Windows)</span><span class="sxs-lookup"><span data-stu-id="76848-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="76848-105">Définit un nom de symbole C/C++ valide.</span><span class="sxs-lookup"><span data-stu-id="76848-105">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="76848-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="76848-106">Patterns</span></span>

<span data-ttu-id="76848-107">Le type simple **CSymbolType** est un **XS : String** qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="76848-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="76848-108">Le nom du symbole peut être vide ou contenir des caractères alphanumériques et des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="76848-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="76848-109">Si le nom est vide, le compilateur de message génère le nom du symbole.</span><span class="sxs-lookup"><span data-stu-id="76848-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="76848-110">Si vous spécifiez un nom, le nom doit commencer par un trait de soulignement ( \_ ) ou par un caractère alphabétique.</span><span class="sxs-lookup"><span data-stu-id="76848-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="76848-111">Notes</span><span class="sxs-lookup"><span data-stu-id="76848-111">Remarks</span></span>

<span data-ttu-id="76848-112">Si le nom du symbole est vide, le compilateur de message utilise l’attribut **Name** de l’élément que vous définissez pour générer le nom du symbole.</span><span class="sxs-lookup"><span data-stu-id="76848-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="76848-113">Le compilateur remplace tous les caractères non alphanumériques par des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="76848-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="76848-114">Par exemple, si l’attribut **Name** du canal est Microsoft-Windows-SampleProvider/Operational, le compilateur utilise Microsoft \_ Windows \_ SampleProvider \_ Operational comme nom de symbole.</span><span class="sxs-lookup"><span data-stu-id="76848-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="76848-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76848-115">Requirements</span></span>



| <span data-ttu-id="76848-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76848-116">Requirement</span></span> | <span data-ttu-id="76848-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="76848-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="76848-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76848-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76848-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76848-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="76848-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76848-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76848-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76848-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





