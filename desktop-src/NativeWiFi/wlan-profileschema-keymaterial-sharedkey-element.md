---
description: Contient une clé réseau ou une phrase secrète.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Élément keyMaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203059"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="4532e-103">Élément keyMaterial (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="4532e-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="4532e-104">L’élément keyMaterial (sharedKey) contient une clé réseau ou une phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="4532e-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="4532e-105">Si l’élément [**protégé**](wlan-profileschema-protected-sharedkey-element.md) a la valeur true, ce matériel de clé est chiffré ; dans le cas contraire, le matériel de clé n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="4532e-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="4532e-106">Le matériel de clé chiffrée est exprimé au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="4532e-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="4532e-107">L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4532e-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4532e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4532e-108">Remarks</span></span>

<span data-ttu-id="4532e-109">La plage de valeurs valides pour l’élément keyMaterial varie selon le type d’authentification et le chiffrement utilisés, comme spécifié par les éléments [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) et [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4532e-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="4532e-110">Elle varie également en fonction du [**type de frappe**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="4532e-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="4532e-111">Le tableau suivant indique les valeurs de **clés** valides pour certaines paires d’authentification et de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4532e-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="4532e-112">valeur [**d’authentification**](wlan-profileschema-authentication-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="4532e-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="4532e-113">valeur de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="4532e-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="4532e-114">valeur de [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md)</span><span class="sxs-lookup"><span data-stu-id="4532e-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="4532e-115">Valeurs de **clés** valides</span><span class="sxs-lookup"><span data-stu-id="4532e-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4532e-116">ouvert ou partagé</span><span class="sxs-lookup"><span data-stu-id="4532e-116">open or shared</span></span>                                                                           | <span data-ttu-id="4532e-117">WEP</span><span class="sxs-lookup"><span data-stu-id="4532e-117">WEP</span></span>                                                                              | <span data-ttu-id="4532e-118">networkKey</span><span class="sxs-lookup"><span data-stu-id="4532e-118">networkKey</span></span>                                                            | <span data-ttu-id="4532e-119">Cet élément contient une clé WEP de 5 ou 13 caractères ANSI, ou de 10 ou 26 caractères hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="4532e-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="4532e-120">WPAPSK ou WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="4532e-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="4532e-121">TKIP ou AES</span><span class="sxs-lookup"><span data-stu-id="4532e-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="4532e-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="4532e-122">passPhrase</span></span>                                                            | <span data-ttu-id="4532e-123">Cet élément contient une phrase secrète comprise entre 8 et 63 caractères ASCII, soit 8 à 63 caractères ANSI dans la plage de 32 à 126.</span><span class="sxs-lookup"><span data-stu-id="4532e-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="4532e-124">Les valeurs de clé doivent respecter les exigences spécifiées par la norme 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="4532e-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="4532e-125">WPAPSK ou WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="4532e-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="4532e-126">TKIP ou AES</span><span class="sxs-lookup"><span data-stu-id="4532e-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="4532e-127">networkKey</span><span class="sxs-lookup"><span data-stu-id="4532e-127">networkKey</span></span>                                                            | <span data-ttu-id="4532e-128">Cet élément contient une clé de 64 caractères hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="4532e-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="4532e-129">Des caractères Unicode peuvent être entrés là où les caractères ANSI ou ASCII sont spécifiés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4532e-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="4532e-130">Toutefois, si les caractères Unicode fournis ne peuvent pas être mappés à des caractères ANSI ou ASCII, le matériel de clé fourni est rejeté.</span><span class="sxs-lookup"><span data-stu-id="4532e-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="4532e-131">Le matériel de clé retourné par [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) est toujours chiffré.</span><span class="sxs-lookup"><span data-stu-id="4532e-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="4532e-132">En outre, si le matériel de clé non chiffré est transmis à [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), le matériel de clé est automatiquement chiffré avant d’être stocké dans le magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="4532e-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="4532e-133">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Le matériel de clé n’est jamais chiffré.</span><span class="sxs-lookup"><span data-stu-id="4532e-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="4532e-134">Si votre processus s’exécute dans le contexte du compte LocalSystem, vous pouvez déchiffrer le matériel de clé en appelant [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="4532e-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="4532e-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="4532e-135">Examples</span></span>

<span data-ttu-id="4532e-136">Pour afficher des exemples de profils qui utilisent l’élément **keyMaterial** , consultez exemple de [profil de non-diffusion](non-broadcast-profile-sample.md), exemple de [Profil WPA-Personnel](wpa-personal-profile-sample.md)et exemple de profil [WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4532e-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4532e-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4532e-137">Requirements</span></span>



| <span data-ttu-id="4532e-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4532e-138">Requirement</span></span> | <span data-ttu-id="4532e-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="4532e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4532e-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4532e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4532e-141">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4532e-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4532e-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4532e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4532e-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4532e-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="4532e-144">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4532e-144">Redistributable</span></span><br/>          | <span data-ttu-id="4532e-145">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="4532e-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4532e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4532e-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="4532e-147">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="4532e-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4532e-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="4532e-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="4532e-149">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="4532e-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4532e-150">**sharedKey (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="4532e-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
