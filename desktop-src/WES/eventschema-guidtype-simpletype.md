---
title: Type simple GUIDType (schéma d’événement)
description: Définit un type d’identificateur global unique, au format de registre. | Type simple GUIDType (schéma d’événement)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Journal des types simples GUIDType
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07635bc43ff07d65eee5f32786818ca7dad8dd64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322085"
---
# <a name="guidtype-simple-type-event-schema"></a><span data-ttu-id="7983c-105">Type simple GUIDType (schéma d’événement)</span><span class="sxs-lookup"><span data-stu-id="7983c-105">GUIDType simple type (Event Schema)</span></span>

<span data-ttu-id="7983c-106">Définit un type d’identificateur global unique, au format de registre.</span><span class="sxs-lookup"><span data-stu-id="7983c-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7983c-107">Modèles</span><span class="sxs-lookup"><span data-stu-id="7983c-107">Patterns</span></span>

<span data-ttu-id="7983c-108">Le type simple **GUIDType** est une chaîne qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="7983c-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="7983c-109">La valeur doit être un type d’identificateur global unique au format du Registre.</span><span class="sxs-lookup"><span data-stu-id="7983c-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="7983c-110">Par exemple, {5b2fc63a-8AF4-44cb-960C-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="7983c-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="7983c-111">Utilisez GUIDGen.exe ou UUIDGen.exe pour créer un GUID.</span><span class="sxs-lookup"><span data-stu-id="7983c-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="7983c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7983c-112">Requirements</span></span>



| <span data-ttu-id="7983c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7983c-113">Requirement</span></span> | <span data-ttu-id="7983c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7983c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7983c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7983c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7983c-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7983c-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7983c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7983c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7983c-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7983c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





