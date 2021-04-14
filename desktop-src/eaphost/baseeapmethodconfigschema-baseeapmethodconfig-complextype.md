---
title: Type complexe BaseEapMethodConfig
description: En savoir plus sur le type complexe BaseEapMethodConfig. Ce type est un élément d’espace réservé pour la configuration de la méthode.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382895"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="3ecef-105">Type complexe BaseEapMethodConfig</span><span class="sxs-lookup"><span data-stu-id="3ecef-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="3ecef-106">Le type complexe **BaseEapMethodConfig** est un élément d’espace réservé pour la configuration de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3ecef-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="3ecef-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3ecef-107">Remarks</span></span>

<span data-ttu-id="3ecef-108">La méthode EAP effectue une validation de schéma sur le contenu de l’élément **BaseEapMethodConfig** .</span><span class="sxs-lookup"><span data-stu-id="3ecef-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecef-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ecef-109">Requirements</span></span>



| <span data-ttu-id="3ecef-110">Role</span><span class="sxs-lookup"><span data-stu-id="3ecef-110">Role</span></span> | <span data-ttu-id="3ecef-111">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="3ecef-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3ecef-112">Client</span><span class="sxs-lookup"><span data-stu-id="3ecef-112">Client</span></span><br/> | <span data-ttu-id="3ecef-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ecef-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ecef-114">Serveur</span><span class="sxs-lookup"><span data-stu-id="3ecef-114">Server</span></span><br/> | <span data-ttu-id="3ecef-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ecef-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ecef-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ecef-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecef-117">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="3ecef-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3ecef-118">Schéma baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="3ecef-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





