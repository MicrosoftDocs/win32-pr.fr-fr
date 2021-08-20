---
description: Cette table contient la liste des ressources minimales prises en charge par Direct3D 10.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Limites des ressources (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93617f77306a85290f4846e0b767e971db5c627659aa8b4bbf8249e3e7a88f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100961"
---
# <a name="resource-limits-direct3d-10"></a>Limites des ressources (Direct3D 10)

Cette table contient la liste des ressources minimales prises en charge par Direct3D 10.



| Ressource                                                                                               | Limite                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Nombre d’éléments dans une mémoire tampon constante                                                                | 4096                                                 |
| Nombre de texels (indépendamment de la taille de la structure) dans une mémoire tampon                                              | 227 texels                                           |
| Dimension Texture1D U                                                                                  | 8 192                                                 |
| Dimension Texture1DArray                                                                               | Tranches de tableau 512                                     |
| Dimension U/V Texture2D                                                                                | 8 192                                                 |
| Dimension Texture2DArray                                                                               | Tranches de tableau 512                                     |
| Dimension U/V/W Texture3D                                                                              | 2 048                                                 |
| Dimension TextureCube                                                                                  | 8 192                                                 |
| Taille de la ressource (en Mo)                                                                                  | 128 MO ¹                                              |
| Filtrage anisotrope MaxAnisotropy                                                                    | 16                                                   |
| Dimension de ressource adressable en filtrant le matériel                                                   | 8192 par dimension                                   |
| Taille de ressource (en Mo) adressable par IA (données d’entrée ou de vertex) ou VS/GS/PS (échantillon de point)              | 128 MO ¹                                              |
| Nombre total d’affichages de ressources par contexte (chaque tableau compte comme 1) (tous les types d’affichages ont une limite partagée) | 220                                                  |
| Taille de la structure de la mémoire tampon (élément multiple)                                                                  | 2 048 octets                                           |
| Taille de sortie du flux                                                                                     | Identique au nombre de texels dans une mémoire tampon (voir ci-dessus) |
| Nombre de vertex de dessin ou DrawInstanced (y compris l’instanciation)                                              | 232                                                  |
| \[ \] Nombre de vertex instances de DrawIndexed () (y compris l’instanciation)                                             | 232                                                  |
| Données de sortie d’appel GS ( \* vertex Components)                                                     | 1 024                                                 |
| Nombre total d’objets d’échantillonneur par contexte                                                            | 4096                                                 |
| Nombre total d’objets Viewport/ciseaux par pipeline                                                  | 16                                                   |
| Nombre total de distances de clips/de Culling par vertex                                                         | 8                                                    |
| Nombre total d’objets de fusion par contexte                                                              | 4096                                                 |
| Nombre total d’objets de profondeur/gabarit par contexte                                                      | 4096                                                 |
| Nombre total d’objets d’état de rastériseur par contexte                                                   | 4096                                                 |
| Nombre maximal d’échantillons par pixel pendant l’échantillonnage multiple                                                    | 32                                                   |
| Nombre d’éléments de vertex de ressource de nuanceur (composants 4 32 bits)                                          | 16                                                   |
| Common-Shader Core (composants 4 32 bits)-nombre de registres Temp (r \# + indexable x \# \[ n \] )             | 4096                                                 |
| Common-Shader Core constant-emplacements de mémoire tampon                                                               | 14                                                   |
| Emplacements d’entrée-ressources de noyau de nuanceur commun                                                                | 128                                                  |
| Emplacements d’échantillonneur de noyau de nuanceur commun                                                                       | 16                                                   |
| Common-Shader Core-subroutine-imbrication Limit                                                            | 32                                                   |
| Limite d’imbrication de contrôle de workflow de noyau de nuanceur commun                                                          | 64                                                   |
| Nombre d’entrées de nuanceur de sommets-nombre d’registres (composants 4 32 bits)                                            | 16                                                   |
| Sortie du nuanceur de sommets-nombre d’registres (composants 4 32 bits)                                           | 16                                                   |
| Nombre d’entrées de nuanceur Geometry-nombre d’registres (composants 4 32 bits)                                          | 16                                                   |
| Sortie du nuanceur de géométrie-nombre d’registres (composants 4 32 bits)                                         | 32                                                   |
| Nombre d’entrées de nuanceur de pixels-nombre d’registres (composants 4 32 bits)                                             | 32                                                   |
| Sortie du nuanceur de pixels-nombre d’registres (composants 4 32 bits)                                            | 8                                                    |
| Nombre de registres de profondeur de sortie du nuanceur de pixels (32 bits \* 1-composant)                                          | 1                                                    |
| Emplacements de ressources d’entrée d’index assembleur d’entrée                                                             | 1                                                    |
| Emplacements de ressources d’entrée du vertex assembleur d’entrée                                                            | 16                                                   |



 

¹ les applications peuvent créer des ressources plus volumineuses que la taille maximale des ressources sur un matériel graphique. Toutefois, nous recommandons que les applications conservent des ressources inférieures à la taille maximale des ressources pour bénéficier de la compatibilité maximale entre les fournisseurs de graphiques. Le runtime garantit que les allocations au sein de la taille maximale des ressources sont prises en charge par tout le matériel Direct3D 10. Si une application tente d’allouer de la mémoire pour une ressource dans la taille de ressource maximale, le runtime ne parvient pas à effectuer la tentative uniquement si le système d’exploitation manque de ressources. Si une application tente d’allouer de la mémoire pour une ressource au-dessus de la taille de ressource maximale, le runtime peut faire échouer la tentative, car le système d’exploitation est trop étendu ou le matériel ne prend pas en charge les allocations au-delà de la taille de ressource maximale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



