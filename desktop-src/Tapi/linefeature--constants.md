---
description: Les \_ constantes LINEFEATURE répertorient les opérations qui peuvent être appelées sur une ligne à l’aide de cette API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526890"
---
# <a name="linefeature_-constants"></a>\_Constantes LINEFEATURE

Les **\_ constantes LINEFEATURE** répertorient les opérations qui peuvent être appelées sur une ligne à l’aide de cette API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Les opérations spécifiques au périphérique peuvent être utilisées sur la ligne.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**
</dt> <dd> <dl> <dt>



Les fonctionnalités spécifiques au périphérique peuvent être utilisées sur la ligne.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ vers l’avant**
</dt> <dd> <dl> <dt>



Le transfert de toutes les adresses peut être utilisé sur la ligne.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (avec une adresse de destination vide) peut être utilisée pour activer la fonctionnalité ne pas déranger sur toutes les adresses sur la ligne. LINEFEATURE \_ Forward sera également défini. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) peut être utilisée pour transférer des appels sur toute adresse sur la ligne à d’autres nombres. LINEFEATURE \_ Forward sera également défini. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Un appel sortant peut être placé sur cette ligne à l’aide d’une adresse non spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**
</dt> <dd> <dl> <dt>



La fonction [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) peut être appelée sur le périphérique de ligne. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Le contrôle de média peut être défini sur cette ligne.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Les modes de terminal pour cette ligne peuvent être définis.

> [!Note]  
> Si aucun des nouveaux bits « FORWARD » modifiés n’est défini dans le membre **dwLineFeatures** dans [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , mais que le \_ bit de transfert LINEFEATURE est défini, l’un des modes Forward peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Les \_ constantes LINEFEATURE sont utilisées dans [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (retourné par [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)). [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) signale, pour une ligne donnée, les fonctionnalités de ligne qui peuvent être appelées alors que la ligne est à l’état actuel. Une application effectue cette détermination de manière dynamique après modification de l’état de ligne, généralement due à des activités d’adresse ou d’appel sur la ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




