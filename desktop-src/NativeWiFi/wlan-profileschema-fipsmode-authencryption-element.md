---
description: Indique si le mode FIPS est activé.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Élément FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752301"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="fc5d7-103">Élément FIPSMode (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="fc5d7-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="fc5d7-104">L’élément **FipsMode** (authEncryption) indique si le mode FIPS (Federal Information Processing Standards) est activé.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="fc5d7-105">Lorsqu’une connexion sans fil fonctionne en mode FIPS, le niveau de sécurité de la connexion est conforme à la norme FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="fc5d7-106">Pour plus d’informations sur FIPS, consultez la [page d’hébergement de FIPS](https://www.itl.nist.gov/fipspubs/).</span><span class="sxs-lookup"><span data-stu-id="fc5d7-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="fc5d7-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-107">This element is optional.</span></span> <span data-ttu-id="fc5d7-108">Si cet élément n’est pas spécifié dans un profil, le mode FIPS n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="fc5d7-109">**FipsMode** peut avoir la valeur true uniquement lorsque les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="fc5d7-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="fc5d7-110">L’élément [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) a la valeur `ESS` (autrement dit, la connexion est une connexion d’infrastructure).</span><span class="sxs-lookup"><span data-stu-id="fc5d7-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="fc5d7-111">L’élément [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) a la valeur `WPA2` ou `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="fc5d7-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="fc5d7-112">L’élément de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md) a la valeur `AES` .</span><span class="sxs-lookup"><span data-stu-id="fc5d7-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="fc5d7-113">Contrairement à la plupart des éléments du \_ schéma de profil WLAN, cet élément se trouve dans l' `https://www.microsoft.com/networking/WLAN/profile/v2` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="fc5d7-114">La valeur de l’élément **FipsMode** est ignorée si le pilote de miniport de l’interface sans fil ne prend pas en charge le mode FIPS.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="fc5d7-115">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="fc5d7-116">Si **FipsMode** est présent dans un profil, l’élément est ignoré.</span><span class="sxs-lookup"><span data-stu-id="fc5d7-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="fc5d7-117">L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5d7-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc5d7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fc5d7-118">Remarks</span></span>

<span data-ttu-id="fc5d7-119">Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="fc5d7-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="fc5d7-120">Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="fc5d7-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="fc5d7-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="fc5d7-121">Examples</span></span>

<span data-ttu-id="fc5d7-122">Pour afficher un exemple de profil qui utilise l’élément **FipsMode** , consultez [exemple de profil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fc5d7-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5d7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc5d7-123">Requirements</span></span>



| <span data-ttu-id="fc5d7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc5d7-124">Requirement</span></span> | <span data-ttu-id="fc5d7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc5d7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc5d7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc5d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5d7-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc5d7-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc5d7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc5d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5d7-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc5d7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc5d7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc5d7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc5d7-131">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="fc5d7-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fc5d7-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="fc5d7-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="fc5d7-133">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="fc5d7-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fc5d7-134">**authEncryption (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="fc5d7-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
