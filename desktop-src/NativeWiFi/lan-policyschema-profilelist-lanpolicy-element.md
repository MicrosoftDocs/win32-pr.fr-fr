---
description: Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Élément profileList (LANPolicy)
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536741"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="184c6-103">Élément profileList (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="184c6-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="184c6-104">L’élément profileList (LANPolicy) contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="184c6-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="184c6-105">Les profils doivent être basés sur [le \_ schéma de profil de réseau local](lan-profileschema-schema.md), avec un élément racine [**LANProfile**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="184c6-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="184c6-106">Les profils basés sur un autre schéma seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="184c6-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="184c6-107">Quand [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) est défini sur false, cet élément ne doit pas être présent dans un profil de stratégie de réseau local.</span><span class="sxs-lookup"><span data-stu-id="184c6-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="184c6-108">Quand **enableAutoConfig** a la valeur true, cet élément est requis.</span><span class="sxs-lookup"><span data-stu-id="184c6-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="184c6-109">L’élément **profileList** est défini par l’élément [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="184c6-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="184c6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="184c6-110">Remarks</span></span>

<span data-ttu-id="184c6-111">Cet élément doit contenir exactement un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="184c6-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="184c6-112">Si plusieurs profils sont spécifiés dans la stratégie, seul le premier réseau sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="184c6-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="184c6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="184c6-113">Requirements</span></span>



| <span data-ttu-id="184c6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="184c6-114">Requirement</span></span> | <span data-ttu-id="184c6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="184c6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="184c6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="184c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="184c6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="184c6-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="184c6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="184c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="184c6-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="184c6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="184c6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="184c6-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="184c6-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="184c6-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="184c6-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="184c6-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="184c6-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="184c6-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="184c6-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="184c6-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




