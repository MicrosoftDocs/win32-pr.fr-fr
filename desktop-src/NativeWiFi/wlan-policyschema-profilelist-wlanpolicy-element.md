---
description: 'Élément profileList (WLANPolicy) : contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Élément profileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109197"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="b2201-103">Élément profileList (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="b2201-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="b2201-104">L’élément profileList (WLANPolicy) contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b2201-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="b2201-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="b2201-105">This element is optional.</span></span> <span data-ttu-id="b2201-106">Si cet élément est présent, il doit contenir au moins un profil.</span><span class="sxs-lookup"><span data-stu-id="b2201-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="b2201-107">Les profils doivent être basés sur [le \_ schéma de profil WLAN](wlan-profileschema-schema.md), avec un élément racine [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="b2201-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b2201-108">L’élément **profileList** est défini par l’élément [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b2201-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2201-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2201-109">Requirements</span></span>



| <span data-ttu-id="b2201-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2201-110">Requirement</span></span> | <span data-ttu-id="b2201-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2201-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2201-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2201-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b2201-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2201-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2201-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2201-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b2201-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2201-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2201-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2201-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2201-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="b2201-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2201-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b2201-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="b2201-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="b2201-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2201-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b2201-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




