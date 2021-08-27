---
description: La \_ constante d’indicateur de bit LINETRANSLATEOPTION décrit une option utilisée par la traduction d’adresses.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Constantes LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d1cc9f3d7798dda9dd5bb69817ccfac64ae88fbc45fccccd59563cc24614d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073019"
---
# <a name="linetranslateoption_-constants"></a>\_Constantes LINETRANSLATEOPTION

La constante d’indicateur de bit **LINETRANSLATEOPTION \_** décrit une option utilisée par la traduction d’adresses.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



Si une chaîne d’appel d’annulation est définie pour l’emplacement, la définition de ce bit entraînera l’insertion de cette chaîne au début de la chaîne de numérotation. Ce mode est couramment utilisé par les applications de télécopie et de modems de données pour empêcher l’interruption des appels en signalant des signaux d’attente. Si aucune chaîne d’appel d’annulation n’est définie pour l’emplacement, ce bit n’a aucun effet. Notez que les applications qui utilisent ce bit sont recommandées pour définir également le \_ bit sécurisé LINECALLPARAMFLAGS dans le membre **dwCallParamFlags** de la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passée à [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) via le paramètre *lpCallParams* , de sorte que si le périphérique de ligne utilise un mécanisme autre que des chiffres à composer pour supprimer les interruptions d’appel, ce mécanisme sera appelé.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



La carte d’appel par défaut doit être remplacée par une carte spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



Cette option force la traduction de l’adresse (nombre) en longue distance.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



Cette option force la conversion du nombre (adresse) en local.


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

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




