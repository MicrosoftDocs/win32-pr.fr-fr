---
title: Élément ConfigBlob (EapHostConfig)
description: Est utilisé lorsque la configuration de la méthode est sous forme d’objet BLOB binaire plutôt que sous forme de chaîne de texte.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Élément ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739693"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="388d9-104">Élément ConfigBlob (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="388d9-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="388d9-105">L’élément **ConfigBlob (EapHostConfig)** est utilisé lorsque la configuration de la méthode est sous forme d’objet blob binaire plutôt que sous forme de chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="388d9-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="388d9-106">L’élément **ConfigBlob** est défini par l’élément [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="388d9-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="388d9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="388d9-107">Remarks</span></span>

<span data-ttu-id="388d9-108">Les éléments [**config**](eaphostconfigschema-config-eaphostconfig-element.md) et **ConfigBlob** ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="388d9-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="388d9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="388d9-109">Requirements</span></span>



| <span data-ttu-id="388d9-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="388d9-110">Requirement</span></span> | <span data-ttu-id="388d9-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="388d9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="388d9-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="388d9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="388d9-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="388d9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="388d9-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="388d9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="388d9-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="388d9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="388d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="388d9-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="388d9-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="388d9-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="388d9-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="388d9-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="388d9-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="388d9-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="388d9-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="388d9-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="388d9-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="388d9-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="388d9-122">Schéma eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="388d9-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





