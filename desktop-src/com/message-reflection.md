---
title: Réflexion de message
description: Réflexion de message
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028531"
---
# <a name="message-reflection"></a>Réflexion de message

Il est fortement recommandé qu’un conteneur de contrôles ActiveX prenne en charge la réflexion de message. Cela entraînera une opération plus efficace pour les contrôles sous-classés. Si la réflexion de message est prise en charge, la propriété ambiante MessageReflect doit être prise en charge et avoir la valeur **true**. Si un conteneur n’implémente pas la réflexion de message, le CDK OLE crée deux fenêtres pour chaque contrôle sous-classé, afin de fournir la réflexion de message pour le compte du conteneur de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




