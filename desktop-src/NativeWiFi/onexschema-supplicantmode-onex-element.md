---
description: Spécifie la méthode de transmission utilisée pour EAPOL-Start messages.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Élément supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517693"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="dc271-103">Élément supplicantMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="dc271-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="dc271-104">L’élément supplicantMode (OneX) spécifie la méthode de transmission utilisée pour EAPOL-Start messages.</span><span class="sxs-lookup"><span data-stu-id="dc271-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="dc271-105">Le tableau suivant décrit les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="dc271-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="dc271-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc271-106">Value</span></span>               | <span data-ttu-id="dc271-107">Description</span><span class="sxs-lookup"><span data-stu-id="dc271-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc271-108">inhibitTransmission</span><span class="sxs-lookup"><span data-stu-id="dc271-108">inhibitTransmission</span></span> | <span data-ttu-id="dc271-109">Les messages de EAPOL-Start ne sont pas transmis.</span><span class="sxs-lookup"><span data-stu-id="dc271-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="dc271-110">Valide pour les profils LAN câblés uniquement.</span><span class="sxs-lookup"><span data-stu-id="dc271-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="dc271-111">includeLearning</span><span class="sxs-lookup"><span data-stu-id="dc271-111">includeLearning</span></span>     | <span data-ttu-id="dc271-112">Le client détermine quand envoyer des paquets EAPOL-Start en fonction de la capacité du réseau.</span><span class="sxs-lookup"><span data-stu-id="dc271-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="dc271-113">Les messages de EAPOL-Start sont envoyés uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dc271-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="dc271-114">Valide pour les profils LAN câblés uniquement.</span><span class="sxs-lookup"><span data-stu-id="dc271-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="dc271-115">conforme</span><span class="sxs-lookup"><span data-stu-id="dc271-115">compliant</span></span>           | <span data-ttu-id="dc271-116">EAPOL-Start messages sont transmis comme spécifié par 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="dc271-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="dc271-117">Valide pour les profils de réseau local câblés et sans fil.</span><span class="sxs-lookup"><span data-stu-id="dc271-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="dc271-118">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="dc271-118">This element is optional.</span></span> <span data-ttu-id="dc271-119">Quand supplicantMode n’est pas spécifié dans un profil, la valeur `compliant` est utilisée pour les profils de réseau local câblés et sans fil.</span><span class="sxs-lookup"><span data-stu-id="dc271-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="dc271-120">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="dc271-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="dc271-121">L’élément **supplicantMode** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dc271-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc271-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc271-122">Requirements</span></span>



| <span data-ttu-id="dc271-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc271-123">Requirement</span></span> | <span data-ttu-id="dc271-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc271-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc271-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc271-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dc271-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc271-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc271-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc271-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dc271-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc271-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc271-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc271-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc271-130">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="dc271-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dc271-131">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="dc271-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="dc271-132">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="dc271-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dc271-133">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="dc271-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




