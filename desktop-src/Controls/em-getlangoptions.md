---
title: Message EM_GETLANGOPTIONS (RichEdit. h)
description: Obtient les paramètres d’option d’un contrôle RichEdit pour l’éditeur de méthode d’entrée (IME) et la prise en charge des langues asiatiques.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27254ccb10093059eb9161410f4e25efdc59306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843165"
---
# <a name="em_getlangoptions-message"></a>\_Message GETLANGOPTIONS em

Obtient les paramètres d’option d’un contrôle RichEdit pour l’éditeur de méthode d’entrée (IME) et la prise en charge des langues asiatiques.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les paramètres de langue IME et asiatiques, qui peuvent correspondre à zéro, une ou plusieurs des valeurs suivantes.



| Code de retour                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**autopolice IMF \_**</dt> </dl>                    | Si cet indicateur est défini, le contrôle modifie automatiquement les polices lorsque l’utilisateur passe explicitement à une disposition de clavier différente. Il est utile de désactiver la **\_ police** active de IMF pour les polices Unicode universelles. Cette option est activée par défaut (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**\_AUTOFONTSIZEADJUST IMF**</dt> </dl>          | Si cet indicateur est défini, le contrôle met à l’échelle les tailles de police liées aux polices à partir de la taille du point d’insertion en fonction du script. Par exemple, les polices asiatiques sont légèrement supérieures à celles de l’Ouest. Cette option est activée par défaut (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**autokeyboard de IMF \_**</dt> </dl>                | Si cet indicateur est défini, le contrôle modifie automatiquement la disposition du clavier lorsque l’utilisateur passe explicitement à une autre police ou lorsque l’utilisateur modifie explicitement le point d’insertion à un nouvel emplacement dans le texte. Est activé automatiquement pour les contrôles bidirectionnels. Pour tous les autres contrôles, il est désactivé par défaut. Cette option est désactivée par défaut (0).<br/>                                 |
| <dl> <dt>**\_DISABLEAUTOBIDIAUTOKEYBOARD IMF**</dt> </dl> | **Windows 8**: si cet indicateur est défini, le contrôle utilise une logique indépendante de la langue pour le basculement automatique du clavier. Cette option est désactivée par défaut (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_DUALFONT IMF**</dt> </dl>                    | Si cet indicateur est défini, le contrôle utilise le mode à double police. Utilisé pour la prise en charge des langues asiatiques. Le contrôle utilise une police anglaise pour le texte ASCII et une police asiatique pour le texte asiatique. Cette option est activée par défaut (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**\_IMEALWAYSSENDNOTIFY IMF**</dt> </dl>         | Cet indicateur contrôle la manière dont le contrôle RichEdit notifie le client lors de la composition de l’IME : <br/> 0 : aucun en- [ \_ changement](en-change.md) ou notifications en [ \_ selChange](en-selchange.md) lors d’un état indéterminé. Envoyer une notification lorsque la dernière chaîne est entrée. Il s’agit de la valeur par défaut.<br/> 1 : envoyer les événements en [ \_ modification](en-change.md) et en [ \_ selChange](en-selchange.md) lors de l’état indéterminé.<br/> |
| <dl> <dt>**\_IMECANCELCOMPLETE IMF**</dt> </dl>           | Cet indicateur détermine la façon dont le contrôle utilise la chaîne de composition d’un IME si l’utilisateur l’annule. Si cet indicateur est défini, le contrôle ignore la chaîne de composition. Si cet indicateur n'est pas défini, le contrôle utilise la chaîne de composition comme chaîne de résultat. Cette option est désactivée par défaut (0).<br/>                                                                                                              |
| <dl> <dt>**\_NOIMPLICITLANG IMF**</dt> </dl>              | **Windows 8**: si cet indicateur est défini, désactivez l’enregistrement de l’entrée au clavier à l’aide de la langue du clavier et en veillant à ce que les IDss de langue non orientale soient compatibles avec le répertoire de caractères. Cette option est désactivée par défaut (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**\_NOKBDLIDFIXUP IMF**</dt> </dl>               | **Windows 8**: si cet indicateur est défini, le contrôle RichEdit désactive le marquage de la langue du clavier sur un contrôle vide. Cette option est désactivée par défaut (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_vérification orthographique d’IMF**</dt> </dl>               | **Windows 8**: si cet indicateur est défini, le contrôle RichEdit active la vérification orthographique. Cette option est désactivée par défaut (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_TKBAUTOCORRECTION IMF**</dt> </dl>           | **Windows 8**: si cet indicateur est défini, activez la correction automatique du clavier tactile. Cette option est désactivée par défaut (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**\_TKBPREDICTION IMF**</dt> </dl>               | **Windows 10**: ignoré.<br/> **Windows 8**: si cet indicateur est défini, le contrôle RichEdit active la prédiction de clavier tactile. Cette option est désactivée par défaut (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**\_UIFONTS IMF**</dt> </dl>                     | Utilisez les polices par défaut de l’interface utilisateur. Cette option est désactivée par défaut (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Notes

L’indicateur de **\_ police de caractères IMF** est défini par défaut. Les **indicateurs \_ autokeyboard** et **IMF \_ IMECANCELCOMPLETE** de IMF sont effacés par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETLANGOPTIONS em**](em-setlangoptions.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





