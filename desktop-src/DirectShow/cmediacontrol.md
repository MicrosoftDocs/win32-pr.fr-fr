---
description: La classe CMediaControl fournit la gestion de classe de base des méthodes IDispatch de l’IMediaControl à interface double. Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869594"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="4bfe4-104">CMediaControl, classe</span><span class="sxs-lookup"><span data-stu-id="4bfe4-104">CMediaControl class</span></span>

![hiérarchie de la classe cmediacontrol](images/cutil02.png)

<span data-ttu-id="4bfe4-106">La `CMediaControl` classe fournit la gestion de classe de base des méthodes [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) de l' [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)à interface double.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="4bfe4-107">Il laisse en tant que virtuel pur les propriétés et les méthodes de l’interface **IMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="4bfe4-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="4bfe4-108">En règle générale, le gestionnaire de graphes de filtres est le seul objet qui implémente l’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="4bfe4-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="4bfe4-109">(les filtres implémentent l’interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , héritée par [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), pour recevoir des commandes de contrôle du gestionnaire de graphique de filtre.) Par conséquent, cette bibliothèque de classes est un usage limité pour filtrer les développeurs.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="4bfe4-110">Les fonctions membres [**CMediaControl :: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl :: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl :: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)et [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) sont des implémentations standard des méthodes [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) à l’aide de la classe [**CBaseDispatch**](cbasedispatch.md) (et d’une bibliothèque de types) pour analyser les commandes et les passer aux méthodes virtuelles pures de l’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="4bfe4-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="4bfe4-111">Les méthodes [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , définies dans Control. ODL, sont laissées comme des virtuels purs.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="4bfe4-112">Fonctions de membre</span><span class="sxs-lookup"><span data-stu-id="4bfe4-112">Member Functions</span></span>                                           | <span data-ttu-id="4bfe4-113">Description</span><span class="sxs-lookup"><span data-stu-id="4bfe4-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfe4-114">**CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="4bfe4-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="4bfe4-115">Construit un objet **CMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="4bfe4-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="4bfe4-116">Méthodes IDispatch</span><span class="sxs-lookup"><span data-stu-id="4bfe4-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="4bfe4-117">Description</span><span class="sxs-lookup"><span data-stu-id="4bfe4-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="4bfe4-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="4bfe4-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="4bfe4-119">Mappe un membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (DISPID), qui peuvent être utilisés lors des appels suivants à la méthode [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="4bfe4-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="4bfe4-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="4bfe4-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="4bfe4-121">Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="4bfe4-122">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="4bfe4-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="4bfe4-123">Récupère le nombre d’interfaces d’informations de type fournies par un objet.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="4bfe4-124">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="4bfe4-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="4bfe4-125">Fournit l'accès aux propriétés et aux méthodes exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="4bfe4-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
