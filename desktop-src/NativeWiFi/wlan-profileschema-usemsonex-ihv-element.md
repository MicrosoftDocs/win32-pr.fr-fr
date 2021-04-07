---
description: Spécifie l’origine des paramètres de sécurité 802.1 X utilisés par un composant de sécurité IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Élément useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952222"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="ecd4b-103">Élément useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="ecd4b-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="ecd4b-104">L’élément **useMSOneX** (IHV) spécifie l’origine des paramètres de sécurité 802.1 x utilisés par un composant de sécurité IHV.</span><span class="sxs-lookup"><span data-stu-id="ecd4b-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="ecd4b-105">Quand **useMSOneX** a la valeur true, les composants de sécurité IHV utilisent les paramètres 802.1 x définis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ecd4b-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="ecd4b-106">Quand **useMSOneX** a la valeur false, les composants de sécurité IHV utilisent les paramètres 802.1 x fournis par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ecd4b-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="ecd4b-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecd4b-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="ecd4b-108">L’élément est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd4b-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd4b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecd4b-109">Requirements</span></span>



| <span data-ttu-id="ecd4b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecd4b-110">Requirement</span></span> | <span data-ttu-id="ecd4b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecd4b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ecd4b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd4b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd4b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecd4b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ecd4b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecd4b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd4b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecd4b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecd4b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd4b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ecd4b-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ecd4b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ecd4b-118">**FABRICANTS**</span><span class="sxs-lookup"><span data-stu-id="ecd4b-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ecd4b-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ecd4b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ecd4b-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ecd4b-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




