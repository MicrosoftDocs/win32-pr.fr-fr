---
description: Définit un type d’identificateur global unique, au format de registre.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Type simple GUIDType (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865098"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="d6102-103">Type simple GUIDType (compteurs de performance)</span><span class="sxs-lookup"><span data-stu-id="d6102-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="d6102-104">Définit un type d’identificateur global unique, au format de registre.</span><span class="sxs-lookup"><span data-stu-id="d6102-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="d6102-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="d6102-105">Patterns</span></span>

<span data-ttu-id="d6102-106">Le type simple **GUIDType** est un **XS : String** qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="d6102-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="d6102-107">La valeur doit être un type d’identificateur global unique au format du Registre.</span><span class="sxs-lookup"><span data-stu-id="d6102-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="d6102-108">Par exemple, {5b2fc63a-8AF4-44cb-960C-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="d6102-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="d6102-109">Utilisez GUIDGen.exe ou UUIDGen.exe pour créer un GUID.</span><span class="sxs-lookup"><span data-stu-id="d6102-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6102-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6102-110">Requirements</span></span>



| <span data-ttu-id="d6102-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6102-111">Requirement</span></span> | <span data-ttu-id="d6102-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6102-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6102-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6102-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d6102-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6102-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6102-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6102-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d6102-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6102-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




