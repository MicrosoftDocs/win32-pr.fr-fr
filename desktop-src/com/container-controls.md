---
title: Contrôles de conteneur
description: Contrôles de conteneur
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462479"
---
# <a name="container-controls"></a>Contrôles de conteneur

Comme décrit ci-dessus, les contrôles de conteneur sont des contrôles ActiveX qui contiennent visuellement d’autres contrôles. L’architecture des contrôles ActiveX spécifie l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour activer les contrôles de conteneur. Les conteneurs peuvent également prendre en charge les contrôles de conteneur sans prendre en charge **IsimpleFrameSite**, bien que le comportement ne puisse pas être garanti. C’est pour cette raison qu’il existe une catégorie de composant pour les contrôles SimpleFrameSite où les fonctionnalités complètes de cette interface sont requises.

Pour prendre en charge les contrôles de conteneur sans implémenter [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un conteneur de contrôles ActiveX doit :

-   Activez tous les contrôles à tout moment.
-   Reparenter les contrôles contenus au hWnd du contrôle conteneur.
-   Restez le parent du contrôle conteneur.

 

 




