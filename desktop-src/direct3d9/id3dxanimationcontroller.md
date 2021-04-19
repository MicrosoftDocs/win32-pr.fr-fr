---
description: Cette interface est utilisée pour contrôler les fonctionnalités d’animation, en connectant les jeux d’animations aux frames de transformation animés.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: Interface ID3DXAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535189"
---
# <a name="id3dxanimationcontroller-interface"></a>Interface ID3DXAnimationController

Cette interface est utilisée pour contrôler les fonctionnalités d’animation, en connectant les jeux d’animations aux frames de transformation animés. L’interface possède des méthodes pour mélanger plusieurs animations et modifier les paramètres de fusion dans le temps pour permettre des transitions lisses et d’autres effets.

## <a name="members"></a>Membres

L’interface **ID3DXAnimationController** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationController** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXAnimationController** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Anime le maillage et avance l’heure de l’animation globale d’une valeur spécifiée.<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Clone, ou copie, un contrôleur d’animation.<br/>                                                                                                  |
| [**GetAnimationSet**](id3dxanimationcontroller--getanimationset.md)                     | Obtient un jeu d’animations.<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | Obtient un jeu d’animations en fonction de son nom.<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Retourne un handle d’événement pour un événement de fusion de priorité en cours d’exécution.<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Retourne un handle d’événement pour l’événement en cours d’exécution sur la piste d’animation spécifiée.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Obtient une description d’un événement d’animation spécifié.<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Obtient le nombre maximal de sorties d’animation que le contrôleur d’animation peut prendre en charge.<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Obtient le nombre maximal de jeux d’animations que le contrôleur d’animation peut prendre en charge.<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Obtient le nombre maximal d’événements que le contrôleur d’animation peut prendre en charge.<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Obtient le nombre maximal de pistes dans le contrôleur d’animation.<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | Retourne le nombre de jeux d’animations actuellement enregistrés dans le contrôleur d’animation.<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | Obtient le poids de fusion de priorité actuel utilisé par le contrôleur d’animation.<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | Obtient l’heure globale de l’animation.<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | Obtient l’animation définie pour le suivi donné.<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | Obtient la description de la piste.<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Retourne un handle d’événement pour l’événement de fusion Priority suivant planifié pour se produire après un événement spécifié.<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Retourne un handle d’événement pour l’événement suivant planifié pour se produire après un événement spécifié sur une piste d’animation.<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | Définit les clés d’événement de fusion pour la piste d’animation spécifiée.<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | Définit une clé d’événement qui active ou désactive une piste d’animation.<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | Définit une clé d’événement qui modifie l’heure locale d’une piste d’animation.<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Définit une clé d’événement qui modifie le taux de lecture d’une piste d’animation.<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | Définit une clé d’événement qui modifie le poids d’une piste d’animation. Le poids est utilisé comme multiplicateur lors de la combinaison de plusieurs pistes.<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Ajoute une sortie d’animation au contrôleur d’animation et enregistre les pointeurs pour les transformations de mise à l’échelle, de rotation et de translation (SRT).<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | Ajoute une animation définie au contrôleur d’animation.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Réinitialise l’heure de l’animation globale à zéro. Tous les événements en attente conservent leurs planifications d’origine, mais dans le nouveau délai.<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | Définit le poids de fusion des priorités utilisé par le contrôleur d’animation.<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | Applique l’animation définie à la piste spécifiée.<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | Définit la description de la piste.<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | Active ou désactive une piste dans le contrôleur d’animation.<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | Définit le suivi sur l’heure d’animation locale spécifiée.<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | Définit le poids de fusion des priorités pour la piste d’animation spécifiée.<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | Définit la vitesse de la piste. La vitesse de la piste est similaire à un multiplicateur qui est utilisé pour accélérer ou ralentir la lecture de la piste.<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | Définit le poids de la piste. Le poids est utilisé pour déterminer comment fusionner plusieurs pistes.<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Supprime tous les événements de fusion de priorité planifiés du contrôleur d’animation.<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Supprime tous les événements d’une piste d’animation spécifiée.<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | Supprime un événement spécifié d’une piste d’animation, empêchant ainsi l’exécution de l’événement.<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | Supprime un jeu d’animations du contrôleur d’animation.<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | Vérifie si un handle d’événement spécifié est valide et que l’événement d’animation n’est pas encore terminé.<br/>                                              |



 

## <a name="remarks"></a>Notes

Créez un objet de contrôleur d’animation avec [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

Le type LPD3DXANIMATIONCONTROLLER est défini comme un pointeur vers l’interface **ID3DXAnimationController** .


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



Le type D3DXEVENTHANDLE est défini comme un handle d’événement pour les événements du contrôleur d’animation.


```
typedef DWORD D3DXEVENTHANDLE;
```



Le type LPD3DXEVENTHANDLE est défini en tant que pointeur vers un handle d’événement pour les événements du contrôleur d’animation.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
