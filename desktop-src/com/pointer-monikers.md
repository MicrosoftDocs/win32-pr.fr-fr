---
title: Monikers de pointeur
description: Un moniker de pointeur identifie un objet qui ne peut exister qu’en état actif ou en cours d’exécution. Cela diffère des autres classes de monikers, qui identifient les objets qui peuvent exister dans l’état passif ou actif.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104381380"
---
# <a name="pointer-monikers"></a><span data-ttu-id="2fc26-104">Monikers de pointeur</span><span class="sxs-lookup"><span data-stu-id="2fc26-104">Pointer Monikers</span></span>

<span data-ttu-id="2fc26-105">Un *moniker de pointeur* identifie un objet qui ne peut exister qu’en état actif ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2fc26-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="2fc26-106">Cela diffère des autres classes de monikers, qui identifient les objets qui peuvent exister dans l’état passif ou actif.</span><span class="sxs-lookup"><span data-stu-id="2fc26-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="2fc26-107">Supposons, par exemple, qu’une application possède un objet qui n’a pas de représentation persistante.</span><span class="sxs-lookup"><span data-stu-id="2fc26-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="2fc26-108">Normalement, si un client de votre application a besoin d’accéder à cet objet, vous pouvez simplement transmettre au client un pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="2fc26-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="2fc26-109">Toutefois, supposons que votre client attende un moniker.</span><span class="sxs-lookup"><span data-stu-id="2fc26-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="2fc26-110">L’objet ne peut pas être identifié par un moniker de fichier, car il n’est pas stocké dans un fichier, ni avec un moniker d’élément, car il n’est pas contenu dans un autre objet.</span><span class="sxs-lookup"><span data-stu-id="2fc26-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="2fc26-111">Au lieu de cela, votre application peut créer un moniker de pointeur, qui est un moniker qui contient simplement un pointeur en interne et le transmet au client.</span><span class="sxs-lookup"><span data-stu-id="2fc26-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="2fc26-112">Le client peut traiter ce moniker comme tout autre.</span><span class="sxs-lookup"><span data-stu-id="2fc26-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="2fc26-113">Toutefois, lorsque le client appelle [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur le moniker du pointeur, le code du moniker ne vérifie pas la table ROT (Running Object Table) ou ne charge rien à partir du stockage.</span><span class="sxs-lookup"><span data-stu-id="2fc26-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="2fc26-114">Au lieu de cela, le code du moniker appelle simplement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur stocké à l’intérieur du moniker.</span><span class="sxs-lookup"><span data-stu-id="2fc26-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="2fc26-115">Les monikers de pointeur autorisent les objets qui existent uniquement dans l’état actif ou en cours d’exécution pour participer aux opérations de moniker et sont utilisés par les clients moniker.</span><span class="sxs-lookup"><span data-stu-id="2fc26-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="2fc26-116">Une différence importante entre les monikers de pointeur et d’autres classes de monikers est que les monikers de pointeur ne peuvent pas être enregistrés dans un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="2fc26-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="2fc26-117">Si vous le faites, l’appel de la méthode [**IMoniker :: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="2fc26-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="2fc26-118">Cela signifie que les monikers de pointeur sont utiles uniquement dans des situations particulières.</span><span class="sxs-lookup"><span data-stu-id="2fc26-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="2fc26-119">Vous pouvez utiliser la fonction [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) si vous devez utiliser un moniker de pointeur.</span><span class="sxs-lookup"><span data-stu-id="2fc26-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fc26-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2fc26-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc26-121">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="2fc26-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="2fc26-122">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="2fc26-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="2fc26-123">Monikers composites</span><span class="sxs-lookup"><span data-stu-id="2fc26-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="2fc26-124">Monikers de fichiers</span><span class="sxs-lookup"><span data-stu-id="2fc26-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="2fc26-125">Monikers d’élément</span><span class="sxs-lookup"><span data-stu-id="2fc26-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




