---
description: Contient des informations sur la clé partagée.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Élément sharedKey (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518312"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="2c38b-103">Élément sharedKey (Security)</span><span class="sxs-lookup"><span data-stu-id="2c38b-103">sharedKey (security) Element</span></span>

<span data-ttu-id="2c38b-104">L’élément sharedKey (Security) contient des informations sur les clés partagées.</span><span class="sxs-lookup"><span data-stu-id="2c38b-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="2c38b-105">Cet élément est requis uniquement si des clés WEP ou PSK sont requises pour la paire authentification et chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2c38b-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
             />
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

<span data-ttu-id="2c38b-106">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2c38b-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2c38b-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2c38b-107">Child elements</span></span>



| <span data-ttu-id="2c38b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="2c38b-108">Element</span></span>                                                                 | <span data-ttu-id="2c38b-109">Type</span><span class="sxs-lookup"><span data-stu-id="2c38b-109">Type</span></span>                                                              | <span data-ttu-id="2c38b-110">Description</span><span class="sxs-lookup"><span data-stu-id="2c38b-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c38b-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="2c38b-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="2c38b-112">string</span><span class="sxs-lookup"><span data-stu-id="2c38b-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="2c38b-113">Contient la clé réseau ou la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="2c38b-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="2c38b-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="2c38b-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="2c38b-115">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="2c38b-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="2c38b-116">**Protect**</span><span class="sxs-lookup"><span data-stu-id="2c38b-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="2c38b-117">boolean</span><span class="sxs-lookup"><span data-stu-id="2c38b-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="2c38b-118">Indique si la clé est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="2c38b-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="2c38b-119">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément doit avoir la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="2c38b-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c38b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2c38b-120">Remarks</span></span>

<span data-ttu-id="2c38b-121">Pour Windows Vista et Windows Server 2008, les données associées à l’élément **sharedKey** sont chiffrées avant d’être enregistrées dans le magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="2c38b-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="2c38b-122">Pour Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2, les données ne sont pas chiffrées.</span><span class="sxs-lookup"><span data-stu-id="2c38b-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="2c38b-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="2c38b-123">Examples</span></span>

<span data-ttu-id="2c38b-124">Pour afficher des exemples de profils qui utilisent l’élément **sharedKey** , consultez exemple de [profil de non-diffusion](non-broadcast-profile-sample.md), exemple de [Profil WPA-Personnel](wpa-personal-profile-sample.md)et exemple de profil [WPA2-personnel](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2c38b-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c38b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c38b-125">Requirements</span></span>



| <span data-ttu-id="2c38b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c38b-126">Requirement</span></span> | <span data-ttu-id="2c38b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c38b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c38b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c38b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2c38b-129">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c38b-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c38b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c38b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2c38b-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c38b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="2c38b-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2c38b-132">Redistributable</span></span><br/>          | <span data-ttu-id="2c38b-133">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="2c38b-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2c38b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c38b-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c38b-135">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="2c38b-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2c38b-136">**caution**</span><span class="sxs-lookup"><span data-stu-id="2c38b-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="2c38b-137">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="2c38b-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2c38b-138">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="2c38b-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
