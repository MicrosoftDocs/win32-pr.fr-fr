---
title: Quand utiliser la table d’interface globale
description: Quand utiliser la table d’interface globale
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031901"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="32833-103">Quand utiliser la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="32833-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="32833-104">Si vous démarshalez plusieurs fois un pointeur d’interface entre des cloisonnements dans un processus, vous pouvez utiliser l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="32833-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="32833-105">Avec d’autres techniques, vous devez remarshaler chaque fois.</span><span class="sxs-lookup"><span data-stu-id="32833-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="32833-106">Si le pointeur d’interface n’est démarshalé qu’une seule fois, vous souhaiterez peut-être utiliser la fonction [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) .</span><span class="sxs-lookup"><span data-stu-id="32833-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="32833-107">Elle peut également être utilisée pour passer un pointeur d’interface d’un thread à un autre dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="32833-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="32833-108">L’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) complique également un autre problème précédemment difficile pour le programmeur.</span><span class="sxs-lookup"><span data-stu-id="32833-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="32833-109">Ce problème se produit lorsque les conditions suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="32833-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="32833-110">Un objet agile in-process agrège le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="32833-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="32833-111">Ce même objet agile contient également des pointeurs d’interface (comme variables membres) vers d’autres objets qui ne sont pas agiles et qui n’agrègent pas le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="32833-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="32833-112">Dans ce cas, si l’objet externe est marshalé vers un autre cloisonnement et que l’application y appelle, et que l’objet tente d’appeler sur l’un de ses pointeurs d’interface de variable membre qui ne sont pas libres de threads ou qui sont des proxies vers des objets d’autres Apartments, il peut obtenir des résultats incorrects ou le \_ thread RPC E \_ incorrect \_ .</span><span class="sxs-lookup"><span data-stu-id="32833-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="32833-113">Cette erreur se produit parce que l’interface interne est conçue pour être appelée uniquement à partir du cloisonnement dans lequel elle a été stockée pour la première fois dans la variable membre.</span><span class="sxs-lookup"><span data-stu-id="32833-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="32833-114">Pour résoudre ce problème, l’objet externe qui agrège le marshaleur libre de threads doit appeler [**IGlobalInterfaceTable :: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) sur l’interface interne et stocker le cookie résultant dans sa variable membre, au lieu de stocker le pointeur d’interface réel.</span><span class="sxs-lookup"><span data-stu-id="32833-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="32833-115">Lorsque l’objet externe souhaite appeler sur le pointeur d’interface d’un objet interne, il doit appeler [**IGlobalInterfaceTable :: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), utiliser le pointeur d’interface retourné, puis le libérer.</span><span class="sxs-lookup"><span data-stu-id="32833-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="32833-116">Lorsque l’objet externe disparaît, il doit appeler [**IGlobalInterfaceTable :: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) pour supprimer l’interface de la table d’interface globale.</span><span class="sxs-lookup"><span data-stu-id="32833-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32833-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32833-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32833-118">Création de la table d’interface globale</span><span class="sxs-lookup"><span data-stu-id="32833-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 