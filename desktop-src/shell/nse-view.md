---
description: La plupart des extensions d’espace de noms sont un sous-ensemble de l’espace de noms Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Affichage d’une vue Self-Contained d’une extension d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973375"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Affichage d’une vue Self-Contained d’une extension d’espace de noms

La plupart des extensions d’espace de noms sont un sous-ensemble de l’espace de noms Shell. Lorsque vous créez un point de jonction, comme décrit dans [spécification de l’emplacement d’une extension d’espace de noms, l'](nse-junction.md)Explorateur Windows permet aux utilisateurs de naviguer vers et à partir de votre extension d’espace de noms comme n’importe quel autre dossier. Toutefois, il est également possible d’utiliser l’Explorateur Windows pour afficher uniquement le contenu de votre extension d’espace de noms. Cette option d’affichage est parfois appelée vue avec *racine*. Bien qu’elles ne soient pas couramment utilisées, les vues avec racine peuvent être préférables à des vues normales pour certains types d’extensions.

Avec une vue avec racine, une nouvelle instance de l’Explorateur Windows est créée, qui affiche le contenu de l’extension sous la forme d’un espace de noms distinct. L’arborescence d’une vue racine affiche uniquement les dossiers qui font partie de l’extension. Les utilisateurs ne peuvent pas naviguer d’une vue enracinée vers d’autres parties de l’espace de noms Shell.

Les extensions sont implémentées de la même façon pour les vues enracinées qu’elles le sont pour les vues normales. La seule différence réside dans le mode d’affichage du contenu de l’extension par l’Explorateur Windows. Il est même possible d’avoir des vues normales et enracinées de la même extension.

Pour ouvrir une vue d’une extension, vous devez lancer une instance de Explorer.exe avec un indicateur/root. Il existe plusieurs façons de lancer une vue avec racine, en fonction de la nature de votre extension.

-   [Comment utiliser un point de jonction pour ouvrir une vue enracinée](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Comment utiliser un fichier de raccourci pour ouvrir une vue avec racine](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Comment afficher une vue enracinée d’un fichier](how-to-display-a-rooted-view-of-a-file.md)

 

 



