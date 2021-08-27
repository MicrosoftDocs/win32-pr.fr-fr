---
title: Document ServiceInfo pour une boutique en ligne de type 1
description: Document ServiceInfo pour une boutique en ligne de type 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893cb3c849e062147d0f6bc80f3f9c1bd56a3457b60dfe30ce837820091e9710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995439"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Document ServiceInfo pour une boutique en ligne de type 1

Les magasins en ligne de type 1 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne. Lecteur Windows Media 11 utilise ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.

le document ServiceInfo pour un magasin de type 1 fournit les informations suivantes à Lecteur Windows Media :

-   Informations utilisées pour configurer le bouton **magasins en ligne** (également appelé onglet), tel que le texte du bouton, la couleur du bouton et l’info-bulle pour le bouton.
-   url pour les images que Lecteur Windows Media affiche pour identifier le magasin en ligne.
-   url des pages web, fournies par le magasin en ligne, qui Lecteur Windows Media hôtes dans son interface utilisateur.
-   URL où Lecteur Windows Media pouvez récupérer le plug-in du magasin en ligne afin que le plug-in puisse être installé sur l’ordinateur de l’utilisateur.

lorsque Lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL. la chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux et l’emplacement géographique de l’utilisateur, ainsi que sur la version de Lecteur Windows Media.

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

 

 




