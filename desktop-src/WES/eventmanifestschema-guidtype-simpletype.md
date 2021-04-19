---
title: Type simple GUIDType (schéma EventManifest)
description: Définit un type d’identificateur global unique, au format de registre. | Type simple GUIDType (schéma EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
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
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532411"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="afcc6-105">Type simple GUIDType (schéma EventManifest)</span><span class="sxs-lookup"><span data-stu-id="afcc6-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="afcc6-106">Définit un type d’identificateur global unique, au format de registre.</span><span class="sxs-lookup"><span data-stu-id="afcc6-106">Defines a globally unique identifier type, in Registry format.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="afcc6-107">Modèles</span><span class="sxs-lookup"><span data-stu-id="afcc6-107">Patterns</span></span>

<span data-ttu-id="afcc6-108">Le type simple **GUIDType** est une chaîne qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="afcc6-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="afcc6-109">La valeur doit être un type d’identificateur global unique au format du Registre.</span><span class="sxs-lookup"><span data-stu-id="afcc6-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="afcc6-110">Par exemple, {5b2fc63a-8AF4-44cb-960C-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="afcc6-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="afcc6-111">Utilisez GUIDGen.exe ou UUIDGen.exe pour créer un GUID.</span><span class="sxs-lookup"><span data-stu-id="afcc6-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="afcc6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afcc6-112">Requirements</span></span>



| <span data-ttu-id="afcc6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afcc6-113">Requirement</span></span> | <span data-ttu-id="afcc6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="afcc6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="afcc6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afcc6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="afcc6-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afcc6-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="afcc6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afcc6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="afcc6-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afcc6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





