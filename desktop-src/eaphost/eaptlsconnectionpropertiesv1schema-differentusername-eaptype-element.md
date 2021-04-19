---
title: Élément DifferentUsername (EapType)
description: En savoir plus sur l’élément DifferentUsername (EapType). Cet élément détermine le nom d’utilisateur EAP-TLS à utiliser.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Élément DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513558"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="0e2b6-105">Élément DifferentUsername (EapType)</span><span class="sxs-lookup"><span data-stu-id="0e2b6-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="0e2b6-106">L’élément **DifferentUsername (EapType)** détermine le nom d’utilisateur EAP-TLS à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="0e2b6-107">L’élément **DifferentUsername** est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2b6-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e2b6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0e2b6-108">Remarks</span></span>

<span data-ttu-id="0e2b6-109">Si l’élément **DifferentUserName** a la valeur true, EAP-TLS doit utiliser un nom d’utilisateur différent du nom qui s’affiche sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="0e2b6-110">Si l’élément **DifferentUserName** a la valeur false, EAP-TLS utilise le nom d’utilisateur qui apparaît sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="0e2b6-111">L’élément **DifferentUserName** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2b6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e2b6-112">Requirements</span></span>



| <span data-ttu-id="0e2b6-113">Role</span><span class="sxs-lookup"><span data-stu-id="0e2b6-113">Role</span></span> | <span data-ttu-id="0e2b6-114">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="0e2b6-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="0e2b6-115">Client</span><span class="sxs-lookup"><span data-stu-id="0e2b6-115">Client</span></span><br/> | <span data-ttu-id="0e2b6-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2b6-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e2b6-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="0e2b6-117">Server</span></span><br/> | <span data-ttu-id="0e2b6-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e2b6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e2b6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e2b6-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e2b6-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="0e2b6-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0e2b6-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="0e2b6-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="0e2b6-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="0e2b6-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0e2b6-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="0e2b6-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="0e2b6-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0e2b6-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="0e2b6-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="0e2b6-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0e2b6-126">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0e2b6-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0e2b6-127">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0e2b6-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





