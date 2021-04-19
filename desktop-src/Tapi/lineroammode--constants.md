---
description: Les \_ constantes d’indicateur de bit LINEROAMMODE décrivent l’état d’itinérance d’un périphérique de ligne.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Constantes LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530475"
---
# <a name="lineroammode_-constants"></a>\_Constantes LINEROAMMODE

Les constantes d’indicateur de bit **LINEROAMMODE \_** décrivent l’état d’itinérance d’un périphérique de ligne.

<dl> <dt>

<span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**Page d’LINEROAMMODE \_**
</dt> <dd> <dl> <dt>



La ligne est connectée au nœud réseau d’hébergement.


</dt> </dl> </dd> <dt>

<span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE \_ itinéranta**
</dt> <dd> <dl> <dt>



La ligne est connectée à l’itinérance : un opérateur et les appels sont facturés en conséquence.


</dt> </dl> </dd> <dt>

<span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE \_ ROAMB**
</dt> <dd> <dl> <dt>



La ligne est connectée au transporteur itinérant-B et les appels sont facturés en conséquence.


</dt> </dl> </dd> <dt>

<span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE \_ INdispo**
</dt> <dd> <dl> <dt>



Le mode itinérant n’est pas disponible et ne sera pas connu.


</dt> </dl> </dd> <dt>

<span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Le mode itinérant est actuellement inconnu, mais peut devenir connu ultérieurement.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




