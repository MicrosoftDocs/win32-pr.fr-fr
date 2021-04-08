---
description: Définit un PHY 802,11 et un type de média.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Énumération DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866037"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="336fc-103">\_ \_ Énumération de type PHY DOT11</span><span class="sxs-lookup"><span data-stu-id="336fc-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="336fc-104">L’énumération du **\_ \_ type de PHY DOT11** définit un type de média 802,11 PHY et.</span><span class="sxs-lookup"><span data-stu-id="336fc-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="336fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="336fc-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="336fc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="336fc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="336fc-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_type de PHY dot11 \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="336fc-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-108">Spécifie un type PHY inconnu ou non initialisé.</span><span class="sxs-lookup"><span data-stu-id="336fc-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**\_ \_ type de PHY dot11 \_ any**</span><span class="sxs-lookup"><span data-stu-id="336fc-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-110">Spécifie un type PHY.</span><span class="sxs-lookup"><span data-stu-id="336fc-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**\_FHSS du \_ type de PHY dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-112">Spécifie un PHY-Spectrum (FHSS) à saut de fréquence.</span><span class="sxs-lookup"><span data-stu-id="336fc-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="336fc-113">Les périphériques Bluetooth peuvent utiliser FHSS ou une adaptation de FHSS.</span><span class="sxs-lookup"><span data-stu-id="336fc-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_type de PHY dot11 \_ \_ DSSS**</span><span class="sxs-lookup"><span data-stu-id="336fc-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-115">Spécifie un type d’étalement du spectre à séquence directe (DSSS).</span><span class="sxs-lookup"><span data-stu-id="336fc-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**\_irbaseband du \_ type de PHY dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-117">Spécifie un type de PHY de bande de bande infrarouge (IR).</span><span class="sxs-lookup"><span data-stu-id="336fc-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**\_type du PHY dot11 \_ \_ OFDM**</span><span class="sxs-lookup"><span data-stu-id="336fc-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-119">Spécifie un type de multiplexage de division de fréquence orthogonale (OFDM).</span><span class="sxs-lookup"><span data-stu-id="336fc-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="336fc-120">802.11 un appareil peut utiliser OFDM.</span><span class="sxs-lookup"><span data-stu-id="336fc-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**\_hrdsss du \_ type de PHY dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-122">Spécifie un type de PHY (HRDSSS) DSSS à haut débit.</span><span class="sxs-lookup"><span data-stu-id="336fc-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_type d' \_ ERP du type de PHY dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-124">Spécifie un type de PHY à taux étendu (ERP).</span><span class="sxs-lookup"><span data-stu-id="336fc-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="336fc-125">les appareils 802.11 g peuvent utiliser ERP.</span><span class="sxs-lookup"><span data-stu-id="336fc-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_type de PHY dot11 \_ \_ HT**</span><span class="sxs-lookup"><span data-stu-id="336fc-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-127">Spécifie le type de PHY 802.11 n.</span><span class="sxs-lookup"><span data-stu-id="336fc-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**\_VHT du \_ type de PHY dot11 \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-129">Spécifie le type de PHY AC 802.11.</span><span class="sxs-lookup"><span data-stu-id="336fc-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="336fc-130">Il s’agit du type PHY à débit très élevé spécifié dans IEEE 802.11 AC.</span><span class="sxs-lookup"><span data-stu-id="336fc-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="336fc-131">Cette valeur est prise en charge sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="336fc-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="336fc-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_démarrage du \_ fabricant de type de PHY dot11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-133">Spécifie le début de la plage utilisée pour définir les types PHY qui sont développés par un fournisseur de matériel indépendant (IHV).</span><span class="sxs-lookup"><span data-stu-id="336fc-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="336fc-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**\_type de PHY de type dot11 \_ \_ \_ fin**</span><span class="sxs-lookup"><span data-stu-id="336fc-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="336fc-135">Spécifie le début de la plage utilisée pour définir les types PHY qui sont développés par un fournisseur de matériel indépendant (IHV).</span><span class="sxs-lookup"><span data-stu-id="336fc-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="336fc-136">Notes</span><span class="sxs-lookup"><span data-stu-id="336fc-136">Remarks</span></span>

<span data-ttu-id="336fc-137">Un IHV peut attribuer une valeur pour ses types PHY propriétaires à partir du **\_ fabricant du type de PHY dot11 \_ \_ \_ Démarrer** par le biais du **type de \_ PHY dot11 \_ \_ \_ end**.</span><span class="sxs-lookup"><span data-stu-id="336fc-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="336fc-138">Le IHV doit attribuer un nombre unique à partir de cette plage pour chacun de ses types PHY propriétaires.</span><span class="sxs-lookup"><span data-stu-id="336fc-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="336fc-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="336fc-139">Requirements</span></span>



| <span data-ttu-id="336fc-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="336fc-140">Requirement</span></span> | <span data-ttu-id="336fc-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="336fc-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="336fc-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="336fc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="336fc-143">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="336fc-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="336fc-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="336fc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="336fc-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="336fc-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="336fc-146">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="336fc-146">Redistributable</span></span><br/>          | <span data-ttu-id="336fc-147">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="336fc-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="336fc-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="336fc-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="336fc-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="336fc-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336fc-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="336fc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336fc-151">**\_attributs d’association WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="336fc-152">**capacité de l' \_ interface WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="336fc-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




