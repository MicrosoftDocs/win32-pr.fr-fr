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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011609"
---
# <a name="dot11_phy_type-enumeration"></a>\_ \_ Énumération de type PHY DOT11

L’énumération du **\_ \_ type de PHY DOT11** définit un type de média 802,11 PHY et.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_type de PHY dot11 \_ \_ inconnu**
</dt> <dd>

Spécifie un type PHY inconnu ou non initialisé.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**\_ \_ type de PHY dot11 \_ any**
</dt> <dd>

Spécifie un type PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**\_FHSS du \_ type de PHY dot11 \_**
</dt> <dd>

Spécifie un PHY-Spectrum (FHSS) à saut de fréquence. les appareils Bluetooth peuvent utiliser FHSS ou une adaptation de FHSS.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**\_type de PHY dot11 \_ \_ DSSS**
</dt> <dd>

Spécifie un type d’étalement du spectre à séquence directe (DSSS).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**\_irbaseband du \_ type de PHY dot11 \_**
</dt> <dd>

Spécifie un type de PHY de bande de bande infrarouge (IR).

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**\_type du PHY dot11 \_ \_ OFDM**
</dt> <dd>

Spécifie un type de multiplexage de division de fréquence orthogonale (OFDM). 802.11 un appareil peut utiliser OFDM.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**\_hrdsss du \_ type de PHY dot11 \_**
</dt> <dd>

Spécifie un type de PHY (HRDSSS) DSSS à haut débit.

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_type d' \_ ERP du type de PHY dot11 \_**
</dt> <dd>

Spécifie un type de PHY à taux étendu (ERP). les appareils 802.11 g peuvent utiliser ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**\_type de PHY dot11 \_ \_ HT**
</dt> <dd>

Spécifie le type de PHY 802.11 n.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**\_VHT du \_ type de PHY dot11 \_**
</dt> <dd>

Spécifie le type de PHY AC 802.11. Il s’agit du type PHY à débit très élevé spécifié dans IEEE 802.11 AC.

cette valeur est prise en charge sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_démarrage du \_ fabricant de type de PHY dot11 \_ \_**
</dt> <dd>

Spécifie le début de la plage utilisée pour définir les types PHY qui sont développés par un fournisseur de matériel indépendant (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**\_type de PHY de type dot11 \_ \_ \_ fin**
</dt> <dd>

Spécifie le début de la plage utilisée pour définir les types PHY qui sont développés par un fournisseur de matériel indépendant (IHV).

</dd> </dl>

## <a name="remarks"></a>Notes

Un IHV peut attribuer une valeur pour ses types PHY propriétaires à partir du **\_ fabricant du type de PHY dot11 \_ \_ \_ Démarrer** par le biais du **type de \_ PHY dot11 \_ \_ \_ end**. Le IHV doit attribuer un nombre unique à partir de cette plage pour chacun de ses types PHY propriétaires.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_attributs d’association WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**capacité de l' \_ interface WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




