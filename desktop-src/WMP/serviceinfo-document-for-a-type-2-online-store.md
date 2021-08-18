---
title: Document ServiceInfo pour un magasin de type 2 en ligne
description: Document ServiceInfo pour un magasin de type 2 en ligne
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995429"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Document ServiceInfo pour un magasin de type 2 en ligne

Les fournisseurs de magasin en ligne de type 2 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne. Lecteur Windows Media 10 et Lecteur Windows Media 11 utilisent ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.

dans Lecteur Windows Media 10, le document ServiceInfo fournit les éléments suivants :

-   informations sur la configuration des volets de tâches qui Lecteur Windows Media s’affichent lorsque le magasin en ligne est actif. Un magasin en ligne peut avoir un, deux ou trois volets de tâches.
-   Informations utilisées pour configurer les boutons du volet de tâches, tels que le texte du bouton, la couleur du bouton et des info-bulles pour les boutons.
-   url pour les images que Lecteur Windows Media affiche pour identifier le magasin en ligne.
-   url des pages web, fournies par le magasin en ligne, qui Lecteur Windows Media hôtes dans son interface utilisateur.
-   informations sur la façon dont Lecteur Windows Media programme d’installation doit configurer le premier magasin en ligne que l’utilisateur voit.

dans Lecteur Windows Media 11, le document ServiceInfo fournit les éléments suivants :

-   Informations utilisées pour configurer le bouton de l’onglet magasins en ligne, tels que le texte du bouton et l’info-bulle pour le bouton.
-   url pour les images que Lecteur Windows Media affiche pour identifier le magasin en ligne.
-   url des pages web, fournies par le magasin en ligne, qui Lecteur Windows Media hôtes dans son interface utilisateur.

Lorsque vous commencez à développer votre magasin en ligne, vous devez fournir à Microsoft l’URL de votre document ServiceInfo. pendant la phase de développement, votre magasin en ligne s’affiche dans Lecteur Windows Media uniquement lorsqu’une clé de registre spéciale est définie.

une fois votre magasin en ligne publié, le scénario ususal est que Lecteur Windows Media récupère automatiquement votre document ServiceInfo à partir du Web. toutefois, dans certains cas, Lecteur Windows Media récupère le document ServiceInfo à partir de l’ordinateur de l’utilisateur. Pour plus d’informations, consultez [définition du magasin en ligne initial](setting-the-initial-online-store.md).

lorsque Lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL. la chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux de l’utilisateur et la version de Lecteur Windows Media.

Vous pouvez créer des documents ServiceInfo statiques ou dynamiques. Un document ServiceInfo statique a une extension de nom de fichier .xml. Un document ServiceInfo dynamique est une page ASP dont l’extension de nom de fichier est. asp ou. aspx.

Tous les éléments disponibles dans le document ServiceInfo ne peuvent pas être utilisés par chaque magasin en ligne, et certains éléments sont facultatifs pour tous les magasins en ligne. pour plus d’informations sur les types de magasins en ligne que vous pouvez créer et les fonctionnalités disponibles pour chaque type, consultez [Lecteur Windows Media des magasins en ligne](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Création du document ServiceInfo de manière dynamique**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




