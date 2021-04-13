---
title: Monikers de classe
description: Bien que les classes soient généralement identifiées directement avec des CLSID dans des fonctions telles que CoCreateInstance ou CoGetClassObject, les classes peuvent également être identifiées par un moniker appelé un moniker de classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311176"
---
# <a name="class-monikers"></a><span data-ttu-id="ccd67-103">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="ccd67-103">Class Monikers</span></span>

<span data-ttu-id="ccd67-104">Bien que les classes soient généralement identifiées directement avec des CLSID dans des fonctions telles que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), les classes peuvent également être identifiées par un moniker appelé un *moniker de classe*.</span><span class="sxs-lookup"><span data-stu-id="ccd67-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="ccd67-105">Les monikers de classe sont liés à l’objet de classe de la classe pour laquelle ils sont créés.</span><span class="sxs-lookup"><span data-stu-id="ccd67-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="ccd67-106">La possibilité d’identifier des classes avec un moniker prend en charge des opérations utiles qui, sinon, ne sont pas difficiles à manier.</span><span class="sxs-lookup"><span data-stu-id="ccd67-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="ccd67-107">Par exemple, les monikers de fichiers traditionnellement prennent en charge la liaison riche uniquement à la classe associée à la classe de fichier à laquelle ils font appel ; le moniker d’un fichier Excel crée une liaison avec une instance d’un objet Excel, et un moniker d’une image GIF est lié à une instance du gestionnaire GIF actuellement inscrit.</span><span class="sxs-lookup"><span data-stu-id="ccd67-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="ccd67-108">Un moniker de classe vous permet d’indiquer la classe que vous souhaitez utiliser pour manipuler un fichier par le biais d’une composition avec un moniker de fichier.</span><span class="sxs-lookup"><span data-stu-id="ccd67-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="ccd67-109">Un moniker de classe pour une classe de graphique 3D composée d’un moniker à un fichier Excel produit un moniker qui se lie à une instance de l’objet de graphique 3D et initialise l’objet avec le contenu du fichier Excel.</span><span class="sxs-lookup"><span data-stu-id="ccd67-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="ccd67-110">Les monikers de classe sont donc particulièrement utiles dans la composition avec d’autres types de monikers, tels que des monikers de fichiers ou des monikers d’élément.</span><span class="sxs-lookup"><span data-stu-id="ccd67-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="ccd67-111">Les monikers de classes peuvent également être composés à droite des monikers qui prennent en charge la liaison à l’interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) .</span><span class="sxs-lookup"><span data-stu-id="ccd67-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="ccd67-112">Lorsqu’il est composé de cette manière, **IClassActivator** donne simplement accès à l’objet de classe et aux instances de la classe par le biais de [**IClassActivator :: GetClassObject,**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="ccd67-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="ccd67-113">Les monikers de classe peuvent être identifiés via [**IMoniker :: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), qui retourne MKSYS \_ CLASSMONIKER dans *pdwMksys*.</span><span class="sxs-lookup"><span data-stu-id="ccd67-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="ccd67-114">Les programmeurs créent généralement des monikers de classe à l’aide de la fonction [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) ou via [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="ccd67-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="ccd67-115">(Pour plus d’informations, consultez [**IMoniker ::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .)</span><span class="sxs-lookup"><span data-stu-id="ccd67-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccd67-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccd67-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccd67-117">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="ccd67-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="ccd67-118">Monikers composites</span><span class="sxs-lookup"><span data-stu-id="ccd67-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="ccd67-119">Monikers de fichiers</span><span class="sxs-lookup"><span data-stu-id="ccd67-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="ccd67-120">Monikers d’élément</span><span class="sxs-lookup"><span data-stu-id="ccd67-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="ccd67-121">Monikers de pointeur</span><span class="sxs-lookup"><span data-stu-id="ccd67-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




