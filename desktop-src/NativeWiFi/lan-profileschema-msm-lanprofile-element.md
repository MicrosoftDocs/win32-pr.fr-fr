---
description: Contient les paramètres de module spécifique au média (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Élément MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203762"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="91229-103">Élément MSM (LANProfile)</span><span class="sxs-lookup"><span data-stu-id="91229-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="91229-104">L’élément MSM (LANProfile) contient des paramètres de module spécifique au média (MSM).</span><span class="sxs-lookup"><span data-stu-id="91229-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="91229-105">L’élément **MSM** est défini par l’élément [**LANProfile**](lan-profileschema-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="91229-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="91229-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="91229-106">Child elements</span></span>



| <span data-ttu-id="91229-107">Élément</span><span class="sxs-lookup"><span data-stu-id="91229-107">Element</span></span>                                                                 | <span data-ttu-id="91229-108">Type</span><span class="sxs-lookup"><span data-stu-id="91229-108">Type</span></span>    | <span data-ttu-id="91229-109">Description</span><span class="sxs-lookup"><span data-stu-id="91229-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91229-110">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="91229-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="91229-111">boolean</span><span class="sxs-lookup"><span data-stu-id="91229-111">boolean</span></span> | <span data-ttu-id="91229-112">Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="91229-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="91229-113">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="91229-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="91229-114">boolean</span><span class="sxs-lookup"><span data-stu-id="91229-114">boolean</span></span> | <span data-ttu-id="91229-115">Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="91229-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="91229-116">**caution**</span><span class="sxs-lookup"><span data-stu-id="91229-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="91229-117">Contient les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="91229-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="91229-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91229-118">Requirements</span></span>



| <span data-ttu-id="91229-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91229-119">Requirement</span></span> | <span data-ttu-id="91229-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="91229-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91229-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91229-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91229-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91229-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91229-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91229-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91229-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91229-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91229-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91229-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="91229-126">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="91229-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="91229-127">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="91229-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="91229-128">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="91229-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="91229-129">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="91229-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




