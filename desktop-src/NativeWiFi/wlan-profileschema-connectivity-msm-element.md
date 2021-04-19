---
description: Contient différents paramètres de connectivité.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Élément de connectivité (MSM)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531412"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="bc718-103">Élément de connectivité (MSM)</span><span class="sxs-lookup"><span data-stu-id="bc718-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="bc718-104">L’élément de connectivité (MSM) contient différents paramètres de connectivité.</span><span class="sxs-lookup"><span data-stu-id="bc718-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
                         />
                    </xs:restriction>
                </xs:simpleType>
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

<span data-ttu-id="bc718-105">L’élément est défini par l’élément [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bc718-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bc718-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bc718-106">Child elements</span></span>



| <span data-ttu-id="bc718-107">Élément</span><span class="sxs-lookup"><span data-stu-id="bc718-107">Element</span></span>                                                            | <span data-ttu-id="bc718-108">Type</span><span class="sxs-lookup"><span data-stu-id="bc718-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="bc718-109">**phyType**</span><span class="sxs-lookup"><span data-stu-id="bc718-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="bc718-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="bc718-110">Examples</span></span>

<span data-ttu-id="bc718-111">Pour afficher des exemples de profils qui utilisent l’élément de **connectivité** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="bc718-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc718-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc718-112">Requirements</span></span>



| <span data-ttu-id="bc718-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc718-113">Requirement</span></span> | <span data-ttu-id="bc718-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc718-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bc718-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc718-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bc718-116">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc718-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc718-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc718-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bc718-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc718-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="bc718-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bc718-119">Redistributable</span></span><br/>          | <span data-ttu-id="bc718-120">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="bc718-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bc718-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc718-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc718-122">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bc718-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bc718-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="bc718-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="bc718-124">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bc718-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bc718-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="bc718-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




