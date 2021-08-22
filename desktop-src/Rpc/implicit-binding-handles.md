---
title: Handles de liaison implicites
description: Les handles de liaison implicite permettent à votre application de sélectionner un serveur spécifique pour exécuter ses appels de procédure distante.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d49618ec505cc776c346a504fb19b65db539dadb90d030e45efbabcf08371db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929074"
---
# <a name="implicit-binding-handles"></a>Handles de liaison implicites

Les handles de liaison implicite permettent à votre application de sélectionner un serveur spécifique pour exécuter ses appels de procédure distante. Pour plus d’informations, consultez [liaison côté client](client-side-binding.md). Ils permettent également à votre programme client/serveur d’utiliser des liaisons authentifiées. Autrement dit, le client peut spécifier des informations d’authentification dans un handle de liaison implicite. La bibliothèque Runtime RPC utilise les informations d’authentification pour établir une session RPC authentifiée entre le client et le serveur. Pour plus d’informations, consultez [Sécurité](security.md).

> [!Note]  
> Les handles de liaison implicite ne sont pas thread-safe. Les applications multithread doivent donc éviter d’utiliser des handles de liaison implicites.

 

Lorsque votre application utilise des liaisons implicites, le client doit définir les informations de liaison afin qu’il puisse créer la liaison. Une fois que le client a créé une liaison implicite, il n’est pas obligé de passer des handles de liaison à des procédures distantes. La bibliothèque RPC gère le reste du mécanisme de la session de communication.

Le client stocke les informations de liaison pour un handle implicite dans une variable globale. Lorsque le compilateur MIDL génère le stub client et le fichier d’en-tête à partir de la spécification d’interface dans votre fichier MIDL, il génère également du code pour une variable de handle de liaison globale. Votre programme client initialise le descripteur, puis ne se réfère pas à celui-ci jusqu’à ce qu’il détruise la liaison.

Vous créez un handle implicite en spécifiant l' \[ attribut de [**\_ handle implicite**](/windows/desktop/Midl/implicit-handle) \] dans le CCP pour une interface comme suit :

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

Le type **handle \_ t** , qui est utilisé dans l’exemple précédent, est un type de données MIDL utilisé pour définir des handles de liaison.

Après la création du handle implicite, l’application doit l’utiliser comme paramètre des fonctions de la bibliothèque Runtime RPC. N’utilisez pas le handle implicite en tant que paramètre pour les appels de procédure distante. L’exemple de code suivant illustre l’utilisation de handles de liaison implicites.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

Dans l’exemple précédent, les fonctions de la bibliothèque Runtime RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) et [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) nécessitaient que le handle de liaison implicite soit passé dans leurs listes de paramètres. Toutefois, la procédure distante MyRemoteProcedure n’a pas été effectuée, car il ne s’agit pas d’une fonction de bibliothèque Runtime RPC.

 

 