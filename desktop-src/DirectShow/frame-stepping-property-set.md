---
description: Jeu de propriétés du pas à pas de frame
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Jeu de propriétés du pas à pas de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999652"
---
# <a name="frame-stepping-property-set"></a>Jeu de propriétés du pas à pas de frame

les décodeurs qui implémentent une recherche avec une précision de frame sous Microsoft DirectShow doivent implémenter le \_ \_ jeu de propriétés FrameStep AM KSPROPSETID, qui est utilisé conjointement avec l’interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .



| Étiquette | Valeur |
|-------------------|----------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ FrameStep |



 



| ID de propriété                              | Description                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_FRAMESTEP, propriété, \_ \_ étape            | Indique au décodeur de commencer une opération d’étape et passe une [**structure \_ \_ FRAMESTEP de propriété am**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) qui spécifie le nombre d’étapes.            |
| AM, \_ propriété \_ FRAMESTEP \_ Annuler          | Indique au décodeur d’annuler l’opération d’étape en cours. Aucune donnée d’instance n’est associée à cette propriété.                                                                  |
| AM, \_ propriété \_ FRAMESTEP \_ CANSTEP         | Le décodeur retourne S \_ OK sur cette instruction pour indiquer qu’il peut effectuer l’exécution pas à pas, ou \_ false dans le cas contraire. Aucune donnée d’instance n’est passée lorsque cette propriété est définie.         |
| AM, \_ propriété \_ FRAMESTEP \_ CANSTEPMULTIPLE | Le décodeur retourne S \_ OK sur cette instruction pour indiquer qu’il peut exécuter pas à pas plusieurs frames à la fois, ou \_ false dans le cas contraire. Aucune donnée d’instance n’est passée lorsque cette propriété est définie. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 



