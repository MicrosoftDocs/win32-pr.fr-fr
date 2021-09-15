---
description: Clonage et partage (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonage et partage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517513"
---
# <a name="cloning-and-sharing-direct3d-9"></a>Clonage et partage (Direct3D 9)

## <a name="cloning-parameters"></a>Clonage des paramètres

Le clonage a les restrictions suivantes.

-   Les clones héritent du pool de l’effet d’origine. Consultez la section paramètres de partage.
-   Les clones héritent des techniques, des passes, des paramètres et des annotations de l’effet d’origine (y compris toutes les annotations ajoutées à [**ID3DXEffect**](id3dxeffect.md)).
-   Les clones héritent des annotations ajoutées dynamiquement de l’effet d’origine.
-   Le clonage sur un nouvel appareil échoue si le pool de l’effet d’origine n’était pas **null** et que l’effet d’origine contenait un paramètre dépendant du périphérique partagé (tel qu’une texture ou un nuanceur).

## <a name="sharing-parameters"></a>Paramètres de partage

Un pool est une mémoire tampon qui partage des paramètres d’effet entre différents effets. Pour ajouter des paramètres à un pool, spécifiez une utilisation partagée lors de la création de l’effet.

Un pool a les restrictions suivantes.

-   Un paramètre est ajouté au pool la première fois qu’un effet contenant ce paramètre (partagé) est ajouté au pool.
-   Un pool obtient les valeurs initiales du premier paramètre partagé ; les paramètres partagés reçoivent ensuite leurs valeurs à partir du pool.
-   Un paramètre est supprimé du pool lorsque toutes les références d’effet au paramètre Shared sont libérées.
-   Tous les effets du pool qui contiennent le même paramètre dépendant du périphérique (partagé) doivent avoir le même appareil.

La **valeur null** peut être utilisée pour ne spécifier aucun pool, auquel cas aucun paramètre n’est partagé. Cela revient presque à spécifier un pool unique uniquement pour cet effet. La seule différence est que, lorsque l’effet est cloné, le clone ne partage pas ses paramètres partagés avec le d’origine.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



