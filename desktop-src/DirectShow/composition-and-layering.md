---
description: Composition et structuration en couches
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composition et structuration en couches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b173ed0727869d3630a2241d7237cf74fb5143a907a95fcc53901a7b85f285c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954228"
---
# <a name="composition-and-layering"></a>Composition et structuration en couches

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Dans une collection de suivis, la première piste a la priorité la plus faible (priorité 0) et chaque piste suivante a une priorité d’un niveau supérieur. À chaque niveau de priorité, les éléments sources de cette piste masquent les éléments sources dans les pistes situées en dessous, sauf si cette couche contient également une transition. Ainsi, vous pouvez imaginer plusieurs passages lors du rendu.

Tout d’abord, elle affiche la piste 0. Il n’y a rien « sous «Track 0 », donc les régions vides sont rendues sous la forme d’une image noire unie. Les transitions dans cette couche se produisent entre l’image noire et la piste 0, ou vice versa. DES présente le suivi 1 en plus de la piste 0, générant des transitions entre les deux pistes. Le résultat est le composite des deux pistes. Ensuite, il place la piste 2 sur ce composite. Les transitions à cette couche se produisent entre le composite et le rail 2. Le processus se poursuit jusqu’à ce que la dernière piste (priorité la plus élevée) soit déplacée.

Lorsque plusieurs pistes sont composites ensemble, elles se comportent comme une seule piste (appelée une piste virtuelle). L’objet composition encapsule ce comportement, ce qui rend possible des transitions complexes. Par exemple, un clip vidéo peut être réinitialisé jusqu’à un deuxième élément, tandis que le composite (les deux clips et la réinitialisation) apparaît en fondu sur un troisième élément.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec les Services d’édition DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



