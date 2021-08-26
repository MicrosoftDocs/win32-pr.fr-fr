---
title: Fonctions d’acquisition de clé
description: Par défaut, le fournisseur de services partagés fournit des clés de chiffrement aux programmes serveur qui les demandent. Chaque fournisseur de services partagés implémente son propre système de génération de clés. Le format des clés générées par le fournisseur de services partagés est spécifique au fournisseur de services partagés.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020231"
---
# <a name="key-acquisition-functions"></a>Fonctions d’acquisition de clé

Par défaut, le fournisseur de services partagés fournit des clés de chiffrement aux programmes serveur qui les demandent. Chaque fournisseur de services partagés implémente son propre système de génération de clés. Le format des clés générées par le fournisseur de services partagés est spécifique au fournisseur de services partagés.

RPC vous permet de remplacer la méthode par défaut de génération de clés de chiffrement. Votre application peut appeler la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) et lui passer un pointeur vers une fonction d’acquisition de clé. Vous pouvez écrire la fonction d’acquisition de clé afin qu’elle génère des clés à l’aide de n’importe quelle méthode de votre choix. Toutefois, la clé qu’elle transmet au programme serveur doit correspondre au format requis par le fournisseur de services partagés.

> [!Note]  
> La plupart des applications n’ont pas besoin d’utiliser les fonctions d’acquisition de clé et peuvent simplement fournir la **valeur null** à tous les paramètres où une fonction d’acquisition de clé est demandée.

 

 

 




