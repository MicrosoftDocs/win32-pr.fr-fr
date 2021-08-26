---
title: Contrôles de conteneur
description: Contrôles de conteneur
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896439"
---
# <a name="container-controls"></a>Contrôles de conteneur

comme décrit ci-dessus, les contrôles de conteneur sont des contrôles ActiveX qui contiennent visuellement d’autres contrôles. l’architecture des contrôles ActiveX spécifie l’interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour activer les contrôles conteneurs. Les conteneurs peuvent également prendre en charge les contrôles de conteneur sans prendre en charge **IsimpleFrameSite**, bien que le comportement ne puisse pas être garanti. C’est pour cette raison qu’il existe une catégorie de composant pour les contrôles SimpleFrameSite où les fonctionnalités complètes de cette interface sont requises.

pour prendre en charge les contrôles de conteneur sans implémenter [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un conteneur de contrôle ActiveX doit :

-   Activez tous les contrôles à tout moment.
-   Reparenter les contrôles contenus au hWnd du contrôle conteneur.
-   Restez le parent du contrôle conteneur.

 

 




