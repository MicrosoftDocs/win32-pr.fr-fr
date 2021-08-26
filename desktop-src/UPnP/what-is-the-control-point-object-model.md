---
title: Qu’est-ce que le modèle objet de point de contrôle ?
description: L’illustration suivante montre le modèle d’objet de point de contrôle de base.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06fa7e9cd8fa2bd2e038002414260bf2468f8d951c24da42bdd7a687af06bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007962"
---
# <a name="what-is-the-control-point-object-model"></a>Qu’est-ce que le modèle objet de point de contrôle ?

L’illustration suivante montre le modèle d’objet de point de contrôle de base.

![modèle d’objet de point de contrôle](images/upnp-object-model.png)

La recherche d’appareils avec l’interface de recherche d’appareils crée un regroupement de périphériques. Une collection Devices contient zéro ou plusieurs objets Device. Les applications peuvent utiliser les différentes méthodes de collecte des appareils pour accéder à des objets d’appareil individuels.

Les objets périphérique contiennent toujours une collection de services qui contient un ou plusieurs objets de service. Ces objets de service sont utilisés par les applications pour communiquer avec et contrôler les appareils.

 

 




