---
title: Clients moniker
description: Les clients moniker doivent commencer par obtenir un moniker, et il existe plusieurs façons pour un client moniker d’obtenir un moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526721"
---
# <a name="moniker-clients"></a><span data-ttu-id="0cba3-103">Clients moniker</span><span class="sxs-lookup"><span data-stu-id="0cba3-103">Moniker Clients</span></span>

<span data-ttu-id="0cba3-104">Les clients moniker doivent commencer par obtenir un moniker, et il existe plusieurs façons pour un client moniker d’obtenir un moniker.</span><span class="sxs-lookup"><span data-stu-id="0cba3-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="0cba3-105">Par exemple, dans les documents composés OLE, lorsque l’utilisateur final crée un élément lié (à l’aide de la boîte de dialogue **Insérer un objet** , du presse-papiers ou du glisser-déplacer), un moniker est incorporé dans le cadre de l’élément lié.</span><span class="sxs-lookup"><span data-stu-id="0cba3-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="0cba3-106">Dans ce cas, le programmeur a un contact minimal avec les monikers.</span><span class="sxs-lookup"><span data-stu-id="0cba3-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="0cba3-107">Par programmation, si vous avez un pointeur d’interface vers un objet qui implémente l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , vous pouvez l’utiliser pour obtenir un moniker, et il existe des méthodes sur d’autres interfaces définies pour retourner des monikers.</span><span class="sxs-lookup"><span data-stu-id="0cba3-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="0cba3-108">Il existe différents types de monikers, qui sont utilisés pour identifier différents genres d’objets, mais pour un client moniker, tous les monikers ont le même aspect.</span><span class="sxs-lookup"><span data-stu-id="0cba3-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="0cba3-109">Un client moniker appelle simplement [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur un moniker et obtient un pointeur d’interface vers l’objet que le moniker identifie.</span><span class="sxs-lookup"><span data-stu-id="0cba3-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="0cba3-110">Que le moniker identifie un objet aussi grand qu’une feuille de calcul entière ou aussi petit qu’une cellule unique dans une feuille de calcul, l’appel de **BindToObject** retourne un pointeur vers cet objet.</span><span class="sxs-lookup"><span data-stu-id="0cba3-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="0cba3-111">Si l’objet est déjà en cours d’exécution, **BindToObject** le trouvera en mémoire.</span><span class="sxs-lookup"><span data-stu-id="0cba3-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="0cba3-112">Si l’objet est stocké passivement sur le disque, **BindToObject** localise un serveur pour cet objet, exécute le serveur et fait en sorte que le serveur remet l’objet à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0cba3-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="0cba3-113">Tous les détails du processus de liaison sont masqués dans le client moniker.</span><span class="sxs-lookup"><span data-stu-id="0cba3-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="0cba3-114">Ainsi, pour un client moniker, l’utilisation du moniker est très simple.</span><span class="sxs-lookup"><span data-stu-id="0cba3-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cba3-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cba3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cba3-116">Fournisseurs de moniker</span><span class="sxs-lookup"><span data-stu-id="0cba3-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="0cba3-117">Implémentations du moniker OLE</span><span class="sxs-lookup"><span data-stu-id="0cba3-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




