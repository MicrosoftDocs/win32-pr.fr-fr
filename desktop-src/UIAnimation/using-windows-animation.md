---
title: Tâches d’animation Windows
description: Les rubriques contenues dans cette section décrivent les tâches de base requises pour les applications qui utilisent le gestionnaire d’animations Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animation Windows Animation Windows, tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511032"
---
# <a name="windows-animation-tasks"></a>Tâches d’animation Windows

Les rubriques contenues dans cette section décrivent les tâches de base requises pour les applications qui utilisent le gestionnaire d’animations Windows.

Ces tâches, dans l’ordre, sont les suivantes :

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                | Description                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Créer les objets d’animation principaux](adding-animation-to-an-application.md)<br/>               | Pour utiliser l’animation Windows dans votre application, la première étape consiste à créer un petit ensemble d’objets d’animation principaux.<br/>                                                                                                                                                                           |
| [Créer des variables d’animation](create-animation-variables.md)<br/>                              | Une application doit créer une variable d’animation pour chaque caractéristique visuelle qui doit être animée à l’aide de l’animation Windows.<br/>                                                                                                                                                            |
| [Mettre à jour le gestionnaire d’animations et dessiner des frames](introducing-windows-animation-manager.md)<br/> | Chaque fois qu’une application planifie un Storyboard, l’application doit fournir l’heure actuelle au gestionnaire d’animations. L’heure actuelle est également requise pour indiquer au gestionnaire d’animations de mettre à jour son état et de définir toutes les variables d’animation sur les valeurs interpolées appropriées.<br/> |
| [Lire les valeurs de la variable d’animation](updating---application-driven-animation.md)<br/>         | Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.<br/>                                                                                                                                  |
| [Créer une table de montage séquentiel et ajouter des transitions](updating---timer-driven-animation.md)<br/>          | Pour créer une animation, une application doit construire une table de montage séquentiel.<br/>                                                                                                                                                                                                                        |
| [Planifier une table de montage séquentiel](scheduling-a-storyboard.md)<br/>                                      | Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des animations Windows](scenic-animation-api-overview.md)
</dt> <dt>

[Informations de référence sur les animations Windows](windows-animation-reference.md)
</dt> <dt>

[Exemples d’animation Windows](windows-animation-samples.md)
</dt> </dl>

 

 





