---
description: Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche. Cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interface IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112387"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="428e3-104">Interface IItemPropertyBag</span><span class="sxs-lookup"><span data-stu-id="428e3-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="428e3-105">Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche.</span><span class="sxs-lookup"><span data-stu-id="428e3-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="428e3-106">Cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="428e3-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="428e3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="428e3-107">Members</span></span>

<span data-ttu-id="428e3-108">L’interface **IItemPropertyBag** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="428e3-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="428e3-109">**IItemPropertyBag** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="428e3-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="428e3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="428e3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="428e3-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="428e3-111">Methods</span></span>

<span data-ttu-id="428e3-112">L’interface **IItemPropertyBag** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="428e3-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="428e3-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="428e3-113">Method</span></span>                                                      | <span data-ttu-id="428e3-114">Description</span><span class="sxs-lookup"><span data-stu-id="428e3-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="428e3-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="428e3-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="428e3-116">Obtient le nombre de propriétés dans le conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="428e3-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="428e3-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="428e3-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="428e3-118">Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="428e3-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="428e3-119">**En lecture**</span><span class="sxs-lookup"><span data-stu-id="428e3-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="428e3-120">Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés.</span><span class="sxs-lookup"><span data-stu-id="428e3-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="428e3-121">**Ecrire**</span><span class="sxs-lookup"><span data-stu-id="428e3-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="428e3-122">Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="428e3-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="428e3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="428e3-123">Remarks</span></span>

<span data-ttu-id="428e3-124">L’interface **IItemPropertyBag** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="428e3-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="428e3-125">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **IItemPropertyBag** et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="428e3-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="428e3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="428e3-126">Requirements</span></span>



| <span data-ttu-id="428e3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="428e3-127">Requirement</span></span> | <span data-ttu-id="428e3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="428e3-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="428e3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="428e3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="428e3-130">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="428e3-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="428e3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="428e3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="428e3-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="428e3-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="428e3-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="428e3-133">Redistributable</span></span><br/>          | <span data-ttu-id="428e3-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="428e3-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
