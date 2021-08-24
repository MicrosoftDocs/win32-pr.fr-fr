---
description: Détecteur de média (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Détecteur de média (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684969"
---
# <a name="media-detector-mediadet"></a>Détecteur de média (MediaDet)

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’objet détecteur de média (MediaDet) récupère les informations de format et les images fixes des sources de fichier. le détecteur de média ne nécessite pas que le gestionnaire de Graph de filtre fonctionne. Pour créer cet objet, appelez **CoCreateInstance**. L’identificateur de classe est CLSID \_ MediaDet.

pour lire Windows fichiers de™ multimédia, l’application doit fournir un certificat logiciel, également appelé clé. Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** du détecteur de média. pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) Windows Media Format](unlocking-the-windows-media-format-sdk.md).

L’objet MediaDet expose les interfaces suivantes :

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



