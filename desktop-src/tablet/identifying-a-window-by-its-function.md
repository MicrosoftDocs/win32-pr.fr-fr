---
description: Description de l’identification d’une fenêtre par sa fonction pour le Tablet PC.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identification d’une fenêtre par sa fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7b7255fd22b44d3aa7de8f9ef11a35db95f822d8029f0a56428b1c04f8ecf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044371"
---
# <a name="identifying-a-window-by-its-function"></a>Identification d’une fenêtre par sa fonction

Identifiez chaque type de fenêtre en lui assignant une classe de fenêtre unique. Évitez d’avoir une classe de fenêtre unique utilisée pour un large éventail de fonctions.

Les aides à l’accessibilité doivent avoir cette identification pour pouvoir gérer différentes fenêtres au sein de la même application. Il peut y avoir des instructions distinctes pour gérer ces fenêtres, telles que l’annonce de zones spécifiques lorsque le contenu change.

Si vous ne pouvez pas utiliser des classes de fenêtres distinctes, vous pouvez exposer les différences par le biais <entity type="reg"/> de Microsoft Active Accessibility <entity type="reg"/> ou, si nécessaire, par un message de fenêtre privée que vous documentez sur votre site Web.

Pour plus d’informations sur l’exposition des classes de fenêtre à l’aide de Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) .

 

 
