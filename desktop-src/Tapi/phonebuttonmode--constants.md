---
description: Les \_ constantes d’indicateur de bit PHONEBUTTONMODE décrivent les classes Button.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Constantes PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761301"
---
# <a name="phonebuttonmode_-constants"></a>\_Constantes PHONEBUTTONMODE

Les constantes d’indicateur de bit **PHONEBUTTONMODE \_** décrivent les classes Button.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_appel PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Le bouton est assigné à une apparence d’appel.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**\_affichage PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Le bouton est un bouton « Soft » associé à l’affichage du téléphone. Un ensemble de téléphones peut avoir zéro ou plusieurs boutons d’affichage.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ factice**
</dt> <dd> <dl> <dt>



Cette valeur est utilisée pour décrire une position de bouton/lampe qui n’a pas de bouton correspondant, mais qui a uniquement un feu.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_fonctionnalité PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Le bouton est affecté à la demande de fonctionnalités à partir du commutateur, telles que la suspension, la Conférence et le transfert.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**\_pavé numérique PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Le bouton est l’un des douze boutons du clavier, de 0 à 9, de « \* » et de «» \# .


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ local**
</dt> <dd> <dl> <dt>



Le bouton est un bouton de fonction local, tel que muet ou contrôle de volume.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Ce type d’énumération est utilisé dans la structure de données [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) pour décrire la signification associée aux boutons du téléphone.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




