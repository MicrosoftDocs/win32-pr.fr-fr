---
description: Contrôles de lecture dans TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Contrôles de lecture dans TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239680"
---
# <a name="playback-controls-in-topoedit"></a>Contrôles de lecture dans TopoEdit

Une fois la topologie résolue, elle est mise en file d’attente dans la session multimédia pour la lecture. TopoEdit fournit un contrôle de transport pour la modification de l’état de la topologie sur la session multimédia.

Le tableau suivant présente la commande menu/barre d’outils et la méthode Media Foundation équivalente pour chaque opération.



| Menu/commande de barre d’outils                                                                                                                                                                                                                          | Méthode Media Foundation                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Dans le menu **contrôles** , cliquez sur **lire**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **lecture** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de nouvelle ligne du bouton de lecture](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| Dans le menu **contrôles** , cliquez sur **arrêter**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **arrêter** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de saut de ligne du bouton arrêter](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| Dans le menu **contrôles** , cliquez sur **suspendre**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **Pause** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de saut de ligne du bouton pause](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Pour plus d’informations sur le contrôle de la lecture par programme à l’aide d’API Media Foundation, consultez Guide pratique [pour contrôler les États de présentation](how-to-control-presentation-states.md).

## <a name="seeking"></a>Cherche

Si la topologie est recherchée, vous pouvez effectuer une recherche à l’aide de la barre de recherche (illustrée dans l’image suivante) pour spécifier un emplacement dans la chronologie de la topologie pour commencer la lecture.

![capture d’écran de la barre de recherche](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Si la source du média est recherchée, la commande Stop rétablit également la topologie jusqu’au début du flux.

 

## <a name="changing-the-playback-rate"></a>Modification de la vitesse de lecture

Si la source du média sous-jacent pour la topologie prend en charge plusieurs vitesses de lecture, vous pouvez utiliser la barre de taux pour modifier la vitesse de lecture. Pour avancer rapidement une topologie sur la session multimédia, augmentez la vitesse en faisant glisser le curseur vers la droite, comme illustré dans l’image suivante.

![capture d’écran de la barre de taux](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> Dans cette version, TopoEdit prend uniquement en charge les taux positifs. La lecture inversée n’est pas prise en charge.

 

Pour plus d’informations sur la modification par programmation de la vitesse de lecture à l’aide d’API Media Foundation, consultez [à propos du contrôle de la fréquence](about-rate-control.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Menus TopoEdit](topoedit-menus.md)
</dt> <dt>

[Barre d’outils TopoEdit](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



