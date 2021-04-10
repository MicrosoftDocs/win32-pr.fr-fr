---
description: Fournit des méthodes pour fournir des paramètres de navigateur. L’interface IItemPreviewerExt est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interface IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951030"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="bc859-104">Interface IItemPreviewerExt</span><span class="sxs-lookup"><span data-stu-id="bc859-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="bc859-105">Fournit des méthodes pour fournir des paramètres de navigateur.</span><span class="sxs-lookup"><span data-stu-id="bc859-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="bc859-106">L’interface **IItemPreviewerExt** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bc859-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="bc859-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bc859-107">Members</span></span>

<span data-ttu-id="bc859-108">L’interface **IItemPreviewerExt** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bc859-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bc859-109">**IItemPreviewerExt** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc859-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="bc859-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bc859-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bc859-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bc859-111">Methods</span></span>

<span data-ttu-id="bc859-112">L’interface **IItemPreviewerExt** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bc859-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="bc859-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="bc859-113">Method</span></span>                                                                               | <span data-ttu-id="bc859-114">Description</span><span class="sxs-lookup"><span data-stu-id="bc859-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc859-115">**GetLinkedContent**</span><span class="sxs-lookup"><span data-stu-id="bc859-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="bc859-116">Autorise l’extension à du contenu riche pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="bc859-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="bc859-117">**GetRelatedPart**</span><span class="sxs-lookup"><span data-stu-id="bc859-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="bc859-118">Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.</span><span class="sxs-lookup"><span data-stu-id="bc859-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="bc859-119">**ProcessTransformCommand**</span><span class="sxs-lookup"><span data-stu-id="bc859-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="bc859-120">Autorise le traitement d’une commande de transformation rencontrée dans un modèle d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="bc859-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="bc859-121">**SuggestBrowserPolicy**</span><span class="sxs-lookup"><span data-stu-id="bc859-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="bc859-122">Suggère la stratégie de sécurité à appliquer au navigateur.</span><span class="sxs-lookup"><span data-stu-id="bc859-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="bc859-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bc859-123">Remarks</span></span>

<span data-ttu-id="bc859-124">L’interface **IItemPreviewerExt** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bc859-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="bc859-125">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **IItemPreviewerExt** et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc859-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc859-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc859-126">Requirements</span></span>



| <span data-ttu-id="bc859-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc859-127">Requirement</span></span> | <span data-ttu-id="bc859-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc859-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc859-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc859-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc859-130">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc859-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc859-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc859-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc859-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc859-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc859-133">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bc859-133">Redistributable</span></span><br/>          | <span data-ttu-id="bc859-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="bc859-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
