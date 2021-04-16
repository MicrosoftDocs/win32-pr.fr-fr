---
description: Contient le nom d’un profil de réseau local sans fil.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Élément Name (WLANProfile)
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
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527789"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="395af-103">Élément Name (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="395af-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="395af-104">L’élément Name (WLANProfile) contient le nom d’un profil de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="395af-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="395af-105">L’élément **Name** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="395af-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="395af-106">Notes</span><span class="sxs-lookup"><span data-stu-id="395af-106">Remarks</span></span>

<span data-ttu-id="395af-107">Les noms respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="395af-107">Names are case-sensitive.</span></span>

<span data-ttu-id="395af-108">Pour Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2), l’élément Name est ignoré lorsque le profil est enregistré dans le magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="395af-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="395af-109">Le nom du profil est dérivé du SSID du réseau.</span><span class="sxs-lookup"><span data-stu-id="395af-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="395af-110">Pour les profils réseau d’infrastructure, le nom du profil correspond à l’identificateur SSID du réseau.</span><span class="sxs-lookup"><span data-stu-id="395af-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="395af-111">Pour les profils réseau ad hoc, le nom du profil correspond à l’identificateur SSID du réseau ad hoc suivi de `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="395af-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="395af-112">Les caractères d’échappement XML, tels que les &, ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="395af-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="395af-113">Évitez d’utiliser des caractères d’échappement XML dans des noms SSID pour les profils déployés sur Windows XP avec SP3 ou l’API LAN sans fil pour Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="395af-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="395af-114">Pour tout profil réseau destiné à être utilisé uniquement sur Windows Vista ou Windows Server 2008, le nom peut être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="395af-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="395af-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="395af-115">Examples</span></span>

<span data-ttu-id="395af-116">Pour afficher des exemples de profils qui utilisent l’élément **Name** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="395af-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="395af-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="395af-117">Requirements</span></span>



| <span data-ttu-id="395af-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="395af-118">Requirement</span></span> | <span data-ttu-id="395af-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="395af-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="395af-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="395af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="395af-121">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="395af-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="395af-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="395af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="395af-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="395af-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="395af-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="395af-124">Redistributable</span></span><br/>          | <span data-ttu-id="395af-125">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="395af-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="395af-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="395af-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="395af-127">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="395af-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="395af-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="395af-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="395af-129">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="395af-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="395af-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="395af-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




