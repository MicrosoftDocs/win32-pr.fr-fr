---
title: Handles de liaison primitifs et personnalisés
description: Tous les handles déclarés avec le handle \_ t ou les \_ types de handle de liaison RPC \_ sont des handles de liaison primitifs.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031741"
---
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="9531f-103">Handles de liaison primitifs et personnalisés</span><span class="sxs-lookup"><span data-stu-id="9531f-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="9531f-104">Tous les handles déclarés avec le [handle \_ t](/windows/desktop/Midl/handle-t) ou les types de [**\_ \_ handle de liaison RPC**](rpc-binding-handle.md) sont des handles de liaison primitifs.</span><span class="sxs-lookup"><span data-stu-id="9531f-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="9531f-105">Vous pouvez étendre les types de [**\_ \_ handle**](rpc-binding-handle.md) de handle [ \_ t](/windows/desktop/Midl/handle-t) ou RPC pour inclure davantage ou des informations différentes que le type de handle primitif contient.</span><span class="sxs-lookup"><span data-stu-id="9531f-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="9531f-106">Dans ce cas, vous créez un handle de liaison personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9531f-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="9531f-107">Pour créer un handle de liaison personnalisé pour votre application distribuée, vous devez créer votre propre type de données et spécifier l' \[ [](/windows/desktop/Midl/handle) \] attribut handle sur une définition de type dans votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="9531f-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="9531f-108">Enfin, les fichiers stub mappent des handles de liaison personnalisés à des handles primitifs.</span><span class="sxs-lookup"><span data-stu-id="9531f-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="9531f-109">Si vous créez votre propre type de handle de liaison, vous devez également fournir des routines de liaison et de séparation que le stub client utilise pour mapper un handle personnalisé à un handle primitif.</span><span class="sxs-lookup"><span data-stu-id="9531f-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="9531f-110">Le stub appelle vos routines de liaison et de séparation au début et à la fin de chaque appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9531f-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="9531f-111">Les routines de liaison et de liaison doivent être conformes aux prototypes de fonction suivants.</span><span class="sxs-lookup"><span data-stu-id="9531f-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="9531f-112">Prototype de fonction</span><span class="sxs-lookup"><span data-stu-id="9531f-112">Function prototype</span></span>                     | <span data-ttu-id="9531f-113">Description</span><span class="sxs-lookup"><span data-stu-id="9531f-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="9531f-114">handle \_ t type \_ Bind (*type*)</span><span class="sxs-lookup"><span data-stu-id="9531f-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="9531f-115">Routine de liaison</span><span class="sxs-lookup"><span data-stu-id="9531f-115">Binding routine</span></span>   |
| <span data-ttu-id="9531f-116">void \_ , type Unbind (*type*, *handle \_ t*)</span><span class="sxs-lookup"><span data-stu-id="9531f-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="9531f-117">Routine de dissociation</span><span class="sxs-lookup"><span data-stu-id="9531f-117">Unbinding routine</span></span> |



 

<span data-ttu-id="9531f-118">L’exemple suivant montre comment un handle de liaison personnalisé peut être défini dans le fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="9531f-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

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

<span data-ttu-id="9531f-119">Si la routine de liaison rencontre une erreur, elle doit lever une exception à l’aide de la fonction [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) .</span><span class="sxs-lookup"><span data-stu-id="9531f-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="9531f-120">Le stub client est ensuite nettoyé et laisse le filtre d’exception au bloc d’exception entourant l’appel de procédure distante du côté client.</span><span class="sxs-lookup"><span data-stu-id="9531f-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="9531f-121">Si la routine de liaison retourne simplement la **valeur null**, le code client obtient une \_ \_ liaison non valide des erreurs RPC S \_ .</span><span class="sxs-lookup"><span data-stu-id="9531f-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="9531f-122">Bien que cela puisse être acceptable dans certains cas, d’autres situations (telles que la mémoire insuffisante) ne répondent pas bien.</span><span class="sxs-lookup"><span data-stu-id="9531f-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="9531f-123">La routine Unbind doit être conçue de manière à ne pas échouer.</span><span class="sxs-lookup"><span data-stu-id="9531f-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="9531f-124">La routine Unbind ne doit pas lever d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="9531f-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="9531f-125">Les routines de liaison et de séparation définies par le programmeur s’affichent dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="9531f-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="9531f-126">Dans l’exemple suivant, la routine de liaison appelle [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour convertir les informations de liaison de chaîne en un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="9531f-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="9531f-127">La routine Unbind appelle [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) pour libérer le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="9531f-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="9531f-128">Le nom du handle de liaison défini par le programmeur \_ , \_ type de handle de données, apparaît dans le cadre du nom des fonctions.</span><span class="sxs-lookup"><span data-stu-id="9531f-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="9531f-129">Il est également utilisé comme type de paramètre dans les paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="9531f-129">It is also used as the parameter type in the function parameters.</span></span>

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

<span data-ttu-id="9531f-130">Les handles de liaison implicites et explicites peuvent être des handles primitifs ou personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9531f-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="9531f-131">Autrement dit, un descripteur peut être :</span><span class="sxs-lookup"><span data-stu-id="9531f-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="9531f-132">Primitive et implicite</span><span class="sxs-lookup"><span data-stu-id="9531f-132">Primitive and implicit</span></span>
-   <span data-ttu-id="9531f-133">Personnalisé et implicite</span><span class="sxs-lookup"><span data-stu-id="9531f-133">Custom and implicit</span></span>
-   <span data-ttu-id="9531f-134">Primitive et Explicit</span><span class="sxs-lookup"><span data-stu-id="9531f-134">Primitive and explicit</span></span>
-   <span data-ttu-id="9531f-135">Personnalisé et explicite</span><span class="sxs-lookup"><span data-stu-id="9531f-135">Custom and explicit</span></span>

 

 