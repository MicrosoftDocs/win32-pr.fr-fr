---
title: Chaînes et messages de commande MCI
description: Chaînes et messages de commande MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Chaînes de commande MCI, à propos de
- Messages de commande MCI, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416846"
---
# <a name="mci-command-strings-and-messages"></a>Chaînes et messages de commande MCI

MCI prend en charge les [chaînes de commande](command-strings.md) et [les messages de commande](command-messages.md). Vous pouvez utiliser des chaînes ou des messages, ou les deux, dans votre application MCI.

-   L' *interface de message de commande* se compose de constantes et de structures. Utilisez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour envoyer des messages à un appareil MCI.
-   L' *interface de chaîne de commande* fournit une version textuelle des messages de commande. Utilisez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) pour envoyer des chaînes à un appareil MCI. Les chaînes de commande dupliquent les fonctionnalités des messages de commande. Le système d’exploitation convertit les chaînes de commande en messages de commande avant de les envoyer au pilote MCI en vue de leur traitement.

Les messages de commande qui récupèrent des informations le font sous la forme de structures, qui sont faciles à interpréter dans une application C. Ces structures peuvent contenir des informations sur de nombreux aspects différents d’un appareil. Les chaînes de commande qui récupèrent des informations le font sous la forme de chaînes et peuvent uniquement récupérer une chaîne à la fois. Votre application doit analyser ou tester chaque chaîne pour l’interpréter. Vous constaterez peut-être que les messages de commande sont plus faciles à utiliser que les chaînes de commande dans certains cas, mais les chaînes de commande sont faciles à mémoriser et à implémenter. Certaines applications MCI utilisent des chaînes de commande lorsque la valeur de retour n’est pas utilisée (autre que pour vérifier la réussite) et les messages de commande lors de la récupération d’informations à partir de l’appareil.

Lorsque les commandes sont présentées, cette vue d’ensemble utilise la forme de chaîne de la commande suivie du formulaire de message entre parenthèses.

 

 