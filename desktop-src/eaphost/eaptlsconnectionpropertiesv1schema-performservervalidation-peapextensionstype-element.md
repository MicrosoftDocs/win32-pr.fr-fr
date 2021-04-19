---
title: PerformServerValidation (EapType)
description: En savoir plus sur l’élément PerformServerValidation. Cet élément indique si la validation du serveur est effectuée. | PerformServerValidation (EapType)
ms.assetid: f6233bff-18e4-45b4-b598-839fa198f676
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655379676bd117b89a6fe41a8d6895260e71a2bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532400"
---
# <a name="performservervalidation-eaptype"></a><span data-ttu-id="07f4a-106">PerformServerValidation (EapType)</span><span class="sxs-lookup"><span data-stu-id="07f4a-106">PerformServerValidation (EapType)</span></span>

<span data-ttu-id="07f4a-107">L’élément **PerformServerValidation (EapType)** indique si la validation du serveur est effectuée.</span><span class="sxs-lookup"><span data-stu-id="07f4a-107">The **PerformServerValidation (EapType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS:PerformServerValidation "
 />
```

<span data-ttu-id="07f4a-108">L’élément est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="07f4a-108">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f4a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="07f4a-109">Remarks</span></span>

<span data-ttu-id="07f4a-110">L’élément **PerformServerValidation** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="07f4a-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f4a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07f4a-111">Requirements</span></span>



| <span data-ttu-id="07f4a-112">Role</span><span class="sxs-lookup"><span data-stu-id="07f4a-112">Role</span></span> | <span data-ttu-id="07f4a-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="07f4a-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="07f4a-114">Client</span><span class="sxs-lookup"><span data-stu-id="07f4a-114">Client</span></span><br/> | <span data-ttu-id="07f4a-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07f4a-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="07f4a-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="07f4a-116">Server</span></span><br/> | <span data-ttu-id="07f4a-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07f4a-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07f4a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07f4a-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="07f4a-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="07f4a-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="07f4a-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="07f4a-120">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="07f4a-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="07f4a-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="07f4a-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="07f4a-122">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="07f4a-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="07f4a-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="07f4a-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="07f4a-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="07f4a-125">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="07f4a-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="07f4a-126">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="07f4a-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="07f4a-127">**PerformServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="07f4a-127">**PerformServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv2shema-tlsextensions-tlsextensionstype-element.md)
</dt> </dl>

 

 





