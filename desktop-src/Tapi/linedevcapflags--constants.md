---
description: Les \_ constantes d’indicateur de bit LINEDEVCAPFLAGS sont une collection de valeurs booléennes qui décrivent différentes fonctionnalités de périphérique en ligne.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761716"
---
# <a name="linedevcapflags_-constants"></a>\_Constantes LINEDEVCAPFLAGS

Les constantes d’indicateur de bit **LINEDEVCAPFLAGS \_** sont une collection de valeurs booléennes qui décrivent différentes fonctionnalités de périphérique en ligne.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indique si les hubs d’appel sont pris en charge sur cette ligne. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indique si le suivi des concentrateurs d’appels est pris en charge sur cette ligne. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Spécifie ce qui se produit lorsqu’une ligne ouverte est fermée pendant que l’application appelle active sur la ligne. Si la **valeur est true**, le fournisseur de services supprime (efface) tous les appels actifs sur la ligne lorsque la dernière application qui a ouvert la ligne la ferme avec [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Si la **valeur est false**, le fournisseur de services ne supprime pas les appels actifs dans de tels cas. Au lieu de cela, les appels restent actifs et sous le contrôle des périphériques externes. Un fournisseur de services définit généralement ce bit sur **false** s’il existe un autre périphérique qui peut garder l’appel actif. par exemple, si une ligne analogique a l’ordinateur et que l’ensemble de téléphones se connectent directement à ces derniers dans une configuration de ligne de partie, le téléphone offhook garde automatiquement l’appel actif même après la mise sous tension de l’ordinateur.

Les applications doivent vérifier cet indicateur pour déterminer s’il faut avertir l’utilisateur (avec une boîte de dialogue OK/Annuler) que les appels actifs seront perdus.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Spécifie si les appels effectués sur des adresses différentes sur cette ligne peuvent être Conférence.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Ces indicateurs indiquent si le modificateur de chaîne de numérotation « $ », « @ » ou « W » est pris en charge pour un périphérique de ligne donné. Elle a la **valeur true** si le modificateur est pris en charge ; Sinon, **false**. Le «  ? » (inviter l’utilisateur à continuer la numérotation) n’est jamais pris en charge par un périphérique en ligne. Ces indicateurs permettent à une application de déterminer à l’avance quels modificateurs entraîneraient la génération d’un LINEERR. L’application a le choix de préanalyser des chaînes de numérotation pour les caractères non pris en charge ou de passer directement la chaîne « brute » de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) au fournisseur dans le cadre de fonctions telles que [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) et laisser la fonction générer une erreur pour lui indiquer quel modificateur non pris en charge se produit en premier dans la chaîne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Spécifie si les éléments d’informations de compatibilité de haut niveau sont pris en charge sur cette ligne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Spécifie si les éléments d’informations de compatibilité de bas niveau sont pris en charge sur cette ligne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Spécifie si les opérations de contrôle de média sont disponibles pour les appels à cette ligne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**\_MSP LINEDEVCAPFLAGS**
</dt> <dd> <dl> <dt>



Indique si un fournisseur de services de média (MSP) est associé à la ligne. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Spécifie si [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ou [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) est en mesure de traiter plusieurs adresses à la fois (comme pour le multiplexage inverse).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Indique si [les interfaces spécifiques au fournisseur](./provider-specific-interfaces.md) ont été implémentées. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

