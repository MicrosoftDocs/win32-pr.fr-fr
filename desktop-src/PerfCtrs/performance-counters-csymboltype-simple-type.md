---
description: Définit un nom de symbole C/C++ valide.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Type simple CSymbolType (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952002"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="2bdcf-103">Type simple CSymbolType (compteurs de performance)</span><span class="sxs-lookup"><span data-stu-id="2bdcf-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="2bdcf-104">Définit un nom de symbole C/C++ valide.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="2bdcf-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="2bdcf-105">Patterns</span></span>

<span data-ttu-id="2bdcf-106">Le type simple **CSymbolType** est un **XS : String** qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="2bdcf-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="2bdcf-107">Le nom du symbole peut être vide ou contenir des caractères alphanumériques et des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="2bdcf-108">Si vous spécifiez un nom, le nom doit commencer par un trait de soulignement ( \_ ) ou par un caractère alphabétique.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdcf-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bdcf-109">Requirements</span></span>



| <span data-ttu-id="2bdcf-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bdcf-110">Requirement</span></span> | <span data-ttu-id="2bdcf-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bdcf-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bdcf-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bdcf-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdcf-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bdcf-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2bdcf-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bdcf-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdcf-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bdcf-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




