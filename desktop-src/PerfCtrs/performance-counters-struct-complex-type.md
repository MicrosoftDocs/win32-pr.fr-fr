---
description: Définit une structure qui contient une ou plusieurs valeurs de compteur.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Type complexe struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517853"
---
# <a name="struct-complex-type"></a><span data-ttu-id="ff283-103">Type complexe struct</span><span class="sxs-lookup"><span data-stu-id="ff283-103">struct Complex Type</span></span>

<span data-ttu-id="ff283-104">Définit une structure qui contient une ou plusieurs valeurs de compteur.</span><span class="sxs-lookup"><span data-stu-id="ff283-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="ff283-105">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff283-105">Attributes</span></span>



| <span data-ttu-id="ff283-106">Nom</span><span class="sxs-lookup"><span data-stu-id="ff283-106">Name</span></span> | <span data-ttu-id="ff283-107">Type</span><span class="sxs-lookup"><span data-stu-id="ff283-107">Type</span></span>                                                                    | <span data-ttu-id="ff283-108">Description</span><span class="sxs-lookup"><span data-stu-id="ff283-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff283-109">name</span><span class="sxs-lookup"><span data-stu-id="ff283-109">name</span></span> | [<span data-ttu-id="ff283-110">**homme : CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="ff283-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="ff283-111">Nom de la structure.</span><span class="sxs-lookup"><span data-stu-id="ff283-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ff283-112">type</span><span class="sxs-lookup"><span data-stu-id="ff283-112">type</span></span> | [<span data-ttu-id="ff283-113">**homme : CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="ff283-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="ff283-114">Nom symbolique qui identifie la structure.</span><span class="sxs-lookup"><span data-stu-id="ff283-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="ff283-115">L’outil [CTRPP](ctrpp.md) crée une variable de struct portant ce nom que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff283-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff283-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff283-116">Requirements</span></span>



| <span data-ttu-id="ff283-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff283-117">Requirement</span></span> | <span data-ttu-id="ff283-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff283-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff283-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff283-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff283-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff283-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff283-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff283-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff283-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff283-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




