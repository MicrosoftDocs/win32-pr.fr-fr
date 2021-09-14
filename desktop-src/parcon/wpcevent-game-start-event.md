---
description: Événement par utilisateur généré par le système lors d’une tentative de lancement d’un jeu. Différentes valeurs de champ sont fournies par le système de l’Explorateur de jeux et les métadonnées correspondantes fournies par les jeux pris en charge.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: Événement WPCEVENT_GAME_START (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235632"
---
# <a name="wpcevent_game_start-event"></a>Événement de démarrage du \_ jeu WPCEVENT \_

Événement par utilisateur généré par le système lors d’une tentative de lancement d’un jeu. Différentes valeurs de champ sont fournies par le système de l’Explorateur de jeux et les métadonnées correspondantes fournies par les jeux pris en charge.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppID* 
</dt> <dd>

GUID du jeu qui a tenté de démarrer.

</dd> <dt>

*InstanceID* 
</dt> <dd>

GUID utilisé pour faire la distinction entre plusieurs installations.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Chaîne de version pour le jeu.

</dd> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès au répertoire principal de l’installation du jeu.

</dd> <dt>

*Évaluation* 
</dt> <dd>

Chaîne qui identifie le niveau d’évaluation d’un jeu dans le système d’évaluation.

</dd> <dt>

*RatingSystem* 
</dt> <dd>

GUID qui identifie le système d’évaluation actuel auquel le niveau d’évaluation s’applique.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*DescCount* 
</dt> <dd>

Nombre de descripteurs présents dans le champ de descripteur.

</dd> <dt>

*Descripteur* 
</dt> <dd>

Chaîne délimitée qui contient des descripteurs qui sont bloqués pour le jeu.

</dd> <dt>

*ELECTRIQUE* 
</dt> <dd>

ID de processus du jeu, utilisé pour mettre en corrélation l’arrêt du processus par un shim.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




