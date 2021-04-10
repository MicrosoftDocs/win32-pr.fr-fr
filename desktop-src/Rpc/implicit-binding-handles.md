---
title: Handles de liaison implicites
description: Les handles de liaison implicite permettent à votre application de sélectionner un serveur spécifique pour exécuter ses appels de procédure distante.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031350"
---
# <a name="implicit-binding-handles"></a><span data-ttu-id="48e0f-103">Handles de liaison implicites</span><span class="sxs-lookup"><span data-stu-id="48e0f-103">Implicit Binding Handles</span></span>

<span data-ttu-id="48e0f-104">Les handles de liaison implicite permettent à votre application de sélectionner un serveur spécifique pour exécuter ses appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="48e0f-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="48e0f-105">Pour plus d’informations, consultez [liaison côté client](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="48e0f-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="48e0f-106">Ils permettent également à votre programme client/serveur d’utiliser des liaisons authentifiées.</span><span class="sxs-lookup"><span data-stu-id="48e0f-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="48e0f-107">Autrement dit, le client peut spécifier des informations d’authentification dans un handle de liaison implicite.</span><span class="sxs-lookup"><span data-stu-id="48e0f-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="48e0f-108">La bibliothèque Runtime RPC utilise les informations d’authentification pour établir une session RPC authentifiée entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="48e0f-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="48e0f-109">Pour plus d’informations, consultez [Sécurité](security.md).</span><span class="sxs-lookup"><span data-stu-id="48e0f-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="48e0f-110">Les handles de liaison implicite ne sont pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="48e0f-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="48e0f-111">Les applications multithread doivent donc éviter d’utiliser des handles de liaison implicites.</span><span class="sxs-lookup"><span data-stu-id="48e0f-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="48e0f-112">Lorsque votre application utilise des liaisons implicites, le client doit définir les informations de liaison afin qu’il puisse créer la liaison.</span><span class="sxs-lookup"><span data-stu-id="48e0f-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="48e0f-113">Une fois que le client a créé une liaison implicite, il n’est pas obligé de passer des handles de liaison à des procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="48e0f-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="48e0f-114">La bibliothèque RPC gère le reste du mécanisme de la session de communication.</span><span class="sxs-lookup"><span data-stu-id="48e0f-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="48e0f-115">Le client stocke les informations de liaison pour un handle implicite dans une variable globale.</span><span class="sxs-lookup"><span data-stu-id="48e0f-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="48e0f-116">Lorsque le compilateur MIDL génère le stub client et le fichier d’en-tête à partir de la spécification d’interface dans votre fichier MIDL, il génère également du code pour une variable de handle de liaison globale.</span><span class="sxs-lookup"><span data-stu-id="48e0f-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="48e0f-117">Votre programme client initialise le descripteur, puis ne se réfère pas à celui-ci jusqu’à ce qu’il détruise la liaison.</span><span class="sxs-lookup"><span data-stu-id="48e0f-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="48e0f-118">Vous créez un handle implicite en spécifiant l' \[ attribut de [**\_ handle implicite**](/windows/desktop/Midl/implicit-handle) \] dans le CCP pour une interface comme suit :</span><span class="sxs-lookup"><span data-stu-id="48e0f-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="48e0f-119">Le type **handle \_ t** , qui est utilisé dans l’exemple précédent, est un type de données MIDL utilisé pour définir des handles de liaison.</span><span class="sxs-lookup"><span data-stu-id="48e0f-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="48e0f-120">Après la création du handle implicite, l’application doit l’utiliser comme paramètre des fonctions de la bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="48e0f-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="48e0f-121">N’utilisez pas le handle implicite en tant que paramètre pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="48e0f-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="48e0f-122">L’exemple de code suivant illustre l’utilisation de handles de liaison implicites.</span><span class="sxs-lookup"><span data-stu-id="48e0f-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="48e0f-123">Dans l’exemple précédent, les fonctions de la bibliothèque Runtime RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) et [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) nécessitaient que le handle de liaison implicite soit passé dans leurs listes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="48e0f-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="48e0f-124">Toutefois, la procédure distante MyRemoteProcedure n’a pas été effectuée, car il ne s’agit pas d’une fonction de bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="48e0f-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 