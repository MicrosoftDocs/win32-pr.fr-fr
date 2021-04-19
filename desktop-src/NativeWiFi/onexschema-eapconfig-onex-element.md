---
description: spécifie la configuration EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Élément EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518234"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="b2a70-103">Élément EAPConfig (OneX)</span><span class="sxs-lookup"><span data-stu-id="b2a70-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="b2a70-104">L’élément **EAPConfig** (Onex) spécifie la configuration EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b2a70-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="b2a70-105">Contrairement à la plupart des éléments du schéma de profil 802.1 X, cet élément se trouve dans l' `https://www.microsoft.com/provisioning/EapHostConfig` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b2a70-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="b2a70-106">Ses éléments enfants sont définis dans le [schéma eaphostconfig](../eaphost/eaphostconfigschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b2a70-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="b2a70-107">L’élément [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) est un enfant de l’élément **EAPConfig** .</span><span class="sxs-lookup"><span data-stu-id="b2a70-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b2a70-108">L’élément **EAPConfig** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b2a70-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a70-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2a70-109">Requirements</span></span>



| <span data-ttu-id="b2a70-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2a70-110">Requirement</span></span> | <span data-ttu-id="b2a70-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2a70-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b2a70-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a70-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a70-113">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2a70-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2a70-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a70-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a70-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2a70-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b2a70-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b2a70-116">Redistributable</span></span><br/>          | <span data-ttu-id="b2a70-117">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="b2a70-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b2a70-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2a70-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2a70-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="b2a70-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2a70-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="b2a70-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b2a70-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="b2a70-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2a70-122">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="b2a70-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
