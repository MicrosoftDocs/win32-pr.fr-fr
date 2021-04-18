---
description: Indique si une clé partagée est chiffrée.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Élément protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515991"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="8d454-103">Élément protected (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="8d454-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="8d454-104">L’élément protected (sharedKey) indique si une clé partagée est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="8d454-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="8d454-105">L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8d454-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d454-106">Notes</span><span class="sxs-lookup"><span data-stu-id="8d454-106">Remarks</span></span>

<span data-ttu-id="8d454-107">Pour Windows Vista et Windows Server 2008, **protected** a toujours la valeur true si le profil a été récupéré à partir du magasin de profils (par exemple, en appelant [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span><span class="sxs-lookup"><span data-stu-id="8d454-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="8d454-108">Pour les profils destinés à être utilisés sur Windows XP avec Service Pack 3 (SP3) ou sur l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2), **protected** doit avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="8d454-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="8d454-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="8d454-109">Examples</span></span>

<span data-ttu-id="8d454-110">Pour afficher des exemples de profils qui utilisent l’élément **protégé** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8d454-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d454-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d454-111">Requirements</span></span>



| <span data-ttu-id="8d454-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d454-112">Requirement</span></span> | <span data-ttu-id="8d454-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d454-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d454-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d454-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8d454-115">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d454-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d454-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d454-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8d454-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d454-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8d454-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8d454-118">Redistributable</span></span><br/>          | <span data-ttu-id="8d454-119">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="8d454-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8d454-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d454-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d454-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="8d454-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8d454-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="8d454-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="8d454-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="8d454-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8d454-124">**sharedKey (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="8d454-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




