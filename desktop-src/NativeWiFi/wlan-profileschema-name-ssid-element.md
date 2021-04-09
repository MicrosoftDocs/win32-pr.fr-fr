---
description: Contient le SSID d’un réseau local sans fil.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: nom (SSID), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867278"
---
# <a name="name-ssid-element"></a><span data-ttu-id="4e195-103">nom (SSID), élément</span><span class="sxs-lookup"><span data-stu-id="4e195-103">name (SSID) Element</span></span>

<span data-ttu-id="4e195-104">L’élément nom (SSID) contient le SSID d’un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="4e195-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4e195-105">L’élément est défini par l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4e195-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e195-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4e195-106">Remarks</span></span>

<span data-ttu-id="4e195-107">Les noms respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="4e195-107">Names are case-sensitive.</span></span>

<span data-ttu-id="4e195-108">Bien que les éléments [**Hex**](wlan-profileschema-hex-ssid-element.md) et **Name** soient facultatifs, au moins un élément **Hex** ou **Name** doit apparaître en tant qu’enfant de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4e195-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="4e195-109">Lorsque les informations de profil sont converties en SSID, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est converti en SSID (le cas échéant) et l’élément **Name** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4e195-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="4e195-110">Si l’élément **Hex** n’est pas présent, l’élément **Name** est converti en SSID à l’aide d’une conversion Unicode en ASCII.</span><span class="sxs-lookup"><span data-stu-id="4e195-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="4e195-111">Lorsqu’un SSID est stocké dans un profil, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est toujours généré.</span><span class="sxs-lookup"><span data-stu-id="4e195-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="4e195-112">L’élément **Name** est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit.</span><span class="sxs-lookup"><span data-stu-id="4e195-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="4e195-113">Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un **nom**.</span><span class="sxs-lookup"><span data-stu-id="4e195-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="4e195-114">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Les caractères d’échappement XML, tels que les &, ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="4e195-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="4e195-115">Évitez d’utiliser des caractères d’échappement XML dans des noms SSID pour les profils déployés sur Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="4e195-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="4e195-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="4e195-116">Examples</span></span>

<span data-ttu-id="4e195-117">Pour afficher des exemples de profils qui utilisent l’élément **Name** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="4e195-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e195-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e195-118">Requirements</span></span>



| <span data-ttu-id="4e195-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e195-119">Requirement</span></span> | <span data-ttu-id="4e195-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e195-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4e195-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e195-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e195-122">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e195-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4e195-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e195-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e195-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e195-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="4e195-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4e195-125">Redistributable</span></span><br/>          | <span data-ttu-id="4e195-126">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="4e195-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4e195-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e195-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e195-128">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="4e195-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4e195-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="4e195-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="4e195-130">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="4e195-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4e195-131">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="4e195-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




