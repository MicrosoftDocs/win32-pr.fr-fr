---
description: Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Élément authEncryption (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536343"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="83a4f-103">Élément authEncryption (Security)</span><span class="sxs-lookup"><span data-stu-id="83a4f-103">authEncryption (security) Element</span></span>

<span data-ttu-id="83a4f-104">L’élément authEncryption (Security) spécifie la paire d’authentification et de chiffrement à utiliser pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="83a4f-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="83a4f-105">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="83a4f-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="83a4f-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="83a4f-106">Child elements</span></span>



| <span data-ttu-id="83a4f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="83a4f-107">Element</span></span>                                                                            | <span data-ttu-id="83a4f-108">Type</span><span class="sxs-lookup"><span data-stu-id="83a4f-108">Type</span></span>                                                              | <span data-ttu-id="83a4f-109">Description</span><span class="sxs-lookup"><span data-stu-id="83a4f-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83a4f-110">**identification**</span><span class="sxs-lookup"><span data-stu-id="83a4f-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="83a4f-111">Spécifie la méthode d’authentification qui doit être utilisée pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="83a4f-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="83a4f-112">**chiffre**</span><span class="sxs-lookup"><span data-stu-id="83a4f-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="83a4f-113">Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="83a4f-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="83a4f-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="83a4f-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="83a4f-115">boolean</span><span class="sxs-lookup"><span data-stu-id="83a4f-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="83a4f-116">Indique si 802.1 X est utilisé.</span><span class="sxs-lookup"><span data-stu-id="83a4f-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="83a4f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="83a4f-117">Remarks</span></span>

<span data-ttu-id="83a4f-118">L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément **authEncryption** .</span><span class="sxs-lookup"><span data-stu-id="83a4f-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="83a4f-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="83a4f-119">Examples</span></span>

<span data-ttu-id="83a4f-120">Pour afficher des exemples de profils qui utilisent l’élément **authEncryption** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="83a4f-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="83a4f-121">Pour afficher un exemple de profil qui utilise l’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) , consultez [exemple de profil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="83a4f-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83a4f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83a4f-122">Requirements</span></span>



| <span data-ttu-id="83a4f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83a4f-123">Requirement</span></span> | <span data-ttu-id="83a4f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="83a4f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="83a4f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83a4f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83a4f-126">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83a4f-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="83a4f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83a4f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83a4f-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83a4f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="83a4f-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="83a4f-129">Redistributable</span></span><br/>          | <span data-ttu-id="83a4f-130">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="83a4f-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="83a4f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83a4f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a4f-132">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="83a4f-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="83a4f-133">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="83a4f-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="83a4f-134">**caution**</span><span class="sxs-lookup"><span data-stu-id="83a4f-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="83a4f-135">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="83a4f-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="83a4f-136">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="83a4f-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
