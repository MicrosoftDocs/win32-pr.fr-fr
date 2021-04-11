---
description: Spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Élément ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951157"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="59ac0-103">Élément ConnectionMode (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="59ac0-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="59ac0-104">L’élément **ConnectionMode (MBNProfile)** spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="59ac0-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="59ac0-105">Cet élément peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="59ac0-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="59ac0-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ac0-106">Value</span></span>       | <span data-ttu-id="59ac0-107">Signification</span><span class="sxs-lookup"><span data-stu-id="59ac0-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="59ac0-108">opération</span><span class="sxs-lookup"><span data-stu-id="59ac0-108">"manual"</span></span>    | <span data-ttu-id="59ac0-109">Ne jamais se connecter automatiquement au réseau.</span><span class="sxs-lookup"><span data-stu-id="59ac0-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="59ac0-110">saisie</span><span class="sxs-lookup"><span data-stu-id="59ac0-110">"auto"</span></span>      | <span data-ttu-id="59ac0-111">Toujours se connecter automatiquement au réseau.</span><span class="sxs-lookup"><span data-stu-id="59ac0-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="59ac0-112">« Auto-démarrage »</span><span class="sxs-lookup"><span data-stu-id="59ac0-112">"auto-home"</span></span> | <span data-ttu-id="59ac0-113">Se connecter automatiquement au réseau sauf dans un réseau itinérant.</span><span class="sxs-lookup"><span data-stu-id="59ac0-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="59ac0-114">Cet élément peut avoir au maximum une occurrence.</span><span class="sxs-lookup"><span data-stu-id="59ac0-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="59ac0-115">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="59ac0-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="59ac0-116">L’élément **ConnectionMode** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="59ac0-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ac0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59ac0-117">Requirements</span></span>



| <span data-ttu-id="59ac0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59ac0-118">Requirement</span></span> | <span data-ttu-id="59ac0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="59ac0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="59ac0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ac0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59ac0-121">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="59ac0-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="59ac0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ac0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59ac0-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="59ac0-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="59ac0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ac0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="59ac0-125">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="59ac0-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="59ac0-126">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="59ac0-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="59ac0-127">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="59ac0-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="59ac0-128">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="59ac0-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




