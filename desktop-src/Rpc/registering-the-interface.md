---
title: Inscription de l’interface
description: L’inscription de l’interface qu’un programme serveur prend en charge permet aux appels de procédure distante provenant de programmes clients d’être distribués à la routine de serveur appropriée.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Appel de procédure distante RPC, tâches, inscription de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190730"
---
# <a name="registering-the-interface"></a>Inscription de l’interface

L’inscription de l’interface qu’un programme serveur prend en charge permet aux appels de procédure distante provenant de programmes clients d’être distribués à la routine de serveur appropriée. Les programmes serveur appellent [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) pour inscrire leurs interfaces. Le fragment de code suivant illustre son utilisation :


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



Le premier paramètre de la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) est une structure que le compilateur MIDL génère à partir du fichier IDL qui définit l’interface (ou les interfaces) du serveur. Les deuxième et troisième paramètres sont respectivement un UUID et un vecteur de point d’entrée. Ils ont la valeur **null** dans cet exemple. Dans de nombreux cas, votre programme serveur définira ces valeurs de paramètre sur la **valeur null**. Les programmes serveur utilisent le deuxième et le troisième paramètres lorsqu’ils fournissent plusieurs implémentations des mêmes procédures dans une interface. Pour plus d’informations, consultez [vecteurs de point d’entrée](registering-interfaces.md).

Les programmes serveur peuvent également utiliser [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) pour inscrire une interface. L’un des avantages de cette fonction est qu’elle offre à votre application la possibilité de définir une fonction de rappel de sécurité. L’utilisation des fonctions de rappel de sécurité est l’approche recommandée pour sécuriser une interface.

> [!Note]  
> MIDL produit deux structures très similaires, une pour le client et une pour le serveur. La structure transmise à la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) est la version serveur de la structure générée par MIDL.

 

 

 




