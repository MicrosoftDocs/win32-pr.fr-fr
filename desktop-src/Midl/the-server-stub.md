---
title: Stub serveur
description: Le stub serveur fournit des points d’entrée de substitution sur le serveur pour chacune des opérations définies dans le fichier IDL d’entrée.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL du compilateur MIDL, MIDL et RPC MIDL, interfaces, stub serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfc940ebbd90e4e028ce96dc3b5c47eb15179d41cfbd064cd235e87192822f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559899"
---
# <a name="the-server-stub"></a>Stub serveur

Le stub serveur fournit des points d’entrée de substitution sur le serveur pour chacune des opérations définies dans le fichier IDL d’entrée.

Quand une routine de stub serveur est appelée par la bibliothèque Runtime RPC, elle exécute les fonctions suivantes :

-   Démarshale les arguments d’entrée (décompresse les arguments à partir de leurs formats transmis).
-   Appelle l’implémentation réelle de la procédure sur le serveur.
-   Marshale les arguments de sortie (empaquette les arguments dans les formulaires transmis).

Le compilateur MIDL bascule [**/Server**](-server.md), [**/sstub**](-sstub.md)et [**/out**](-out.md) sur le fichier stub du serveur.

 

 




