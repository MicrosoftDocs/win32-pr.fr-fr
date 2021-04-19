---
title: Indicateurs de création de transformation CMM
description: CMMs utilise les indicateurs de création de transformation comme indicateurs pour la création d’une transformation de couleur. Il revient à la méthode CMM de déterminer la meilleure façon d’utiliser ces indicateurs.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "106522482"
---
# <a name="cmm-transform-creation-flags"></a>Indicateurs de création de transformation CMM

CMMs utilise les indicateurs de création de transformation comme indicateurs pour la création d’une transformation de couleur. Il revient à la méthode CMM de déterminer la meilleure façon d’utiliser ces indicateurs.

Toutes les fonctions qui utilisent ces indicateurs passent ou reçoivent des valeurs d’indicateur via un paramètre appelé *dwFlags*. Le **mot** de poids fort de *dwFlags* doit être défini sur une valeur du tableau suivant.



| Constante                    | Description                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVER la vérification de la \_ gamme \_     | Utilisez cette transformation pour la vérification de la gamme de couleurs.                                                                                                       |
| UTILISER \_ \_ Colorimétrie relative | Ne conservez pas le point blanc. Si la gamme de sortie ne prend pas en charge une couleur donnée, utilisez la couleur la plus proche prise en charge. Consultez rendu des intentions. |
| \_traduction rapide             | Rechercher uniquement la couleur. N’interpolez pas la couleur.                                                                                            |
| PRESERVEBLACK               | Insère le GMMP de génération noir approprié comme dernier GMMP dans la séquence de transformation                                                     |
| \_toujours WCS                 | Utilisez le chemin de code WCS même pour les transformations ICC.                                                                                               |
| \_transformation séquentielle       | Indicateur de création de transformation pour la création d’une transformation de couleur séquentielle (non optimisée).                                                           |



 

Le **mot** de poids faible peut avoir l’une des valeurs constantes suivantes.



| Constante     | Description                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| MODE de vérification \_  | La transformation sera utilisée pour afficher un aperçu de l’image. Qualité d’image faible.                                    |
| \_mode normal | La transformation sera utilisée pour l’affichage normal de l’image. Qualité d’image moyenne.                            |
| MEILLEUR \_ mode   | La transformation sera utilisée pour l’affichage de l’image de qualité supérieure possible sur l’appareil cible. |



 

En passant du \_ mode preuve au meilleur \_ mode, la qualité de la sortie s’améliore généralement et la vitesse de transformation diminue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Constantes ICM](wcs-constants.md)
</dt> </dl>

 

 




