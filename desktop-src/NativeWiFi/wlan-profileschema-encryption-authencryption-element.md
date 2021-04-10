---
description: Spécifie le type de chiffrement des données à utiliser pour se connecter à un réseau local sans fil.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Élément Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113614"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="6acfd-103">Élément Encryption (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="6acfd-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="6acfd-104">L’élément Encryption (authEncryption) spécifie le type de chiffrement des données à utiliser pour se connecter à un réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="6acfd-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6acfd-105">L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6acfd-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acfd-106">Notes</span><span class="sxs-lookup"><span data-stu-id="6acfd-106">Remarks</span></span>

<span data-ttu-id="6acfd-107">Lorsque l’élément de **chiffrement** a la valeur WEP, [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) doit être défini sur **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="6acfd-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="6acfd-108">La méthode de chiffrement AES est spécifiée dans les spécifications [802.1 x](https://ieeexplore.ieee.org/document/1438730) et [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="6acfd-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="6acfd-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="6acfd-109">Examples</span></span>

<span data-ttu-id="6acfd-110">Pour afficher des exemples de profils qui utilisent l’élément de **chiffrement** , consultez [exemples de profils sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6acfd-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6acfd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6acfd-111">Requirements</span></span>



| <span data-ttu-id="6acfd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6acfd-112">Requirement</span></span> | <span data-ttu-id="6acfd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acfd-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6acfd-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acfd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6acfd-115">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acfd-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6acfd-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acfd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6acfd-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acfd-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6acfd-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6acfd-118">Redistributable</span></span><br/>          | <span data-ttu-id="6acfd-119">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="6acfd-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6acfd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6acfd-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6acfd-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6acfd-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6acfd-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="6acfd-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="6acfd-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6acfd-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6acfd-124">**authEncryption (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="6acfd-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




