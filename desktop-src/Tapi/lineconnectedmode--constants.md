---
description: Les \_ constantes d’indicateur de bit LINECONNECTEDMODE décrivent différents sous-États d’un appel connecté.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542614"
---
# <a name="lineconnectedmode_-constants"></a>\_Constantes LINECONNECTEDMODE

Les constantes d’indicateur de bit **LINECONNECTEDMODE \_** décrivent différents sous-États d’un appel connecté. Un mode est disponible en tant qu’État d’appel à l’application après que l’état d’appel passe à Connected, et dans la ligne \_ CALLSTATE message indiquant que l’appel se trouve dans LINECALLSTATE \_ connected. Ces valeurs sont utilisées lorsque l’appel est sur une adresse partagée (Bridged) avec d’autres stations (pour plus d’informations, consultez [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique. Les **\_ constantes LINECONNECTEDMODE** ont les valeurs suivantes :

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ actif**
</dt> <dd> <dl> <dt>



Indique que l’appel est connecté à la station active (la station active est un participant à l’appel). Si le mode d’état de l’appel est 0 (zéro), l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont). Le mode peut basculer entre actif et inactif pendant un appel si l’utilisateur rejoint et quitte l’appel via une action manuelle. Dans une telle situation, une opération de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou de [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) peut ne pas réellement supprimer l’appel ou le mettre en attente, car l’état des autres stations sur l’appel peut être régi (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participent n’est pas possible). au lieu de cela, l’appel peut être remplacé par le mode inactif s’il reste connecté sur d’autres stations.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**
</dt> <dd> <dl> <dt>



Indique que la station est un participant actif dans l’appel, mais que le tiers distant a passé l’appel en attente (l’autre partie considère que l’appel est à l’État onHold). Normalement, ces informations sont disponibles uniquement lorsque les deux points de terminaison de l’appel se trouvent dans le même domaine de basculement. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmé**
</dt> <dd> <dl> <dt>



Indique que le fournisseur de services a reçu une notification affirmative indiquant que l’appel est passé à l’état connecté (par exemple, via la surveillance des réponses ou des mécanismes similaires). Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ inactif**
</dt> <dd> <dl> <dt>



Indique que l’appel est actif sur une ou plusieurs autres stations, mais que la station active n’est pas un participant à l’appel. Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont). Un appel dans l’état inactif peut être joint à l’aide de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). De nombreuses opérations qui sont valides dans les appels de l’État CONNECTed peuvent être impossibles dans le mode inactif, par exemple la surveillance des tons et des chiffres, car la station ne participe pas réellement à l’appel ; la surveillance est généralement suspendue (même si elle n’est pas annulée) pendant que l’appel est en mode inactif.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**
</dt> <dd> <dl> <dt>



Indique que la station n’est pas un participant actif dans l’appel et que le tiers distant a passé l’appel en attente. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Non extensible. Tous les 32 bits sont réservés.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINECONNECTEDMODE qui ne sont pas prises en charge sur la version négociée. Les applications qui ne sont pas Cognizant de LINECONNECTEDMODE \_ supposent probablement qu’un appel qui se trouve dans LINECALLSTATE \_ connecté est dans LINECONNECTEDMODE \_ actif.

Les \_ \_ valeurs inactives LINECONNECTEDMODE actives et LINECONNECTEDMODE sont utilisées lorsque l’appel est sur une adresse partagée avec d’autres stations (Bridged, voir [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique. Si le mode d’état d’appel connecté est « actif », cela signifie que l’appel est connecté à la station active (la station actuelle est un participant à l’appel). Si le mode d’état de l’appel est « inactif », l’appel est actif sur une ou plusieurs autres stations, mais la station actuelle n’est pas un participant à l’appel. Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est « active » (ce qui serait la situation sur une adresse sans pont). Le mode peut basculer entre actif et inactif pendant un appel si l’utilisateur rejoint et quitte l’appel via une action manuelle.

Dans une telle situation, une opération de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou de [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) peut ne pas réellement supprimer l’appel ou le mettre en attente, car l’état des autres stations sur l’appel peut être régi (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participent n’est pas possible); au lieu de cela, l’appel peut simplement être remplacé par le mode inactif s’il reste connecté sur d’autres stations. Un appel dans l’état inactif peut être joint à l’aide de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).

De nombreuses opérations qui sont valides dans les appels de l’État Connected peuvent être impossibles dans le mode inactif, par exemple la surveillance des tons et des chiffres, car la station ne participe pas réellement à l’appel ; la surveillance est généralement suspendue (même si elle n’est pas annulée) pendant que l’appel est en mode inactif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




