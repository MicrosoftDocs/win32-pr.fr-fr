---
description: À propos de l’API de transcodage
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: À propos de l’API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449772"
---
# <a name="about-the-transcode-api"></a>À propos de l’API de transcodage

Le diagramme suivant montre comment l’API de transcodage est en relation avec le reste du pipeline d’encodage Media Foundation.

![diagramme qui affiche l’API de transcodage.](images/encoding08.png)

Le pipeline d’encodage contient les objets de traitement de données suivants :

-   Source du média
-   Décodeur
-   Redimensionnement vidéo ou rééchantillonneur audio
-   Encodeur
-   Récepteur multimédia

Le redimensionnement vidéo est nécessaire uniquement si la taille de la vidéo de sortie diffère de la source. Le rééchantillonneur audio est nécessaire uniquement si l’audio doit être rééchantillonné avant l’encodage. La paire décodeur/encodeur est requise pour le transcodage, mais pas pour remuxing.

La *topologie* d’encodage est l’ensemble d’objets de pipeline (source, décodeur, redimensionnement, rééchantillonneur, encodeur et récepteur multimédia), ainsi que les points de connexion entre eux. Pour plus d’informations sur les topologies, consultez [topologies](topologies.md).

Différents composants sont chargés de créer les différents objets de pipeline :

-   L’application utilise généralement le programme de [résolution source](source-resolver.md) pour créer la source du média.
-   La [session multimédia](media-session.md) charge et configure le décodeur, le redimensionnement vidéo et le rééchantillonneur audio. En interne, elle utilise le chargeur de topologie pour effectuer cette opération (voir [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   L’API de transcodage charge et configure l’encodeur et le récepteur multimédia.

Les applications avancées peuvent configurer l’encodeur et le récepteur multimédia directement, plutôt que d’utiliser l’API de transcodage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de transcodage](transcode-api.md)
</dt> <dt>

[Utilisation de l’API de transcodage](fast-transcode-objects.md)
</dt> </dl>

 

 



