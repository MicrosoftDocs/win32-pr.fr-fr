---
title: Création de la table d’interface globale
description: Création de la table d’interface globale
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383007"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="42c8c-103">Création de la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="42c8c-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="42c8c-104">Utilisez l’appel suivant pour créer l’objet de table d’interface globale et obtenir un pointeur vers [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span><span class="sxs-lookup"><span data-stu-id="42c8c-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="42c8c-105">Lors de la création de l’objet table d’interface globale à l’aide de l’appel précédent, il est nécessaire de créer un lien vers la bibliothèque UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="42c8c-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="42c8c-106">Cela permet de résoudre les symboles externes CLSID \_ StdGlobalInterfaceTable et IID \_ IGlobalInterfaceTable.</span><span class="sxs-lookup"><span data-stu-id="42c8c-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="42c8c-107">Comme il existe une seule instance de la table d’interface globale par processus, tous les appels à cette fonction dans un processus retournent la même instance.</span><span class="sxs-lookup"><span data-stu-id="42c8c-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="42c8c-108">Après l’appel à la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , inscrivez l’interface à partir du cloisonnement dans lequel elle réside avec un appel à la méthode [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) .</span><span class="sxs-lookup"><span data-stu-id="42c8c-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="42c8c-109">Cette méthode fournit un cookie qui identifie l’interface et son emplacement.</span><span class="sxs-lookup"><span data-stu-id="42c8c-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="42c8c-110">Un cloisonnement qui recherche un pointeur vers cette interface appelle ensuite la méthode [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) avec ce cookie, et l’implémentation fournit ensuite un pointeur d’interface vers le cloisonnement appelant.</span><span class="sxs-lookup"><span data-stu-id="42c8c-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="42c8c-111">Pour révoquer l’inscription globale de l’interface, tout cloisonnement peut appeler la méthode [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .</span><span class="sxs-lookup"><span data-stu-id="42c8c-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="42c8c-112">Un exemple simple d’utilisation de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) serait lorsque vous souhaiterez passer un pointeur d’interface sur un objet dans un thread cloisonné (STA) à un thread de travail dans un autre cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="42c8c-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="42c8c-113">Plutôt que d’avoir à les marshaler dans un flux et à passer le flux au thread de travail en tant que paramètre de thread, **IGlobalInterfaceTable** vous permet simplement de passer un cookie.</span><span class="sxs-lookup"><span data-stu-id="42c8c-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="42c8c-114">Lorsque vous inscrivez l’interface dans la table d’interface globale, vous recevez un cookie que vous pouvez utiliser au lieu de passer le pointeur réel (chaque fois que vous devez passer le pointeur) à un paramètre de non-méthode qui passe à un autre cloisonnement (en tant que paramètre de [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) via [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) ou à la mémoire en cours d’exécution accessible en dehors de votre cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="42c8c-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="42c8c-115">La prudence est nécessaire, car l’utilisation d’interfaces globales place la charge supplémentaire sur le programmeur de gestion des problèmes tels que les conditions de concurrence et l’exclusion mutuelle, qui sont associées à l’accès à l’état global à partir de plusieurs threads simultanément.</span><span class="sxs-lookup"><span data-stu-id="42c8c-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="42c8c-116">COM fournit une implémentation standard de l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="42c8c-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="42c8c-117">Il est vivement recommandé d’utiliser cette implémentation standard, car elle fournit une fonctionnalité thread-safe complète.</span><span class="sxs-lookup"><span data-stu-id="42c8c-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42c8c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42c8c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42c8c-119">Quand utiliser la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="42c8c-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 