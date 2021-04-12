---
description: Décrit les statistiques utilise permutation relatives aux appels PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Structure D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211814"
---
# <a name="d3dpresentstats-structure"></a>D3DPRESENTSTATS, structure

Décrit les statistiques utilise permutation relatives aux appels [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**PresentCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’appels de présentation réussis effectués par un périphérique d’affichage qui est actuellement en cours de génération sur l’écran. Ce paramètre est véritablement l’ID actuel du dernier appel présent et n’est pas nécessairement le nombre total d’appels d’API présents.

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Le nombre de vblank à partir duquel le dernier a été affiché à l’écran, le nombre de vblank incrémente une fois tous les vblank intervalle.

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Le nombre de vblank lorsque le planificateur a échantillonné l’heure de la machine en appelant QueryPerformanceCounter.

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Heure de la dernière machine échantillonnée du planificateur, obtenue en appelant [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Quand une application 9Ex adopte le mode Flip (D3DSWAPEFFECT \_ FLIPEX), les applications peuvent détecter la suppression de frame en appelant GetPresentStatistics à tout moment. En effet, ils peuvent effectuer les opérations suivantes.

1.  Rendre sur la mémoire tampon d’arrière-plan
2.  Appel présent
3.  Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue
4.  Restituer le frame suivant à la mémoire tampon d’arrière-plan
5.  Appel présent
6.  Répétez les étapes 4 et 5 1 ou plus.
7.  Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue
8.  Comparez les valeurs de PresentRefreshCount à partir des deux structures D3DPRESENTSTATS stockées. L’application peut calculer le PresentRefreshCount correspondant d’un paramètre PresentCount particulier en fonction des hypothèses de l’incrémentation de PresentRefreshCount et de l’assignation PresentCount des images présentées. Si le dernier échantillonné PresentRefreshCount ne correspond pas au PresentCount (par exemple, si le PresentRefreshCount a été incrémenté mais que PresentCount n’en a pas, il y avait un abandon d’image).

Les applications peuvent déterminer si un frame a été supprimé en échantillonnant deux instances de PresentCount et GetPresentStats (en appelant l’API GetPresentStats à deux points quelconques dans le temps). Par exemple, une application multimédia qui présente le même taux de fréquence d’actualisation du moniteur (par exemple, le taux de rafraîchissement de l’analyse est 60 Hz, l’application présente une trame toutes les 1/60 secondes) veut présenter les images A, B, C, D, E, chacune correspondant aux ID de présentation (PresentCount) 1, 2, 3, 7, 8.

Le code d’application ressemble à la séquence suivante.

1.  Restituer le frame A à la mémoire tampon d’arrière-plan
2.  Appel présent, PresentCount = 1
3.  Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue
4.  Restituer les 4 frames suivants, B, C, D, E, respectivement
5.  Appel présent 4 fois, PresentCounts = 2, 3, 7, 8, respectivement
6.  Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue
7.  Comparez les valeurs de PresentRefreshCount à partir des deux structures D3DPRESENTSTATS stockées. Si la différence est 2, par exemple, 2 intervalles vblank se sont écoulés entre les deux appels de l’API GetPresentStats, alors la dernière trame présente doit être Frame C. Étant donné que l’application présente un intervalle très vblank (taux d’actualisation de l’analyse), le temps écoulé entre le moment où la trame A est présentée et le moment où la trame C est présentée doit être 2 vblanks.
8.  Comparez les valeurs de PresentCount à partir des deux structures D3DPRESENTSTATS stockées. Si le premier PresentCount est 1 (correspondant au frame A) et que le deuxième PresentCount est 3 (correspondant à l’image C), aucun cadre n’a été supprimé. Si le deuxième PresentCount est 3, ce qui correspond au frame D, l’application sait qu’une image a été supprimée.

Notez que GetPresentStatistics sera traité après son appel, quel que soit l’état du mode FLIPEX appels PresentEx.

**Windows Vista :** Les appels présents seront mis en file d’attente, puis traités avant que l’appel GetPresentStats ne soit traité.

Quand une application détecte que la présentation de certains cadres est en arrière-plan, elle peut ignorer ces frames et corriger la présentation pour la resynchronisation avec vblank. Pour ce faire, une application peut simplement ne pas restituer les images tardives et démarrer le rendu avec la prochaine image correcte dans la file d’attente. Toutefois, si une application a déjà démarré le rendu des frames tardifs, elle peut utiliser un nouveau paramètre present dans D3D9Ex appelé D3DPRESENT \_ FORCEIMMEDIATE. L’indicateur est passé dans les paramètres de l’appel de l’API présent et indique au runtime que le frame sera traité immédiatement dans l’intervalle de vblank suivant, qui n’est pas visible à l’écran. Voici l’exemple d’utilisation de l’application après la dernière étape de l’exemple précédent.

1.  Restituer le frame suivant à la mémoire tampon d’arrière-plan
2.  Découvrir à partir de PresentRefreshCount que le frame suivant est déjà en retard
3.  Définir l’intervalle présent sur D3DPRESENT \_ FORCEIMMEDIATE
4.  Appel présent sur le frame suivant

Les applications peuvent synchroniser les flux vidéo et audio de la même manière, car le comportement de GetPresentStatistics ne change pas dans ce scénario.

Le mode de basculement D3D9Ex fournit des informations sur les statistiques des frames aux applications Windows et aux applications 9Ex plein écran.

**Windows Vista :** Utilisez les API DWM pour récupérer les statistiques actuelles.

Lorsque Gestionnaire de fenêtrage est désactivé, les applications du mode fenêtre 9Ex utilisant le mode Flip recevront les informations statistiques de précision limitée.

* * Windows Vista : * *

Si une application n’est pas assez rapide pour suivre la fréquence d’actualisation du moniteur, peut-être en raison d’un matériel lent ou d’un manque de ressources système, il peut rencontrer un problème graphique. Un problème est appelé Visual contretemps. Si une analyse est configurée pour s’actualiser à 60 Hz et que l’application ne peut gérer que 30 fps, la moitié des trames aura des problèmes.

Les applications peuvent détecter un problème en effectuant le suivi de SynchRefreshCount. Par exemple, une application peut exécuter la séquence d’actions suivante.

1.  Rendu à la mémoire tampon d’arrière-plan.
2.  Appel présent.
3.  Appelez GetPresentStats et stockez la structure D3DPRESENTSTATS résultante.
4.  Restitue le frame suivant à la mémoire tampon d’arrière-plan.
5.  Appel présent.
6.  Appelez GetPresentStats et stockez la structure D3DPRESENTSTATS résultante.
7.  Comparez les valeurs de SyncRefreshCount à partir des deux structures D3DPRESENTSTATS stockées. Si la différence est supérieure à un, le frame a été ignoré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
