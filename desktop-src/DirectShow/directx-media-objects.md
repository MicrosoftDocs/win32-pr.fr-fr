---
description: Objets multimédia DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objets multimédia DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ef7dc17ab595748d9ccbfa16e33e7b4b8057d161c7f1e5d9f589e6768ec35f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821194"
---
# <a name="directx-media-objects"></a>Objets multimédia DirectX

> [!Note]  
> Les DMOs ont été remplacés par [Media Foundation transformations](/windows/desktop/medfound/media-foundation-transforms) (MFTS). les interfaces DMO sont toujours prises en charge. Toutefois, si vous écrivez un codec personnalisé ou un plug-in de traitement audio/vidéo, vous devez envisager de l’implémenter en tant que table MFT.

 

Les objets DMOs (DirectX Media Objects) sont des composants de diffusion en continu de données COM. à certains égards, les DMOs sont similaires aux filtres Microsoft DirectShow. à l’instar des filtres DirectShow, DMOs prend les données d’entrée et les utilise pour produire des données de sortie. Toutefois, les interfaces de programmation d’applications (API) pour DMOs sont bien plus simples que les API correspondantes pour DirectShow. Par conséquent, les DMOs sont plus faciles à créer, à tester et à utiliser. DMOs peut être utilisé dans de nombreux scénarios :

-   les Applications basées sur DirectShow peuvent utiliser DMOs via un filtre de DirectShow appelé filtre de [Wrapper de DMO](dmo-wrapper-filter.md) . La distinction entre les filtres et les DMOs est transparente pour l’application. l’application n’appelle pas directement les api DMO.
-   Les applications basées sur Microsoft DirectSound peuvent utiliser l’effet audio DMOs. là encore, l’application est protégée des api DMO de bas niveau par les api DirectSound de niveau supérieur.
-   Les applications peuvent utiliser DMOs directement.

ainsi, en écrivant un DMO, vous créez un composant qui peut être utilisé dans un large éventail d’applications. Cette documentation contient les sections suivantes :

-   [À propos de DMOs](about-dmos.md)
-   [Utilisation de DMOs](using-dmos.md)
-   [Écriture d’un DMO](writing-a-dmo.md)
-   [Paramètres de média](media-parameters.md)
-   [DMO Faire](dmo-reference.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
