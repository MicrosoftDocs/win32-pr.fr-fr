---
title: Élément config (EapHostConfig)
description: Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Élément config EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465610"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="8cddb-104">Élément config (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="8cddb-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="8cddb-105">L’élément **config (EapHostConfig)** est utilisé lorsque la configuration de la méthode est au format texte XML et non pas dans un objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="8cddb-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="8cddb-106">L’élément **config** est défini par l’élément [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8cddb-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cddb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8cddb-107">Remarks</span></span>

<span data-ttu-id="8cddb-108">Les éléments **config** et [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="8cddb-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cddb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cddb-109">Requirements</span></span>



| <span data-ttu-id="8cddb-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cddb-110">Requirement</span></span> | <span data-ttu-id="8cddb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cddb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cddb-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cddb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8cddb-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cddb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cddb-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cddb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8cddb-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cddb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cddb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cddb-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="8cddb-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="8cddb-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8cddb-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="8cddb-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="8cddb-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="8cddb-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8cddb-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="8cddb-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="8cddb-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="8cddb-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8cddb-122">Schéma eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="8cddb-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





