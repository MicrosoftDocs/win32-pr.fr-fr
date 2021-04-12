---
description: La classe CMediaEvent fournit l’implémentation de la classe de base des méthodes IDispatch du IMediaEvent à interface double. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211272"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="b1ff9-104">CMediaEvent, classe</span><span class="sxs-lookup"><span data-stu-id="b1ff9-104">CMediaEvent class</span></span>

![hiérarchie de la classe cmediaevent](images/cutil03.png)

<span data-ttu-id="b1ff9-106">La `CMediaEvent` classe fournit l’implémentation de la classe de base des méthodes **IDispatch** des [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)à deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="b1ff9-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="b1ff9-107">Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface **IMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="b1ff9-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="b1ff9-108">La `CMediaEvent` classe fournit également l’implémentation de la classe de base de l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) qui dérive de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="b1ff9-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="b1ff9-109">Les fonctions membres [**CMediaEvent :: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent :: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent :: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)et [**CMediaEvent :: Invoke**](cmediaevent-invoke.md) sont des implémentations standard de l’interface **IDispatch** à l’aide de la classe [**CBaseDispatch**](cbasedispatch.md) (et d’une bibliothèque de types) pour analyser les commandes et les passer aux méthodes virtuelles pures de l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="b1ff9-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="b1ff9-110">Fonctions de membre</span><span class="sxs-lookup"><span data-stu-id="b1ff9-110">Member Functions</span></span>                                         | <span data-ttu-id="b1ff9-111">Description</span><span class="sxs-lookup"><span data-stu-id="b1ff9-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ff9-112">**CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="b1ff9-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="b1ff9-113">Construit un objet **CMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="b1ff9-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="b1ff9-114">Méthodes IDispatch</span><span class="sxs-lookup"><span data-stu-id="b1ff9-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="b1ff9-115">Description</span><span class="sxs-lookup"><span data-stu-id="b1ff9-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="b1ff9-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="b1ff9-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="b1ff9-117">Mappe un membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peuvent être utilisés lors des appels suivants à la méthode **IDispatch :: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="b1ff9-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="b1ff9-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="b1ff9-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="b1ff9-119">Récupère un objet d’informations de type, qui récupère les informations de type pour une interface.</span><span class="sxs-lookup"><span data-stu-id="b1ff9-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="b1ff9-120">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="b1ff9-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="b1ff9-121">Récupère le nombre d’interfaces d’informations de type fournies par un objet.</span><span class="sxs-lookup"><span data-stu-id="b1ff9-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="b1ff9-122">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="b1ff9-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="b1ff9-123">Fournit l'accès aux propriétés et aux méthodes exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="b1ff9-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



