---
description: En règle générale, un fournisseur fournit des données pour le compte d’une application.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Communication avec votre application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb696c0c12ed8de542b07067fe16e13c9c098cb712393975e82d948bc3238979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061227"
---
# <a name="communicating-with-your-application"></a>Communication avec votre application

En règle générale, un fournisseur fournit des données pour le compte d’une application. Par exemple, un serveur peut créer une DLL de performance pour fournir ses données de compteur. La communication entre une application et son fournisseur diffère pour les applications en mode utilisateur et en mode noyau. Les fournisseurs s’exécutent en mode utilisateur. Pour cette raison, les applications en mode utilisateur, telles que les applications d’impression et d’affichage, peuvent utiliser n’importe quelle technique pour la communication entre processus, comme les canaux nommés, le mappage de fichiers ou RPC. Toutefois, les applications en mode noyau doivent fournir une interface IOCTL qui retourne les données de performances au fournisseur.

> [!WARNING]
> N’utilisez pas COM comme mécanisme IPC. Le système ne peut pas garantir l’état d’initialisation COM du thread appelant l’interface. Par conséquent, la DLL peut ne pas être en mesure d’initialiser correctement COM et de collecter les données.

 

 

 



