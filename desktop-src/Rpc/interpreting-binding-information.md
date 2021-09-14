---
title: Interprétation des informations de liaison
description: Microsoft RPC permet à vos programmes client et serveur d’accéder aux informations contenues dans un handle de liaison et de les interpréter.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Appel de procédure distante RPC, tâches, interprétation de la liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194148"
---
# <a name="interpreting-binding-information"></a>Interprétation des informations de liaison

Microsoft RPC permet à vos programmes client et serveur d’accéder aux informations contenues dans un handle de liaison et de les interpréter. Cela ne signifie pas que vous pouvez ou devez essayer d’accéder directement au contenu d’un handle de liaison. Microsoft RPC fournit des fonctions qui définissent et récupèrent les informations dans des handles de liaison.

Pour obtenir les informations dans un handle de liaison, transmettez le handle à [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Elle retourne les informations de liaison sous la forme d’une chaîne. Pour chaque appel à **RpcBindingToStringBinding**, vous devez avoir un appel correspondant à la fonction [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

Vous pouvez appeler la fonction [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) pour analyser la chaîne que vous obtenez à partir de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Cette fonction alloue des chaînes pour contenir les informations qu’elle analyse. Si vous ne souhaitez pas qu’il analyse une partie particulière des informations de liaison, transmettez une valeur **null** comme valeur de ce paramètre. Veillez à appeler [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) pour chacune des chaînes qu’il alloue.

Le fragment de code suivant illustre comment une application peut appeler ces fonctions.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



L’exemple de code précédent appelle les fonctions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) et [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) pour obtenir et analyser les informations dans un handle de liaison valide. Notez que la valeur **null** a été transmise en tant que deuxième paramètre à **RpcStringBindingParse**. Cela provoque l’ignorance de l’analyse de l’UUID de l’objet par cette fonction. Étant donné qu’elle n’analyse pas l’UUID, **RpcStringBindingParse** n’alloue pas de chaîne pour celle-ci. Cette technique permet à votre application d’allouer uniquement de la mémoire pour les informations qui vous intéressent à l’analyse et à l’analyse.

 

 




