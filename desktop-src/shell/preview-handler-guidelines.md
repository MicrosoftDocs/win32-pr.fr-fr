---
description: Lorsque vous fournissez un aperçu, les instructions suivantes doivent être suivies.
title: Instructions du gestionnaire d’aperçus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719627"
---
# <a name="preview-handler-guidelines"></a>Instructions du gestionnaire d’aperçus

Lorsque vous fournissez un aperçu, les instructions suivantes doivent être suivies.

-   Un aperçu doit contenir une interface utilisateur minimale ; il s’agit simplement d’une version préliminaire. Elle doit afficher uniquement le contenu du fichier. Elle ne doit pas afficher de boîtes de dialogue, d’écrans de démarrage, de barres d’outils ou de volets de tâches. Le volet de lecture est couramment utilisé conjointement avec la recherche pour identifier rapidement un fichier. Tout ce qui encombre le volet de lecture ou qui dépasse le contenu du fichier ou provoque l’évitement des retards dans l’affichage de l’aperçu.
-   La version préliminaire doit permettre à l’utilisateur de naviguer dans le document. L’utilisateur doit également pouvoir sélectionner et copier du texte.
-   L’aperçu ne doit pas consommer beaucoup de mémoire, doit consommer un minimum de ressources et doit avoir un temps de démarrage rapide.
-   L’exécution de tous les scripts et macros dans le fichier en cours d’aperçu doit être bloquée à des fins de sécurité et de confidentialité.
-   La version préliminaire doit prendre en charge les accélérateurs de clavier pour la navigation et la sélection, comme pris en charge par l’application. Il doit également afficher un menu contextuel lorsque l’utilisateur clique avec le bouton droit.
-   Lorsqu’un fichier est affiché en tant qu’aperçu, l’aperçu ne doit pas verrouiller le fichier lui-même. Un fichier peut être visualisé et ouvert dans son application associée en même temps.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires d’aperçus et hôte de l’interpréteur de commandes](preview-handlers.md)
</dt> <dt>

[Génération de gestionnaires d’aperçus](building-preview-handlers.md)
</dt> </dl>

 

 



