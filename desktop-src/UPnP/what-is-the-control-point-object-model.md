---
title: Qu’est-ce que le modèle objet de point de contrôle ?
description: L’illustration suivante montre le modèle d’objet de point de contrôle de base.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311362"
---
# <a name="what-is-the-control-point-object-model"></a>Qu’est-ce que le modèle objet de point de contrôle ?

L’illustration suivante montre le modèle d’objet de point de contrôle de base.

![modèle d’objet de point de contrôle](images/upnp-object-model.png)

La recherche d’appareils avec l’interface de recherche d’appareils crée un regroupement de périphériques. Une collection Devices contient zéro ou plusieurs objets Device. Les applications peuvent utiliser les différentes méthodes de collecte des appareils pour accéder à des objets d’appareil individuels.

Les objets périphérique contiennent toujours une collection de services qui contient un ou plusieurs objets de service. Ces objets de service sont utilisés par les applications pour communiquer avec et contrôler les appareils.

 

 




