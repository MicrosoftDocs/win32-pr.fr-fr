---
description: Fournit des méthodes qui définissent l’interaction entre une interface utilisateur et les objets d’espace de noms de recherche créés par l’indexeur.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interface ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393463"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="a8ca1-103">Interface ISearchItem</span><span class="sxs-lookup"><span data-stu-id="a8ca1-103">ISearchItem interface</span></span>

<span data-ttu-id="a8ca1-104">Fournit des méthodes qui définissent l’interaction entre une interface utilisateur et les objets d’espace de noms de recherche créés par l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="a8ca1-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="a8ca1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a8ca1-105">Members</span></span>

<span data-ttu-id="a8ca1-106">L’interface **ISearchItem** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a8ca1-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8ca1-107">**ISearchItem** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a8ca1-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="a8ca1-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8ca1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8ca1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8ca1-109">Methods</span></span>

<span data-ttu-id="a8ca1-110">L’interface **ISearchItem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a8ca1-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="a8ca1-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="a8ca1-111">Method</span></span>                                                         | <span data-ttu-id="a8ca1-112">Description</span><span class="sxs-lookup"><span data-stu-id="a8ca1-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8ca1-113">**GetParentFolder**</span><span class="sxs-lookup"><span data-stu-id="a8ca1-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="a8ca1-114">Obtient l’objet **ISearchItem** si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).</span><span class="sxs-lookup"><span data-stu-id="a8ca1-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="a8ca1-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8ca1-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="a8ca1-116">Obtient l’objet de l’interface utilisateur (IU) de **ISearchItem**.</span><span class="sxs-lookup"><span data-stu-id="a8ca1-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="a8ca1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a8ca1-117">Remarks</span></span>

<span data-ttu-id="a8ca1-118">[**ISearchItem :: GetParentFolder**](-search-isearchitem-getparentfolder.md) est pris en charge uniquement sur Windows XP et windows Server 2003, et ne doit plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a8ca1-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a8ca1-119">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **ISearchItem** et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)et [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ca1-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ca1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8ca1-120">Requirements</span></span>



| <span data-ttu-id="a8ca1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8ca1-121">Requirement</span></span> | <span data-ttu-id="a8ca1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8ca1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8ca1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8ca1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ca1-124">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8ca1-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8ca1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8ca1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ca1-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8ca1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8ca1-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a8ca1-127">Redistributable</span></span><br/>          | <span data-ttu-id="a8ca1-128">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a8ca1-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
