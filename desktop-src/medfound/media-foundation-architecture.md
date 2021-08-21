---
description: Cette section décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez Media Foundation Guide de programmation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Architecture Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974213"
---
# <a name="media-foundation-architecture"></a>Architecture Media Foundation

Cette section décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez [Media Foundation Guide de programmation](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                         | Description                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble de l’architecture Media Foundation](overview-of-the-media-foundation-architecture.md)<br/> | Offre une vue d’ensemble de l’architecture Media Foundation.<br/>                                                                                                                                                                                                               |
| [Primitives de Media Foundation](media-foundation-primitives.md)<br/>                                     | Décrit certaines interfaces de base utilisées dans Media Foundation.<br/> Presque toutes les applications de Media Foundation utilisent ces interfaces.<br/>                                                                                                                       |
| [API de plateforme Media Foundation](media-foundation-platform-apis.md)<br/>                               | Décrit les fonctions de Media Foundation principales, telles que les rappels asynchrones et les files d’attente de travail.<br/> Certaines applications peuvent utiliser des interfaces de niveau plateforme. En outre, les plug-ins personnalisés, tels que les sources multimédias et MFTs, utilisent ces interfaces.<br/>                                       |
| [Pipeline Media Foundation](media-foundation-pipeline.md)<br/>                                         | La couche de pipeline Media Foundation se compose de sources multimédias, de MFTs et de récepteurs multimédias. La plupart des applications n’appellent pas directement des méthodes sur la couche de pipeline. Au lieu de cela, les applications utilisent l’une des couches supérieures, telles que la session multimédia ou le lecteur source et le writer du récepteur.<br/> |
| [Session multimédia](media-session.md)<br/>                                                                 | La session multimédia gère le workflow de données dans le pipeline Media Foundation.<br/>                                                                                                                                                                                                           |
| [Lecteur source](source-reader.md)<br/>                                                                 | Le lecteur source permet à une application d’obtenir des données à partir d’une source multimédia, sans que les applicating aient besoin d’appeler directement les API de source de média. Le lecteur source peut également effectuer le décodage des flux compressés.<br/>                                                            |
| [Chemin du média protégé](protected-media-path.md)<br/>                                                   | Le chemin d’accès au média protégé (PMP) fournit un environnement protégé pour la diffusion de contenu vidéo Premium. Il n’est pas nécessaire d’utiliser l’PMP lors de l’écriture d’une application Media Foundation. <br/>                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation : notions essentielles](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation et COM](media-foundation-and-com.md)
</dt> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




