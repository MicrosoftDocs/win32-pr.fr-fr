---
description: Contient les paramètres de sécurité pour les réseaux câblés.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Élément Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106538562"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="3dd45-103">Élément Security (MSM) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="3dd45-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="3dd45-104">L’élément Security (MSM) contient des paramètres de sécurité pour les réseaux câblés.</span><span class="sxs-lookup"><span data-stu-id="3dd45-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="3dd45-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="3dd45-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
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

<span data-ttu-id="3dd45-106">L’élément de **sécurité** est défini par l’élément [**MSM**](lan-profileschema-msm-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd45-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3dd45-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3dd45-107">Child elements</span></span>



| <span data-ttu-id="3dd45-108">Élément</span><span class="sxs-lookup"><span data-stu-id="3dd45-108">Element</span></span>                                                                 | <span data-ttu-id="3dd45-109">Type</span><span class="sxs-lookup"><span data-stu-id="3dd45-109">Type</span></span>    | <span data-ttu-id="3dd45-110">Description</span><span class="sxs-lookup"><span data-stu-id="3dd45-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dd45-111">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="3dd45-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="3dd45-112">boolean</span><span class="sxs-lookup"><span data-stu-id="3dd45-112">boolean</span></span> | <span data-ttu-id="3dd45-113">Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3dd45-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="3dd45-114">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="3dd45-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="3dd45-115">boolean</span><span class="sxs-lookup"><span data-stu-id="3dd45-115">boolean</span></span> | <span data-ttu-id="3dd45-116">Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="3dd45-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3dd45-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dd45-117">Requirements</span></span>



| <span data-ttu-id="3dd45-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dd45-118">Requirement</span></span> | <span data-ttu-id="3dd45-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dd45-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3dd45-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dd45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd45-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dd45-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3dd45-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dd45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd45-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dd45-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3dd45-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dd45-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="3dd45-125">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="3dd45-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3dd45-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="3dd45-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3dd45-127">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="3dd45-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3dd45-128">**MSM (LANProfile)**</span><span class="sxs-lookup"><span data-stu-id="3dd45-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




