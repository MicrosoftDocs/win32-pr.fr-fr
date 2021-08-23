---
description: simulation d’Graph génération avec GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: simulation d’Graph génération avec GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4f5bee201e2bd5b771348596b46caa513944aa148c7ec17a9e2974a360e60c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583193"
---
# <a name="simulating-graph-building-with-graphedit"></a>simulation d’Graph génération avec GraphEdit

DirectShow fournit un utilitaire de débogage appelé GraphEdit, que vous pouvez utiliser pour créer et tester des graphiques de filtre.

GraphEdit est un outil visuel permettant de créer des graphiques de filtres. Avec GraphEdit, vous pouvez expérimenter avec un graphique de filtre avant d’écrire du code d’application. Vous pouvez également charger un graphique de filtre créé par votre application pour vérifier que votre application génère le graphique approprié. Si vous développez un filtre personnalisé, GraphEdit offre un moyen rapide de le tester : Chargez simplement un graphique avec votre filtre personnalisé et essayez d’exécuter le graphique. si vous débutez avec DirectShow, GraphEdit est un bon moyen de vous familiariser avec les graphiques de filtres et l’architecture DirectShow.

L’illustration suivante montre comment GraphEdit représente un graphique de filtre simple.

![graphique de filtre simple dans GraphEdit](images/gedit09.png)

Chaque filtre est représenté sous la forme d’un rectangle. Les petits carrés situés le long des bords des filtres représentent des broches. Les broches d’entrée se trouvent sur le côté gauche du filtre et les broches de sortie se trouvent sur le côté droit. Les flèches représentent les connexions entre les broches.

Avec GraphEdit, vous pouvez :

-   Créez et modifiez des graphiques de filtre à l’aide d’une interface de glisser-déplacer.
-   Simulez des appels de programmation pour générer un graphique.
-   Exécuter, suspendre, arrêter et Rechercher un graphique.
-   Consultez les filtres qui sont inscrits sur votre ordinateur et affichez les informations de Registre pour chaque filtre.
-   Affichez les pages de propriétés de filtre.
-   Affichez les types de médias des connexions de code confidentiel.

Cette section contient les rubriques suivantes :

-   [Utilisation de GraphEdit](using-graphedit.md)
-   [chargement d’un Graph à partir d’un processus externe](loading-a-graph-from-an-external-process.md)
-   [enregistrement d’un Graph de filtre dans un fichier baGraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Chargement d’un fichier baGraphEdit par programmation](loading-a-graphedit-file-programmatically.md)
-   [Format de fichier GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 



