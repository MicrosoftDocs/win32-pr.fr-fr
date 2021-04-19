---
description: Fournit une méthode pour appeler des objets ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interface ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517460"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="205b4-103">Interface ISearchProtocolUI</span><span class="sxs-lookup"><span data-stu-id="205b4-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="205b4-104">Fournit une méthode pour appeler des objets [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="205b4-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="205b4-105">Les méthodes de cette interface sont appelées par l’hôte de protocole lors du traitement des URL à partir du Rassembleur.</span><span class="sxs-lookup"><span data-stu-id="205b4-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="205b4-106">Le gestionnaire de protocole implémente le protocole d’accès à une source de contenu dans son format natif, et cette interface implémente un gestionnaire de protocole personnalisé pour développer les sources de données qui peuvent être indexées.</span><span class="sxs-lookup"><span data-stu-id="205b4-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="205b4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="205b4-107">Members</span></span>

<span data-ttu-id="205b4-108">L’interface **ISearchProtocolUI** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="205b4-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="205b4-109">**ISearchProtocolUI** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="205b4-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="205b4-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="205b4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="205b4-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="205b4-111">Methods</span></span>

<span data-ttu-id="205b4-112">L’interface **ISearchProtocolUI** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="205b4-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="205b4-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="205b4-113">Method</span></span>                                                                       | <span data-ttu-id="205b4-114">Description</span><span class="sxs-lookup"><span data-stu-id="205b4-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="205b4-115">**GetSearchItemForUrl**</span><span class="sxs-lookup"><span data-stu-id="205b4-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="205b4-116">Obtient l’élément de recherche pour les données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="205b4-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="205b4-117">Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="205b4-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="205b4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="205b4-118">Remarks</span></span>

<span data-ttu-id="205b4-119">L’interface **ISearchProtocolUI** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="205b4-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="205b4-120">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **ISearchProtocolUI** et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="205b4-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="205b4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="205b4-121">Requirements</span></span>



| <span data-ttu-id="205b4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="205b4-122">Requirement</span></span> | <span data-ttu-id="205b4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="205b4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="205b4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="205b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="205b4-125">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="205b4-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="205b4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="205b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="205b4-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="205b4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="205b4-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="205b4-128">Redistributable</span></span><br/>          | <span data-ttu-id="205b4-129">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="205b4-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
