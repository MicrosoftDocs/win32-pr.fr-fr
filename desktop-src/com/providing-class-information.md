---
title: Fournir des informations sur la classe
description: Fournir des informations sur la classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100700"
---
# <a name="providing-class-information"></a><span data-ttu-id="b1a22-103">Fournir des informations sur la classe</span><span class="sxs-lookup"><span data-stu-id="b1a22-103">Providing Class Information</span></span>

<span data-ttu-id="b1a22-104">Il est souvent utile pour un client d’un objet d’examiner les informations de type de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1a22-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="b1a22-105">À partir du CLSID de l’objet, un client peut localiser la bibliothèque de types de l’objet à l’aide des entrées de Registre, puis peut analyser la bibliothèque de types pour l’entrée de coclasse de la bibliothèque correspondant au CLSID.</span><span class="sxs-lookup"><span data-stu-id="b1a22-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="b1a22-106">Toutefois, tous les objets n’ont pas de CLSID, bien qu’ils aient encore besoin de fournir des informations de type.</span><span class="sxs-lookup"><span data-stu-id="b1a22-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="b1a22-107">En outre, il est commode pour un client d’avoir un moyen de demander simplement à un objet ses informations de type au lieu de passer par tous les caractère fastidieux pour extraire les mêmes informations à partir des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="b1a22-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="b1a22-108">Cette fonctionnalité est importante lorsque vous traitez des interfaces sortantes sur des objets connectables.</span><span class="sxs-lookup"><span data-stu-id="b1a22-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="b1a22-109">(Pour plus d’informations sur la façon dont les objets connectables offrent cette fonctionnalité, consultez [utilisation de IProvideClassInfo](using-iprovideclassinfo.md) .)</span><span class="sxs-lookup"><span data-stu-id="b1a22-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="b1a22-110">Dans ce cas, un client peut interroger l’objet pour [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="b1a22-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="b1a22-111">Si ces interfaces existent, le client appelle la méthode [**GetClassinfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) pour obtenir les informations de type de l’interface.</span><span class="sxs-lookup"><span data-stu-id="b1a22-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="b1a22-112">En implémentant [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un objet spécifie qu’il peut fournir des informations de type pour toute la classe. autrement dit, ce qu’il décrirait dans sa section coclasse de sa bibliothèque de types, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b1a22-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="b1a22-113">[**GetClassinfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) retourne un pointeur **ITypeInfo** qui correspond aux informations de coclasse de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1a22-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="b1a22-114">Grâce à ce pointeur **ITypeInfo** , le client peut examiner toutes les définitions d’interface entrantes et sortantes de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1a22-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="b1a22-115">L’objet peut également fournir des [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="b1a22-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="b1a22-116">L’interface **IProvideClassInfo2** est une extension simple de [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) qui permet de récupérer rapidement et facilement les identificateurs d’interface sortants d’un objet pour son jeu d’événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1a22-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="b1a22-117">**IProvideClassInfo2** est dérivée de **IProvideClassInfo**.</span><span class="sxs-lookup"><span data-stu-id="b1a22-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1a22-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1a22-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a22-119">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="b1a22-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




