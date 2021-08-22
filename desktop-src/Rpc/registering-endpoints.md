---
title: Inscription des points de terminaison
description: L’inscription du programme serveur dans le mappage des points de terminaison de l’ordinateur hôte du serveur permet aux programmes clients de déterminer le point de terminaison (généralement un port TCP/IP ou un canal nommé) vers lequel le programme serveur est à l’écoute.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Appel de procédure distante RPC, tâches, inscrire des points de terminaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926856"
---
# <a name="registering-endpoints"></a>Inscription des points de terminaison

L’inscription du programme serveur dans le mappage des points de terminaison de l’ordinateur hôte du serveur permet aux programmes clients de déterminer le point de terminaison (généralement un port TCP/IP ou un canal nommé) vers lequel le programme serveur est à l’écoute. Pour s’inscrire dans le mappage de point de terminaison du système hôte du serveur, un programme serveur appelle la fonction [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) comme indiqué dans le fragment de code suivant :


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



Le premier paramètre de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) est la structure qui représente l’interface. Vous pouvez le trouver dans le fichier d’en-tête que le compilateur MIDL a généré à partir de votre fichier MIDL pour cette application distribuée. Consultez [développement de l’interface](developing-the-interface.md). Ensuite, **RpcEpRegister** a besoin que votre application passe un ensemble de handles de liaison stockés dans un vecteur de liaison.

Outre l’inscription des noms d’interface, votre application serveur peut également inscrire des UUID d’objet dans le mappage de point de terminaison. Dans cet exemple, il n’y a aucun UUID d’objet à inscrire, donc le troisième paramètre de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) est défini sur **null**.

Le dernier paramètre est une chaîne de commentaire. Bien que la bibliothèque Runtime RPC n’utilise pas cette chaîne, il est recommandé de définir la chaîne, car elle améliore la facilité de gestion du système. Un administrateur système peut utiliser la chaîne pour détecter les ports utilisés par les applications, qui peuvent ensuite être utilisées pour déterminer les ports à gérer par les pare-feu.

 

 




