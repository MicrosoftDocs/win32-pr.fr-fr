---
description: La combinaison de couleurs permet à une application de créer de nouvelles couleurs en combinant le stylet ou la couleur du pinceau avec les couleurs de l’image existante.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Mélange de couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105728"
---
# <a name="color-mixing"></a>Mélange de couleurs

La combinaison de couleurs permet à une application de créer de nouvelles couleurs en combinant le stylet ou la couleur du pinceau avec les couleurs de l’image existante. L’application peut choisir de dessiner le stylet ou la couleur du pinceau en l’État (dessinant efficacement sur une image existante) ou de mélanger la couleur aux couleurs déjà présentes.

Le mode de combinaison de premier plan, parfois appelé opération Raster binaire, détermine la façon dont ces couleurs sont mélangées. Une application peut fusionner des couleurs, en préservant tous les composants des deux couleurs ; masquer les couleurs, supprimer ou modérer les composants qui ne sont pas courants ; ou masquez exclusivement les couleurs, en supprimant ou en modérant les composants qui sont courants. Il existe plusieurs variantes de ces opérations de mixage de base.

Le mélange des couleurs est soumis à une approximation des couleurs. Si le résultat du mixage des couleurs est une couleur que l’appareil ne peut pas générer, le système se rapproche du résultat, en utilisant une couleur qu’il peut générer. Si une application combine des couleurs digénérées, les couleurs individuelles utilisées pour créer la couleur décomposée sont mélangées et les résultats sont soumis à une approximation des couleurs.

Une application définit le mode de combinaison de premier plan à l’aide de la fonction [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) et récupère le mode actuel à l’aide de la fonction [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .

Bien qu’il y ait un mode mixte en arrière-plan, ce mode ne contrôle pas la combinaison de couleurs. Au lieu de cela, il spécifie si une couleur d’arrière-plan est utilisée lors du dessin de lignes stylisées, de pinceaux hachurés et de texte.

 

 



