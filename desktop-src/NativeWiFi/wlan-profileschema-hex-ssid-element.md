---
description: Contient le SSID d’un réseau local sans fil au format hexadécimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Élément hex (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540822"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="a8850-103">Élément hex (SSID)</span><span class="sxs-lookup"><span data-stu-id="a8850-103">hex (SSID) Element</span></span>

<span data-ttu-id="a8850-104">L’élément hex (SSID) contient le SSID d’un réseau local sans fil au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="a8850-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
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

<span data-ttu-id="a8850-105">L’élément est défini par l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8850-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8850-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a8850-106">Remarks</span></span>

<span data-ttu-id="a8850-107">Bien que les éléments **Hex** et [**Name**](wlan-profileschema-name-ssid-element.md) soient facultatifs, au moins un élément **Hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) doit apparaître en tant qu’enfant de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8850-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="a8850-108">Lorsque les informations de profil sont converties en SSID, l’élément **Hex** est converti en SSID (le cas échéant) et l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a8850-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="a8850-109">Si l’élément **Hex** n’est pas présent, l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est converti en SSID à l’aide d’une conversion Unicode en ASCII.</span><span class="sxs-lookup"><span data-stu-id="a8850-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="a8850-110">Lorsqu’un SSID est stocké dans un profil, l’élément **Hex** est toujours généré.</span><span class="sxs-lookup"><span data-stu-id="a8850-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="a8850-111">L’élément [**Name**](wlan-profileschema-name-ssid-element.md) est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit.</span><span class="sxs-lookup"><span data-stu-id="a8850-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="a8850-112">Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un [**nom**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="a8850-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8850-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8850-113">Examples</span></span>

<span data-ttu-id="a8850-114">Pour afficher un exemple de profil qui utilise l’élément **Hex** , consultez [exemple de profil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a8850-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8850-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8850-115">Requirements</span></span>



| <span data-ttu-id="a8850-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8850-116">Requirement</span></span> | <span data-ttu-id="a8850-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8850-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a8850-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8850-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8850-119">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8850-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8850-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8850-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8850-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8850-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a8850-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a8850-122">Redistributable</span></span><br/>          | <span data-ttu-id="a8850-123">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="a8850-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a8850-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8850-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8850-125">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a8850-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8850-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="a8850-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="a8850-127">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8850-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8850-128">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="a8850-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




