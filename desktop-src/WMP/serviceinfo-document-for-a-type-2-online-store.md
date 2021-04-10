---
title: Document ServiceInfo pour un magasin de type 2 en ligne
description: Document ServiceInfo pour un magasin de type 2 en ligne
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029355"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Document ServiceInfo pour un magasin de type 2 en ligne

Les fournisseurs de magasin en ligne de type 2 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne. Le lecteur Windows Media 10 et le lecteur Windows Media 11 utilisent ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.

Dans le lecteur Windows Media 10, le document ServiceInfo fournit les informations suivantes :

-   Informations sur la configuration des volets de tâches que le lecteur Windows Media affiche lorsque le magasin en ligne est actif. Un magasin en ligne peut avoir un, deux ou trois volets de tâches.
-   Informations utilisées pour configurer les boutons du volet de tâches, tels que le texte du bouton, la couleur du bouton et des info-bulles pour les boutons.
-   URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.
-   URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.
-   Informations sur la façon dont le programme d’installation du lecteur Windows Media doit configurer la première boutique en ligne visible par l’utilisateur.

Dans le lecteur Windows Media 11, le document ServiceInfo fournit les informations suivantes :

-   Informations utilisées pour configurer le bouton de l’onglet magasins en ligne, tels que le texte du bouton et l’info-bulle pour le bouton.
-   URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.
-   URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.

Lorsque vous commencez à développer votre magasin en ligne, vous devez fournir à Microsoft l’URL de votre document ServiceInfo. Pendant la phase de développement, votre magasin en ligne s’affiche dans le lecteur Windows Media uniquement lorsqu’une clé de Registre spéciale est définie.

Une fois votre magasin en ligne publié, le scénario ususal est que le lecteur Windows Media récupère automatiquement votre document ServiceInfo à partir du Web. Dans certains cas, toutefois, le lecteur Windows Media récupère le document ServiceInfo sur l’ordinateur de l’utilisateur. Pour plus d’informations, consultez [définition du magasin en ligne initial](setting-the-initial-online-store.md).

Lorsque le lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL. La chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux de l’utilisateur et la version du lecteur Windows Media.

Vous pouvez créer des documents ServiceInfo statiques ou dynamiques. Un document ServiceInfo statique a une extension de nom de fichier. Xml. Un document ServiceInfo dynamique est une page ASP dont l’extension de nom de fichier est. asp ou. aspx.

Tous les éléments disponibles dans le document ServiceInfo ne peuvent pas être utilisés par chaque magasin en ligne, et certains éléments sont facultatifs pour tous les magasins en ligne. Pour plus d’informations sur les types de magasins en ligne que vous pouvez créer et les fonctionnalités disponibles pour chaque type, consultez [Windows Media Player Online stores](windows-media-player-online-stores.md).

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

 

 




