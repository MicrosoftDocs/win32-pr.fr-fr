---
title: BITS_COST_STATE (Bits5d \_ 0. h)
description: L’énumération de l’état du coût des BITS \_ \_ définit les valeurs constantes qui spécifient l’état du coût des bits.
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: 88fb0b949fb06a6e1eb6e14cdf55c8d54d9ab33c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942246"
---
# <a name="bits_cost_state"></a>\_État du coût des bits \_

Définit des constantes qui spécifient l’état du coût des BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**État du coût des BITS non \_ \_ \_ restreint**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**\_ \_ utilisation limitée de l’état du coût du service bits \_ \_ \_ inconnue**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**État du coût des BITS en \_ \_ dessous du \_ \_ seuil**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**État du coût des BITS à \_ \_ proximité du \_ \_ Cap**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**État du coût du service BITS \_ \_ \_ OVERCAP \_ facturé**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**\_État du coût bits \_ \_ OVERCAP \_ limité**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_ \_ \_ utilisation \_ basée sur l’état du coût du service bits**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**OPTION de coût des BITS \_ \_ ignorer la \_ \_ congestion**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**État du coût des BITS \_ \_ \_ réservé**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Réservé.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**transfert de l’état du coût du service BITS \_ \_ \_ \_ non \_ itinérant**
</dt> <dd> <dl> <dt>

(BITS \_ OPTION de coût \_ \_ Ignorer les bits d’encombrement coût des bits \_ \| \_ \_ \_ basés sur l’utilisation de l' \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ État du coût des bits limités OVERCAP État du coût de l’état du coût des bits de poids proche de l’état du coût des bits d’extrémité 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**transfert de l’état du coût du service BITS \_ \_ \_ \_ non \_ supplément**
</dt> <dd> <dl> <dt>

(BITS \_ OPTION de coût \_ \_ Ignorer les bits de \_ congestion utilisation de \| l’état du coût \_ \_ \_ \_ bits basés sur l' \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ État du coût des bits limités OVERCAP État du coût à proximité de bits
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**\_standard de \_ transfert d’État du coût du service \_ \_**
</dt> <dd> <dl> <dt>

(BITS \_ OPTION de coût ignorer les bits d’encombrement coût des bits basés sur l’utilisation de l’état du coût OVERCAP de l’état du coût des bits limités État du coût \_ \_ \_ \| \_ \_ \_ inférieur à \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ l’utilisation limitée état \_ \_ \| \_ \_ \_ du coût bits inconnu État du coût non restreint) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**transfert de l’état du coût du service non \_ \_ \_ \_ restreint**
</dt> <dd> <dl> <dt>

(BITS \_ OPTION de coût \_ \_ Ignorer les bits d' \_ encombrement État du \| \_ coût OVERCAP les bits de \_ \_ \_ limitation État du coût non \| \_ \_ \_ restreint)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**transfert de l’état du coût du service BITS \_ \_ \_ \_ toujours**
</dt> <dd> <dl> <dt>

(BITS \_ OPTION de coût \_ \_ Ignorer les bits de congestion état \_ \| \_ coût état des \_ \_ bits itinérants utilisation de l’État coût des bits \| \_ \_ \_ \_ basés sur l' \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ État du coût OVERCAP de l’état du coût des bits de charge OVERCAP État du coût
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Bits5 \_ 0. h (inclure bits. h)</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





