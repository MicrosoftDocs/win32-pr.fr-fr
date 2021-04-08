---
title: Document ServiceInfo pour une boutique en ligne de type 1
description: Document ServiceInfo pour une boutique en ligne de type 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029357"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Document ServiceInfo pour une boutique en ligne de type 1

Les magasins en ligne de type 1 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne. Le lecteur Windows Media 11 utilise ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.

Le document ServiceInfo pour un magasin de type 1 fournit les informations suivantes au lecteur Windows Media :

-   Informations utilisées pour configurer le bouton **magasins en ligne** (également appelé onglet), tel que le texte du bouton, la couleur du bouton et l’info-bulle pour le bouton.
-   URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.
-   URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.
-   URL où le lecteur Windows Media peut récupérer le plug-in de la Banque en ligne afin que le plug-in puisse être installé sur l’ordinateur de l’utilisateur.

Lorsque le lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL. La chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux et l’emplacement géographique de l’utilisateur, ainsi que sur la version du lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Création du document ServiceInfo de manière dynamique**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




