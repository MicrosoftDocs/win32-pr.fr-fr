---
description: Détecteur de média (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Détecteur de média (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116058"
---
# <a name="media-detector-mediadet"></a>Détecteur de média (MediaDet)

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’objet détecteur de média (MediaDet) récupère les informations de format et les images fixes des sources de fichier. Le détecteur de média ne nécessite pas le fonctionnement du gestionnaire de graphique de filtre. Pour créer cet objet, appelez **CoCreateInstance**. L’identificateur de classe est CLSID \_ MediaDet.

Pour lire des fichiers Windows Media™, l’application doit fournir un certificat logiciel, également appelé clé. Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** du détecteur de média. Pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).

L’objet MediaDet expose les interfaces suivantes :

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



