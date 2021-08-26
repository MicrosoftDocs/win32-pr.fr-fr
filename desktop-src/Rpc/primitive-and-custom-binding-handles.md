---
title: Handles de liaison primitifs et personnalisés
description: Tous les handles déclarés avec le handle \_ t ou les \_ types de handle de liaison RPC \_ sont des handles de liaison primitifs.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019149"
---
# <a name="primitive-and-custom-binding-handles"></a>Handles de liaison primitifs et personnalisés

Tous les handles déclarés avec le [handle \_ t](/windows/desktop/Midl/handle-t) ou les types de [**\_ \_ handle de liaison RPC**](rpc-binding-handle.md) sont des handles de liaison primitifs. Vous pouvez étendre les types de [**\_ \_ handle**](rpc-binding-handle.md) de handle [ \_ t](/windows/desktop/Midl/handle-t) ou RPC pour inclure davantage ou des informations différentes que le type de handle primitif contient. Dans ce cas, vous créez un handle de liaison personnalisé.

Pour créer un handle de liaison personnalisé pour votre application distribuée, vous devez créer votre propre type de données et spécifier l' \[ [](/windows/desktop/Midl/handle) \] attribut handle sur une définition de type dans votre fichier IDL. Enfin, les fichiers stub mappent des handles de liaison personnalisés à des handles primitifs.

Si vous créez votre propre type de handle de liaison, vous devez également fournir des routines de liaison et de séparation que le stub client utilise pour mapper un handle personnalisé à un handle primitif. Le stub appelle vos routines de liaison et de séparation au début et à la fin de chaque appel de procédure distante. Les routines de liaison et de liaison doivent être conformes aux prototypes de fonction suivants.



| Prototype de fonction                     | Description       |
|----------------------------------------|-------------------|
| handle \_ t type \_ Bind (*type*)           | Routine de liaison   |
| void \_ , type Unbind (*type*, *handle \_ t*) | Routine de dissociation |



 

L’exemple suivant montre comment un handle de liaison personnalisé peut être défini dans le fichier IDL :

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Si la routine de liaison rencontre une erreur, elle doit lever une exception à l’aide de la fonction [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) . Le stub client est ensuite nettoyé et laisse le filtre d’exception au bloc d’exception entourant l’appel de procédure distante du côté client. Si la routine de liaison retourne simplement la **valeur null**, le code client obtient une \_ \_ liaison non valide des erreurs RPC S \_ . Bien que cela puisse être acceptable dans certains cas, d’autres situations (telles que la mémoire insuffisante) ne répondent pas bien. La routine Unbind doit être conçue de manière à ne pas échouer. La routine Unbind ne doit pas lever d’exceptions.

Les routines de liaison et de séparation définies par le programmeur s’affichent dans l’application cliente. Dans l’exemple suivant, la routine de liaison appelle [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour convertir les informations de liaison de chaîne en un handle de liaison. La routine Unbind appelle [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) pour libérer le handle de liaison.

Le nom du handle de liaison défini par le programmeur \_ , \_ type de handle de données, apparaît dans le cadre du nom des fonctions. Il est également utilisé comme type de paramètre dans les paramètres de fonction.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Les handles de liaison implicites et explicites peuvent être des handles primitifs ou personnalisés. Autrement dit, un descripteur peut être :

-   Primitive et implicite
-   Personnalisé et implicite
-   Primitive et Explicit
-   Personnalisé et explicite

 

 