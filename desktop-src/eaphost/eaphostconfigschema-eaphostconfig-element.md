---
title: Élément EapHostConfig
description: Contient l’élément EapMethod et l’élément config ou ConfigBlob. Les éléments config et ConfigBlob ne peuvent pas être utilisés simultanément.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Élément EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032282"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="b09da-105">Élément EapHostConfig</span><span class="sxs-lookup"><span data-stu-id="b09da-105">EapHostConfig Element</span></span>

<span data-ttu-id="b09da-106">L’élément **EapHostConfig** contient l’élément [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) et l’élément [**config**](eaphostconfigschema-config-eaphostconfig-element.md) ou [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b09da-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="b09da-107">Les éléments [**config**](eaphostconfigschema-config-eaphostconfig-element.md) et [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="b09da-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="b09da-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b09da-108">Child elements</span></span>



| <span data-ttu-id="b09da-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b09da-109">Element</span></span>                                                                    | <span data-ttu-id="b09da-110">Type</span><span class="sxs-lookup"><span data-stu-id="b09da-110">Type</span></span>                                                                                     | <span data-ttu-id="b09da-111">Description</span><span class="sxs-lookup"><span data-stu-id="b09da-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b09da-112">**Package**</span><span class="sxs-lookup"><span data-stu-id="b09da-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="b09da-113">**BaseEapMethodConfig**</span><span class="sxs-lookup"><span data-stu-id="b09da-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="b09da-114">Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.</span><span class="sxs-lookup"><span data-stu-id="b09da-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="b09da-115">**ConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="b09da-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="b09da-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="b09da-116">hexBinary</span></span>                                                                                | <span data-ttu-id="b09da-117">Est utilisé lorsque la configuration de la méthode est sous forme d’objet BLOB binaire au lieu d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="b09da-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="b09da-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="b09da-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="b09da-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="b09da-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="b09da-120">Identifie la méthode référencée.</span><span class="sxs-lookup"><span data-stu-id="b09da-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="b09da-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b09da-121">Remarks</span></span>

<span data-ttu-id="b09da-122">L’élément **processContents** active les futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="b09da-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="b09da-123">L’élément **processContents** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b09da-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b09da-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b09da-124">Requirements</span></span>



| <span data-ttu-id="b09da-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b09da-125">Requirement</span></span> | <span data-ttu-id="b09da-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b09da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b09da-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b09da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b09da-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b09da-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b09da-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b09da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b09da-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b09da-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b09da-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b09da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09da-132">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="b09da-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b09da-133">Schéma eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="b09da-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





