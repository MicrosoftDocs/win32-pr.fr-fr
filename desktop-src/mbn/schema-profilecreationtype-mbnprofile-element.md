---
description: Contient des informations sur le créateur du profil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Élément ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113454"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="92660-103">Élément ProfileCreationType (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="92660-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="92660-104">L’élément **ProfileCreationType (MBNProfile)** contient des informations sur le créateur du profil.</span><span class="sxs-lookup"><span data-stu-id="92660-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="92660-105">Cet élément peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="92660-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="92660-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="92660-106">Value</span></span>                 | <span data-ttu-id="92660-107">Signification</span><span class="sxs-lookup"><span data-stu-id="92660-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92660-108">"UserProvisioned"</span><span class="sxs-lookup"><span data-stu-id="92660-108">"UserProvisioned"</span></span>     | <span data-ttu-id="92660-109">Ce profil est créé par les informations fournies par l’utilisateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="92660-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="92660-110">"AdminProvisioned"</span><span class="sxs-lookup"><span data-stu-id="92660-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="92660-111">Ce profil est créé par les administrateurs informatiques et distribué aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="92660-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="92660-112">"OperatorProvisioned"</span><span class="sxs-lookup"><span data-stu-id="92660-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="92660-113">Ce profil est créé par un opérateur réseau et distribué aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="92660-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="92660-114">"DeviceProvisioned"</span><span class="sxs-lookup"><span data-stu-id="92660-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="92660-115">Ce profil est créé par le service haut débit mobile à l’aide des informations stockées dans le contexte approvisionné par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="92660-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="92660-116">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="92660-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="92660-117">L’élément **ProfileCreationType** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="92660-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="92660-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92660-118">Requirements</span></span>



| <span data-ttu-id="92660-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92660-119">Requirement</span></span> | <span data-ttu-id="92660-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="92660-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="92660-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92660-121">Minimum supported client</span></span><br/> | <span data-ttu-id="92660-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92660-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="92660-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92660-123">Minimum supported server</span></span><br/> | <span data-ttu-id="92660-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="92660-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="92660-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92660-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="92660-126">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="92660-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="92660-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="92660-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="92660-128">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="92660-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="92660-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="92660-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




