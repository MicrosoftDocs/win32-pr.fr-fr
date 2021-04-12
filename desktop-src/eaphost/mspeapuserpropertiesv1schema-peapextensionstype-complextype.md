---
title: Type complexe PeapExtensionsType (propriétés de connexion)
description: En savoir plus sur le type complexe PeapExtensionsType. Ce type active les améliorations futures du schéma.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType type complexe EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316487"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="3700b-105">Type complexe PeapExtensionsType (propriétés de connexion)</span><span class="sxs-lookup"><span data-stu-id="3700b-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="3700b-106">Le type complexe **PeapExtensionsType** permet de futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="3700b-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="3700b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3700b-107">Remarks</span></span>

<span data-ttu-id="3700b-108">Le type complexe **PeapExtensionsType** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="3700b-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3700b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3700b-109">Requirements</span></span>



| <span data-ttu-id="3700b-110">Role</span><span class="sxs-lookup"><span data-stu-id="3700b-110">Role</span></span> | <span data-ttu-id="3700b-111">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="3700b-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3700b-112">Client</span><span class="sxs-lookup"><span data-stu-id="3700b-112">Client</span></span><br/> | <span data-ttu-id="3700b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3700b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3700b-114">Serveur</span><span class="sxs-lookup"><span data-stu-id="3700b-114">Server</span></span><br/> | <span data-ttu-id="3700b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3700b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3700b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3700b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3700b-117">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="3700b-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3700b-118">Schéma mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3700b-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





