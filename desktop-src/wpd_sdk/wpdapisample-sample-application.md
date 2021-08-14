---
description: Application WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Application WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef1741f2cad07e28bee514cf6109cdbbf7347966e1a8184a88a11936cbccdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963468"
---
# <a name="wpdapisample-application"></a>Application WpdApiSample

L’exemple d’application WpdApiSample est une application de bureau en ligne de commande qui vous permet d’énumérer des appareils connectés, d’explorer des appareils, de rechercher des propriétés et des attributs, d’envoyer et de récupérer des objets, et ainsi de suite. Au démarrage, l’application ouvre une fenêtre de commande qui répertorie les tâches que vous pouvez effectuer.

L’exemple d’application WpdApiSample comprend les fichiers suivants :



| **File**               | **Description**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp | Contient des fonctions qui énumèrent tous les objets sur un appareil.                                                                                                                                            |
| ContentProperties. cpp  | Contient des fonctions qui lisent et écrivent des propriétés d’objet et effectuent des requêtes de jeu de propriétés en bloc.                                                                                                         |
| ContentTransfer. cpp    | Contient des fonctions qui transfèrent du contenu vers ou à partir de l’appareil, lisent les exigences de type d’objet et créent un dossier sur l’appareil.                                                                         |
| DeviceCapabilities. cpp | Contient des fonctions permettant de répertorier les types d’objets fonctionnels sur l’appareil, de répertorier les types de contenu pris en charge par chaque type d’objet fonctionnel et d’afficher des profils d’objet de rendu.                             |
| DeviceEnumeration. cpp  | Répertorie les noms conviviaux, les fabricants et les descriptions de tous les appareils connectés.                                                                                                                       |
| DeviceEvents. cpp       | Contient des fonctions qui journalisent des événements de périphérique et leurs paramètres chaque fois que des événements sont déclenchés.                                                                                                                 |
| stdafx.cpp             | Comprend les fichiers standard.                                                                                                                                                                              |
| WpdApiSample. cpp       | Héberge la fonction de démarrage **\_ tmain** , qui appelle la fonction de **menu contextuel** locale, qui affiche une liste des périphériques et des tâches disponibles et appelle la fonction appropriée pour la sélection de menu de l’utilisateur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple](sample.md)
</dt> </dl>

 

 



