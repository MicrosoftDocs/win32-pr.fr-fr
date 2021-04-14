---
title: Élément type (EapMethodType)
description: En savoir plus sur l’élément type (EapMethodType), qui fait référence au type de méthode EAP. Consultez spécifications et afficher les ressources disponibles supplémentaires.
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Élément type EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382864"
---
# <a name="type-eapmethodtype-element"></a><span data-ttu-id="48f3b-105">Élément type (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="48f3b-105">Type (EapMethodType) Element</span></span>

<span data-ttu-id="48f3b-106">L’élément **type (EapMethodType)** fait référence au type de méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="48f3b-106">The **Type (EapMethodType)** element refers to the EAP method type.</span></span>

<span data-ttu-id="48f3b-107">Le type est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="48f3b-107">The Type is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

<span data-ttu-id="48f3b-108">L’élément **type** est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="48f3b-108">The **Type** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f3b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48f3b-109">Requirements</span></span>



| <span data-ttu-id="48f3b-110">Role</span><span class="sxs-lookup"><span data-stu-id="48f3b-110">Role</span></span> | <span data-ttu-id="48f3b-111">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="48f3b-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="48f3b-112">Client</span><span class="sxs-lookup"><span data-stu-id="48f3b-112">Client</span></span><br/> | <span data-ttu-id="48f3b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48f3b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48f3b-114">Serveur</span><span class="sxs-lookup"><span data-stu-id="48f3b-114">Server</span></span><br/> | <span data-ttu-id="48f3b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48f3b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48f3b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48f3b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="48f3b-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="48f3b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="48f3b-118">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="48f3b-118">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="48f3b-119">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="48f3b-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="48f3b-120">Schéma eapcommon</span><span class="sxs-lookup"><span data-stu-id="48f3b-120">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





