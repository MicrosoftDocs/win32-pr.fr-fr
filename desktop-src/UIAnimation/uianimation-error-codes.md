---
title: Windows Codes d’erreur d’animation (winerror. h)
description: si une erreur se produit, Windows Animation retourne un code en tant que valeur HRESULT. cette section fournit la liste des codes d’erreur spécifiques à Windows Animation. Pour obtenir la liste des codes d’erreur COM généraux, consultez Codes d’erreur COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192471"
---
# <a name="windows-animation-error-codes"></a>Windows Codes d’erreur d’animation

si une erreur se produit, Windows Animation retourne un code en tant que valeur **HRESULT** . cette section fournit la liste des codes d’erreur spécifiques à Windows Animation. Pour obtenir la liste des codes d’erreur COM généraux, consultez [codes d’erreur com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**échec de la création de l’interface utilisateur \_ \_ \_**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Impossible de créer l’objet.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**arrêt de l’interface utilisateur \_ E \_ \_ appelé**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



La méthode [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) a été appelée sur le gestionnaire d’animations, provoquant l’arrêt du gestionnaire d’animations, ainsi que toutes les variables d’animation et les storyboards qu’il a créées pour être libérés.

> [!Note]  
> Aucune méthode ne peut être appelée sur un objet d’animation après l' [**arrêt**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**\_ \_ réentrance non conforme de l’interface utilisateur \_**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Cette méthode ne peut pas être appelée pendant ce type de rappel.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**\_objet UI \_ E \_ sealed**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Cet objet ayant été scellé, cette modification n’est plus autorisée.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_valeur UI \_ E \_ non \_ définie**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



La valeur demandée n’a jamais été définie et ne peut donc pas être récupérée.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_valeur UI \_ E \_ non \_ déterminée**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



La valeur demandée ne peut pas être déterminée.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**sortie de l’interface utilisateur \_ \_ non valide \_**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Un rappel a retourné un paramètre de sortie non valide.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**interface utilisateur \_ E \_ booléenne \_ attendue**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Un rappel a retourné un code de réussite autre que S \_ OK ou s \_ false.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**interface utilisateur \_ E \_ autre \_ propriétaire**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Un paramètre qui doit être détenu par cet objet est détenu par un autre objet.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ correspondance ambiguë de l’interface utilisateur \_**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Plus d’un élément correspond aux critères de recherche.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**dépassement de capacité de l’interface utilisateur \_ E \_ FP \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Un dépassement de capacité à virgule flottante s’est produit.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**THREAD d’interface utilisateur \_ \_ incorrect \_**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Cette méthode peut uniquement être appelée à partir du thread qui a créé l’objet.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**Storyboard de l’interface utilisateur \_ \_ \_ actif**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



La table de montage séquentiel est actuellement dans la planification.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**IU \_ E \_ Storyboard \_ non \_ lu**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



Le Storyboard n’est pas en train de fonctionner.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**IMAGE clé de démarrage de l’interface utilisateur \_ \_ après la \_ \_ \_ fin**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



L’image clé de début peut se produire après l’image clé de fin.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**\_ \_ image clé de fin UI E \_ \_ non \_ déterminée**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Il se peut qu’il ne soit pas possible de déterminer l’heure de fin de l’image clé lorsque l’image clé de démarrage est atteinte.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_ \_ chevauchement des boucles UI E \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Deux parties répétées d’une table de montage séquentiel peuvent se chevaucher.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**TRANSITION d’interface utilisateur \_ E \_ \_ déjà \_ utilisée**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



La transition a déjà été ajoutée à un autre Storyboard ou a été ajoutée à une table de montage séquentiel qui a terminé la diffusion et a été libérée.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**\_transition UI \_ E \_ non \_ dans le \_ Storyboard**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



La transition n’a pas été ajoutée à une table de montage séquentiel.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**\_transition UI \_ E \_ eclipsed**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



La transition peut Eclipse le début d’une autre transition dans le Storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**heure de l’interface utilisateur \_ E \_ avant la \_ \_ dernière \_ mise à jour**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



L’heure spécifiée est antérieure à l’heure passée à la dernière mise à jour.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_ \_ client du minuteur de l’interface utilisateur \_ \_ déjà \_ connecté**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Ce client est déjà connecté à un minuteur.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                       |
| En-tête<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Référence d’animation](windows-animation-reference.md)
</dt> </dl>

 

