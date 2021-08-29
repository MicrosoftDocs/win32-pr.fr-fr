---
title: Type de bouton
description: Type de bouton
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Lecteur Windows Media Apparences mobiles, types de bouton
- apparences, types de bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eeece7250242af0eb78d1938ad827b238f2de2337b6a8acc0eeeefec5f52acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123699"
---
# <a name="button-type"></a>Type de bouton

Les boutons se présentent sous deux types généraux : emplacement et région. Chaque type général a trois types spécifiques, en effectuant six types de boutons.

> [!Note]  
> les types de boutons sont déconseillés dans les habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure.

 

Types de boutons d’emplacement

Les boutons d’emplacement utilisent des coordonnées pour définir leurs emplacements par rapport à l’arrière-plan. Le tableau suivant indique les valeurs qui sont valides pour les types de bouton d’emplacement. Vous n’avez pas besoin de définir des valeurs pour les types que vous n’utiliserez pas dans votre apparence.



| Valeur  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Envoi de données (push)   | Définit un bouton qui déclenche un événement une seule fois. Le bouton doit être envoyé à chaque fois pour déclencher d’autres événements. Par exemple, un bouton se déplace vers l’élément suivant dans la sélection. L’emplacement du bouton est défini par ses coordonnées.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bascule | Définit un bouton qui déclenche un événement qui modifie un État. L’état reste jusqu’à ce que le bouton fasse l’objet d’un push. Par exemple, un bouton qui mélange la playlist. Une fois que la sélection est dans un état aléatoire, elle reste aléatoire jusqu’à ce que le bouton soit de nouveau envoyé. L’emplacement du bouton est défini par ses coordonnées.                                                                                                                                                                                                                                                                                                                                                           |
| 2Push  | Définit un bouton qui déclenche un événement, puis passe à un État qui est prêt à déclencher un événement différent. Les deux États sont activés chaque fois que le bouton est poussé. Par exemple, un bouton qui utilise la fonction **PlayPause** pour basculer entre la diffusion et la suspension de l’élément multimédia actuel. Lorsque le bouton est poussé la première fois, l’état de lecture principal est déclenché et une image secondaire est affichée pour indiquer qu’un événement de **Pause** peut être déclenché. Lorsque le bouton est envoyé à nouveau, l’État pause est déclenché et l’image d’origine est affichée pour indiquer qu’un événement de **lecture** peut être déclenché. L’emplacement du bouton est défini par ses coordonnées. |



 

Types de boutons de région

Les boutons de région utilisent des zones de couleur dans l’image de la région pour définir où les robinets seront traités pour un bouton particulier. Le tableau suivant indique les valeurs qui sont valides pour les types de bouton de région. Vous n’avez pas besoin de définir des valeurs pour les types que vous n’utiliserez pas dans votre apparence.



| Valeur     | Description                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| PushHit   | Semblable à la valeur du bouton de commande, à la différence près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région.   |
| ToggleHit | Semblable à la valeur du bouton bascule, à la différence près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région. |
| 2PushHit  | Semblable à la valeur du bouton 2Push, à ceci près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région.  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




