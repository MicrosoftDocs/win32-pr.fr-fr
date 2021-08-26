---
description: Vous pouvez surveiller les statistiques des objets lors de l’exécution d’une application. En procédant ainsi, vous pouvez ajuster les caractéristiques du pool d’objets pour obtenir l’équilibre entre les performances et les ressources que vous aimeriez avoir.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Analyse des statistiques des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e58946953ef1688dcb44223522cc58ccd1195f07ec0173a0b75413fe441195f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070459"
---
# <a name="monitoring-object-statistics"></a>Analyse des statistiques des objets

Vous pouvez surveiller les statistiques des objets lors de l’exécution d’une application. En procédant ainsi, vous pouvez ajuster les caractéristiques du pool d’objets pour obtenir l’équilibre entre les performances et les ressources que vous aimeriez avoir.

Vous pouvez surveiller l’état de tous les objets qui sont configurés pour prendre en charge les statistiques d’objets et les rapports d’événements. L’activation des statistiques d’objets a une légère baisse des performances.

**Pour activer les statistiques d’objets**

1.  Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .

3.  Pour activer les statistiques d’objet pour le composant, sous **contexte d’activation**, activez la case à cocher le **composant prend en charge les événements et les statistiques** .

**Pour surveiller l’état des objets**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, ouvrez le dossier de l’application qui comprend les composants que vous souhaitez analyser.

2.  Cliquez avec le bouton droit sur le dossier **composants** , pointez sur **affichage**, puis cliquez sur **affichage des États**. Le volet d’informations affiche désormais l’affichage de l’État pour tous les composants de l’application. Le tableau suivant décrit les six colonnes de la vue d’État.

    

    | Colonne                        | Description                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifie un composant spécifique.<br/>                                                                                                                                                                                |
    | **Objets**<br/>        | Affiche le nombre d’objets actuellement détenus par les références du client.<br/>                                                                                                                                       |
    | **Activé**<br/>      | Affiche le nombre d’objets actuellement activés. <br/>                                                                                                                                                      |
    | **Mis en pool**<br/>         | Affiche le nombre total d’objets créés par le pool, y compris les objets en cours d’utilisation et les objets qui sont désactivés.<br/>                                                                                      |
    | **Dans l’appel**<br/>        | Identifie des objets dans l’appel.<br/>                                                                                                                                                                                     |
    | **Durée de l’appel (MS)**<br/> | Affiche la durée moyenne de l’appel (en millisecondes) des appels de méthode effectués au cours des 20 dernières secondes (jusqu’à 20 appels). L’heure de l’appel est mesurée au niveau de l’objet et n’inclut pas le temps utilisé pour traverser le réseau.<br/> |

    

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration d’un composant à regrouper](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




