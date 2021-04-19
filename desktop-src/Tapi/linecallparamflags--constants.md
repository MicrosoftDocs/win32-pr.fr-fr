---
description: Les \_ constantes LINECALLPARAMFLAGS décrivent différents indicateurs d’État sur un appel.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539193"
---
# <a name="linecallparamflags_-constants"></a>\_Constantes LINECALLPARAMFLAGS

Les constantes **LINECALLPARAMFLAGS \_** décrivent différents indicateurs d’État sur un appel.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ BLOCKID**
</dt> <dd> <dl> <dt>



L’identité de l’expéditeur doit être masquée (ID de l’appelant du bloc).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Le téléphone du tiers appelé doit être automatiquement pris offhook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inactif**
</dt> <dd> <dl> <dt>



L’appel doit être issu de l’apparence d’un appel inactif et ne pas joindre un appel en cours. Lors de l’utilisation de la fonction [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , si la \_ valeur d’inactivité LINECALLPARAMFLAGS n’est pas définie et qu’il existe un appel sur la ligne, la fonction s’arrête dans l’appel existant si nécessaire pour effectuer le nouvel appel. S’il n’existe aucun appel, la fonction effectue le nouvel appel comme spécifié.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Ce bit est utilisé uniquement conjointement avec [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) et [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). L’adresse à conférence avec l’appel en cours est spécifiée dans le membre **TargetAddress** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). L’appel de consultation ne dessine pas physiquement la tonalité à partir du commutateur, mais il progresse à travers différents États d’établissement d’appels (par exemple, la numérotation, la procédure). Lorsque l’appel de consultation atteint l’état connecté, la Conférence est automatiquement établie. l’appel d’origine, qui était resté à l’état connecté, passe à l’État Conférence ; l’appel de consultation passe à l’État Conférence ; le hConfCall passe à l’état connecté. Si l’appel de consultation échoue (passe à l’état déconnecté suivi de Idle), le hConfCall passe également à l’état inactif, et l’appel d’origine (qui peut être une conférence existante, dans le cas de **linePrepareAddToConference**) reste dans l’état connecté. Le tiers ou les tiers d’origine ne perçoivent jamais l’appel onHold. Cette fonctionnalité est souvent utilisée pour ajouter un superviseur à un appel de l’agent ACD lorsque cela est nécessaire pour surveiller les interactions avec un appelant irate.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Ce bit est utilisé uniquement conjointement avec [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Elle combine le fonctionnement de **lineSetupTransfer** suivi de [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) sur l’appel de consultation en une seule étape. L’adresse à composer est spécifiée dans le membre **TargetAddress** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). L’appel d’origine est placé dans l’état *onholdpendingtransfer* , tout comme si **lineSetupTransfer** était appelé normalement, et l’appel de consultation est établi normalement. L’application doit toujours appeler [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) pour appliquer le transfert. Cette fonctionnalité est souvent utilisée lors de l’appel d’un transfert à partir d’un serveur via un lien de contrôle d’appel tiers, car ces liens ne prennent pas en charge le processus normal en deux étapes.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Le téléphone de l’expéditeur doit être automatiquement pris offhook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**
</dt> <dd> <dl> <dt>



Ce bit est utilisé uniquement lors du placement d’un appel sur une adresse avec la fonctionnalité de numérotation prédictive (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER est activé dans le membre **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). Le bit doit être activé pour activer la progression des appels et/ou les fonctionnalités d’analyse des appareils multimédias de l’appareil. Si ce bit n’est pas activé, l’appel est placé sans la progression de l’appel ou la surveillance du type de média, et aucun transfert automatique n’est initié en fonction de l’état de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ sécurisé**
</dt> <dd> <dl> <dt>



L’appel doit être configuré comme sécurisé.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




