---
title: Propriétés du contrôle de l’agent
description: Propriétés du contrôle de l’agent
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028769"
---
# <a name="agent-control-properties"></a>Propriétés du contrôle de l’agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les propriétés suivantes sont directement accessibles à partir du contrôle de l’agent :

-   [**Connecté**](connected-property.md)
-   [**Nom**](name-property-a.md)
-   [**RaiseRequestErrors**](raiserequesterrors-property.md)

En outre, certains environnements de programmation peuvent assigner des propriétés supplémentaires au moment du design ou au moment de l’exécution. Par exemple, Visual Basic ajoute les propriétés gauche, index, tag et Top qui définissent l’emplacement du contrôle sur un formulaire, même si le contrôle n’apparaît pas sur la page du formulaire au moment de l’exécution.

La propriété Suspended est toujours prise en charge pour la compatibilité descendante, mais retourne toujours **false** , car le serveur ne prend plus en charge l’État Suspended.

 

 




