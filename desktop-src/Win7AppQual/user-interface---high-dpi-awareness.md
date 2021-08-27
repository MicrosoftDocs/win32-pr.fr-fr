---
description: Interface utilisateur - Prise en charge de la haute résolution
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interface utilisateur - Prise en charge de la haute résolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52c2bb42ad2c54fc1d23e44edf54e4bc88f8ab40a3f3a04f9dbc57b484b55173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994579"
---
# <a name="user-interface---high-dpi-awareness"></a>Interface utilisateur - Prise en charge de la haute résolution

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows XP \| Windows Vista \| Windows 7  

## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -moyenne  

## <a name="description"></a>Description

L’objectif est d’encourager les utilisateurs finaux à définir leurs affichages sur la résolution native et à utiliser DPI plutôt que la résolution d’écran pour modifier la taille du texte affiché et des images. Windows 7 peut détecter automatiquement et configurer une résolution par défaut pour les nouvelles installations sur les ordinateurs configurés par leurs oem à l’aide des paramètres ppp. Il existe des outils que vous pouvez utiliser pour concevoir des applications qui prennent en charge la résolution élevée afin de garantir les résultats les plus lisibles.

nous avons ajouté deux nouvelles fonctionnalités haute résolution à Windows 7 :

-   Paramètre PPP par utilisateur (précédemment par ordinateur)
-   Modifier le DPI sans redémarrer (la fermeture/la connexion est toujours requise)

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Les applications qui ne gèrent pas le cas de résolution élevée sont susceptibles d’exposer des artefacts visuels, notamment :

-   Découpage de l’interface utilisateur ou du texte par d’autres éléments d’interface utilisateur
-   Tailles de police incohérentes
-   Interfaces utilisateur hors écran
-   Flou du texte ou de l’interface utilisateur
-   Opérations de glisser-déplacer ou autres entrées rompues
-   Rendu partiel des applications DX plein écran

## <a name="solution"></a>Solution

Pour que vos applications prennent en charge DPI :

1.  Effectuez une série de tests fonctionnels de haut niveau, y compris l’installation et la désinstallation, aux paramètres suivants :

    | Paramètre                                              | Éléments à rechercher                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 @ 120 ppp (125% de mise à l’échelle)                    | Il s’agit d’une résolution efficace de ~ 800x600, donc recherchez l’interface utilisateur découpée des problèmes d’écran ou de disposition. Recherchez également les bitmaps pixelisée & icônes.                         |
    | 1600 x 1200 @144 (150% de mise à l’échelle)                    | Interface utilisateur floue. Vérifiez que toutes les opérations de la souris fonctionnent, en particulier faire glisser & opérations de déplacement. Vérifiez également que les modes plein écran fonctionnent correctement.                                     |
    | 1600 x 1200 144 ppp avec la virtualisation DPI désactivée | Souvent, les boutons et l’interface utilisateur ne sont pas mis à l’échelle en fonction du texte plus grand & il y a un extrait de texte significatif. Recherchez les problèmes de disposition en général & pixelisée bitmats & icônes. |

    

     

2.  Notez tous les problèmes détectés, notamment l’emplacement, la résolution d’écran et les paramètres ppp, ainsi que la façon dont l’application se comporte dans les autres configurations PPP/résolution pour l’exhaustivité
3.  Vérifier chaque problème par rapport aux problèmes courants de codage PPP
4.  Évaluer le coût de la prise en charge de la résolution complète de l’application
5.  Créer une liste des ressources haute résolution requises (par exemple, des boutons, des icônes)
6.  Traiter et corriger la liste des problèmes de résolution détectés à l’étape 1
7.  Intégrer les nouvelles ressources de l’étape 5
8.  Déclarer la prise en charge DPI de votre application

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

Réexécutez l’évaluation de la détection des PPP et vérifiez que les problèmes sont résolus.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Développement d’applications bureautiques haute résolution sur Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Contactez-nous pour obtenir des questions techniques :**<disup@microsoft.com>

 

 
