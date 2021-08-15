---
title: Procédure de génération générale
description: Page de navigation pour le processus de création d’une application client/serveur à l’aide d’un appel de procédure distante (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8402a14ceac3b34114e7b40998038a4e09fb7ba1a915c173f2062f7fab9e63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929630"
---
# <a name="general-build-procedure"></a>Procédure de génération générale

Le processus de création d’une application client/serveur à l’aide de Microsoft RPC est le suivant :

-   Développez l’interface.
-   Développez le serveur qui implémente l’interface.
-   Développez le client qui utilise l’interface.

La figure suivante illustre ces étapes.

![processus de création d’une application client-serveur à l’aide de Microsoft RPC](images/appdev.png)

Il est possible et courant de développer simultanément les applications client et serveur. Étant donné que les programmes client et serveur sont tous deux dépendants de l’interface, l’interface entre eux doit être développée avant le développement du client et du serveur, comme indiqué dans le diagramme précédent.

Cette section décrit les étapes nécessaires à la création d’une application client/serveur avec RPC. Les informations sont présentées dans les rubriques suivantes :

-   [Développement de l’interface](developing-the-interface.md)
-   [Développement du serveur](developing-the-server.md)
-   [Développement du client](developing-the-client.md)

 

 




