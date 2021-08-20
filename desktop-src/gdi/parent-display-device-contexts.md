---
description: Un contexte de périphérique parent permet à une application de réduire le temps nécessaire pour configurer la zone de découpage pour une fenêtre.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contextes de périphérique d’affichage parent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f7f1a00c62927953ee7122d451719e8f6209b46d593fa2b5e4ca36d270d539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886214"
---
# <a name="parent-display-device-contexts"></a>Contextes de périphérique d’affichage parent

Un *contexte de périphérique parent* permet à une application de réduire le temps nécessaire pour configurer la zone de découpage pour une fenêtre. Une application utilise généralement des contextes d’appareil parent pour accélérer le dessin des fenêtres de contrôle sans nécessiter un contexte de périphérique ou de classe privé. Par exemple, le système utilise des contextes de périphérique parent pour le bouton de commande et les contrôles d’édition. Les contextes de périphérique parent sont destinés à être utilisés uniquement avec les fenêtres enfants, jamais avec des fenêtres contextuelles ou de niveau supérieur.

Une application peut spécifier le \_ style cs PARENTDC pour définir la zone de découpage de la fenêtre enfant sur celle de la fenêtre parente afin que l’enfant puisse dessiner dans le parent. La spécification de CS \_ PARENTDC améliore les performances d’une application, car le système n’a pas besoin de recalculer la région visible pour chaque fenêtre enfant.

Les valeurs d’attribut définies par la fenêtre parente ne sont pas conservées pour la fenêtre enfant ; par exemple, la fenêtre parente ne peut pas définir le pinceau pour ses fenêtres enfants. La seule propriété conservée est la zone de découpage. La fenêtre doit découper sa propre sortie vers les limites de la fenêtre. Étant donné que la zone de découpage du contexte de périphérique parent est identique à la fenêtre parente, la fenêtre enfant peut potentiellement dessiner sur la totalité de la fenêtre parente, mais le contexte de périphérique parent ne doit pas être utilisé de cette façon.

Le système ignore le \_ style cs PARENTDC si la fenêtre parente utilise un contexte de périphérique de classe ou privé, si la fenêtre parente découpe ses fenêtres enfants, ou si la fenêtre enfant découpe ses fenêtres enfants ou leurs fenêtres sœurs.

 

 



