---
title: TLSExtensions (schéma v1)
description: En savoir plus sur l’élément TLSExtensions (EapType). Cet élément active les améliorations futures du schéma.
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510709"
---
# <a name="tlsextensions-v1-schema"></a><span data-ttu-id="3f3b4-105">TLSExtensions (schéma v1)</span><span class="sxs-lookup"><span data-stu-id="3f3b4-105">TLSExtensions (v1 schema)</span></span>

<span data-ttu-id="3f3b4-106">L’élément **TLSExtensions (EapType)** permet de futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-106">The **TLSExtensions (EapType)** element enables future enhancements to the schema.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

<span data-ttu-id="3f3b4-107">L’élément est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3b4-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3b4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3f3b4-108">Remarks</span></span>

<span data-ttu-id="3f3b4-109">L’élément **TLSExtensions** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="3f3b4-109">The **TLSExtensions** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3b4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f3b4-110">Requirements</span></span>



| <span data-ttu-id="3f3b4-111">Role</span><span class="sxs-lookup"><span data-stu-id="3f3b4-111">Role</span></span> | <span data-ttu-id="3f3b4-112">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="3f3b4-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3f3b4-113">Client</span><span class="sxs-lookup"><span data-stu-id="3f3b4-113">Client</span></span><br/> | <span data-ttu-id="3f3b4-114">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f3b4-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3f3b4-115">Serveur</span><span class="sxs-lookup"><span data-stu-id="3f3b4-115">Server</span></span><br/> | <span data-ttu-id="3f3b4-116">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f3b4-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f3b4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f3b4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f3b4-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="3f3b4-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3f3b4-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="3f3b4-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="3f3b4-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="3f3b4-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3f3b4-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="3f3b4-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="3f3b4-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3f3b4-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3f3b4-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="3f3b4-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3f3b4-124">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3f3b4-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3f3b4-125">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3f3b4-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3f3b4-126">**TLSExtensions (TLSExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="3f3b4-126">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





