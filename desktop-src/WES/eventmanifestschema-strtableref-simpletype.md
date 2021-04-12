---
title: Type simple strTableRef
description: Définit une chaîne qui fait référence à une chaîne de message définie dans une table de chaînes du manifeste ou dans un fichier de message (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Journal des types simples strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508722"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="b7fe4-104">Type simple strTableRef</span><span class="sxs-lookup"><span data-stu-id="b7fe4-104">strTableRef Simple Type</span></span>

<span data-ttu-id="b7fe4-105">Définit une chaîne qui fait référence à une chaîne de message définie dans une table de chaînes du manifeste ou dans un fichier de message (. MC).</span><span class="sxs-lookup"><span data-stu-id="b7fe4-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="b7fe4-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="b7fe4-106">Patterns</span></span>

<span data-ttu-id="b7fe4-107">Le type simple **strTableRef** est un **XS : String** qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="b7fe4-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="b7fe4-108">La chaîne doit se présenter sous la forme $string. *stringid* ou $MC.*symbolid*.</span><span class="sxs-lookup"><span data-stu-id="b7fe4-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="b7fe4-109">Si la chaîne se présente sous la forme, $string. *stringid*, il doit référencer une chaîne dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="b7fe4-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="b7fe4-110">Si la chaîne se présente sous la forme $mc.*symbolid*, elle doit faire référence à un symbole défini dans le fichier de message.</span><span class="sxs-lookup"><span data-stu-id="b7fe4-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7fe4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7fe4-111">Requirements</span></span>



| <span data-ttu-id="b7fe4-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7fe4-112">Requirement</span></span> | <span data-ttu-id="b7fe4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7fe4-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b7fe4-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fe4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b7fe4-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7fe4-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b7fe4-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fe4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b7fe4-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7fe4-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





