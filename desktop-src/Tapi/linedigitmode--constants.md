---
description: Les \_ constantes LINEDIGITMODE décrivent différents types de génération de chiffre inbande.
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: Constantes LINEDIGITMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544069"
---
# <a name="linedigitmode_-constants"></a>\_Constantes LINEDIGITMODE

Les constantes **LINEDIGITMODE \_** décrivent différents types de génération de chiffre inbande.

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**\_DTMF LINEDIGITMODE**
</dt> <dd> <dl> <dt>



Utilise des tonalités DTMF pour signaler des chiffres. Les chiffres valides sont 0 à 9, « \* », « » \# , «A », « B », « C » et « d ».


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**LINEDIGITMODE \_ DTMFEND**
</dt> <dd> <dl> <dt>



Utilise des tonalités DTMF pour signaler des chiffres et détecter les bords inversés. Les chiffres valides sont 0 à 9, « \* », « » \# , «A », « B », « C » et « d ».


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**\_impulsion LINEDIGITMODE**
</dt> <dd> <dl> <dt>



Utilise des séquences d’impulsions rotatives pour signaler des chiffres. Les chiffres valides sont compris entre 0 et 9.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Un mode digit peut être spécifié lors de la génération ou de la détection de chiffres. Notez que les chiffres d’impulsions sont générés en créant et en cassant le circuit de boucle local. Ces impulsions sont absorbées par le commutateur. L’extrémité distante observe simplement cela comme une série de clics audio à la bande. La détection des chiffres envoyés comme impulsions doit donc être en mesure de détecter ces séquences de 1 à 10 clics audibles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




