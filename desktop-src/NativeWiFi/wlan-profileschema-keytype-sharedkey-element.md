---
description: Indique si la clé partagée sera une clé réseau ou une phrase secrète.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: KeyType (sharedKey), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531708"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="1db0a-103">KeyType (sharedKey), élément</span><span class="sxs-lookup"><span data-stu-id="1db0a-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="1db0a-104">L’élément KeyType (sharedKey) indique si la clé partagée sera une clé réseau ou une phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="1db0a-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1db0a-105">L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1db0a-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db0a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1db0a-106">Remarks</span></span>

<span data-ttu-id="1db0a-107">Lorsque l’élément de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md) a la valeur WEP, **KeyType** doit être défini sur **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="1db0a-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="1db0a-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="1db0a-108">Examples</span></span>

<span data-ttu-id="1db0a-109">Pour afficher des exemples de profils qui utilisent l’élément **KeyType** , consultez exemple de [profil de non-diffusion](non-broadcast-profile-sample.md), exemple de [Profil WPA-Personnel](wpa-personal-profile-sample.md)et exemple de profil [WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1db0a-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1db0a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1db0a-110">Requirements</span></span>



| <span data-ttu-id="1db0a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1db0a-111">Requirement</span></span> | <span data-ttu-id="1db0a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1db0a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1db0a-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1db0a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1db0a-114">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1db0a-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1db0a-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1db0a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1db0a-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1db0a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1db0a-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1db0a-117">Redistributable</span></span><br/>          | <span data-ttu-id="1db0a-118">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="1db0a-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1db0a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1db0a-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="1db0a-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="1db0a-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1db0a-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="1db0a-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="1db0a-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="1db0a-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1db0a-123">**sharedKey (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="1db0a-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




