---
title: Réflexion de message
description: Réflexion de message
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855471"
---
# <a name="message-reflection"></a>Réflexion de message

il est fortement recommandé qu’un conteneur de contrôle ActiveX prenne en charge la réflexion de message. Cela entraînera une opération plus efficace pour les contrôles sous-classés. Si la réflexion de message est prise en charge, la propriété ambiante MessageReflect doit être prise en charge et avoir la valeur **true**. Si un conteneur n’implémente pas la réflexion de message, le CDK OLE crée deux fenêtres pour chaque contrôle sous-classé, afin de fournir la réflexion de message pour le compte du conteneur de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




