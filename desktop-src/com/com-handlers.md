---
title: Gestionnaires COM
description: L’objectif des gestionnaires COM est de fournir certains \ 0034 ; intelligent \ 0034 ; code dans l’espace d’adressage du client qui peut optimiser les appels entre un client et un serveur. Les gestionnaires peuvent remplacer certaines interfaces tout en déléguant les autres directement au serveur (via le proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517184"
---
# <a name="com-handlers"></a>Gestionnaires COM

L’objectif des gestionnaires COM est de fournir un code « intelligent » dans l’espace d’adressage du client qui peut optimiser les appels entre un client et un serveur. Les gestionnaires peuvent remplacer certaines interfaces tout en déléguant les autres directement au serveur (via le proxy).

Il existe deux types de gestionnaires COM :

-   [Le gestionnaire OLE](the-ole-handler.md) est une dll lourde qui fournit des services importants pour la liaison et l’incorporation. Il est généralement créé avant que le serveur ne soit lancé et initialisé afin que le serveur soit activé lorsque l’objet incorporé passe à l’État en cours d’exécution.
-   [Le gestionnaire léger côté client](the-lightweight-client-side-handler.md) peut être créé à n’importe quel effet, peut être très petit et ne peut pas être créé avant le serveur.

 

 




