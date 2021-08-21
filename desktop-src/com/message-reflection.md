---
title: Réflexion de message
description: Réflexion de message
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048047"
---
# <a name="message-reflection"></a>Réflexion de message

il est fortement recommandé qu’un conteneur de contrôle ActiveX prenne en charge la réflexion de message. Cela entraînera une opération plus efficace pour les contrôles sous-classés. Si la réflexion de message est prise en charge, la propriété ambiante MessageReflect doit être prise en charge et avoir la valeur **true**. Si un conteneur n’implémente pas la réflexion de message, le CDK OLE crée deux fenêtres pour chaque contrôle sous-classé, afin de fournir la réflexion de message pour le compte du conteneur de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




