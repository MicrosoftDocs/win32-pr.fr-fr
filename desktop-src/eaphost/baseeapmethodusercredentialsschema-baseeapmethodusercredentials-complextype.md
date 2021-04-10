---
title: Type complexe BaseEapMethodUserCredentials
description: En savoir plus sur le type complexe BaseEapMethodUserCredentials. Ce type est un élément d’espace réservé pour les données d’informations d’identification de méthode.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730180"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="fd098-105">Type complexe BaseEapMethodUserCredentials</span><span class="sxs-lookup"><span data-stu-id="fd098-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="fd098-106">Le type complexe **BaseEapMethodUserCredentials** est un élément d’espace réservé pour les données d’informations d’identification de méthode.</span><span class="sxs-lookup"><span data-stu-id="fd098-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
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

## <a name="remarks"></a><span data-ttu-id="fd098-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fd098-107">Remarks</span></span>

<span data-ttu-id="fd098-108">La méthode EAP effectue une validation de schéma sur le contenu de **BaseEapMethodUserCredentials**.</span><span class="sxs-lookup"><span data-stu-id="fd098-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd098-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd098-109">Requirements</span></span>



| <span data-ttu-id="fd098-110">Role</span><span class="sxs-lookup"><span data-stu-id="fd098-110">Role</span></span> | <span data-ttu-id="fd098-111">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="fd098-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="fd098-112">Client</span><span class="sxs-lookup"><span data-stu-id="fd098-112">Client</span></span><br/> | <span data-ttu-id="fd098-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd098-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd098-114">Serveur</span><span class="sxs-lookup"><span data-stu-id="fd098-114">Server</span></span><br/> | <span data-ttu-id="fd098-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd098-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd098-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd098-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd098-117">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="fd098-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fd098-118">Schéma baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="fd098-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





