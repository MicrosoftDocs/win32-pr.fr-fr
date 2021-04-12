---
title: Élément RequireCryptoBinding (EapType)
description: Indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Élément RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385084"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="e57c5-104">Élément RequireCryptoBinding (EapType)</span><span class="sxs-lookup"><span data-stu-id="e57c5-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="e57c5-105">L’élément **RequireCryptoBinding (EapType)** indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.</span><span class="sxs-lookup"><span data-stu-id="e57c5-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="e57c5-106">L’élément **RequireCryptoBinding** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e57c5-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e57c5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e57c5-107">Remarks</span></span>

<span data-ttu-id="e57c5-108">Si l’élément **RequireCryptoBinding** a la valeur true, PEAP s’authentifie auprès des serveurs qui ne prennent pas en charge TLV ; Si la valeur est FALSe, PEAP s’authentifie uniquement avec les serveurs qui prennent en charge TLV.</span><span class="sxs-lookup"><span data-stu-id="e57c5-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="e57c5-109">L’élément **RequireCryptoBinding** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e57c5-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57c5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e57c5-110">Requirements</span></span>



| <span data-ttu-id="e57c5-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e57c5-111">Requirement</span></span> | <span data-ttu-id="e57c5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e57c5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e57c5-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e57c5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e57c5-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e57c5-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e57c5-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e57c5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e57c5-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e57c5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e57c5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e57c5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e57c5-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="e57c5-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e57c5-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e57c5-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e57c5-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="e57c5-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e57c5-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e57c5-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e57c5-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e57c5-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e57c5-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="e57c5-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e57c5-124">Schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e57c5-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e57c5-125">Éléments de schéma mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e57c5-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





