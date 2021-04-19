---
description: Obtient l’objet ISearchItem si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'ISearchItem :: GetParentFolder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517240"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="813df-103">ISearchItem :: GetParentFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="813df-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="813df-104">Obtient l’objet [**ISearchItem**](-search-isearchitem.md) si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).</span><span class="sxs-lookup"><span data-stu-id="813df-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="813df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="813df-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="813df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="813df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="813df-107">*IShellFolder* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="813df-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="813df-108">Type : **ppShellFolder \* \***</span><span class="sxs-lookup"><span data-stu-id="813df-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="813df-109">Au retour, contient l’adresse d’un pointeur vers le dossier qui contient l’URL actuelle.</span><span class="sxs-lookup"><span data-stu-id="813df-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="813df-110">L' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est exposée par tous les objets de dossier de l’espace de noms Shell, et ses méthodes sont utilisées pour gérer les dossiers.</span><span class="sxs-lookup"><span data-stu-id="813df-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="813df-111">*LPITEMIDLIST* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="813df-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="813df-112">Tapez : \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="813df-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="813df-113">Au retour, contient l’adresse d’un pointeur vers une liste d’identificateurs d’éléments (PIDL) qui identifie le dossier parent.</span><span class="sxs-lookup"><span data-stu-id="813df-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="813df-114">Le paramètre _LPITEMIDLIST \* peut faire référence à un objet à n’importe quel niveau sous le dossier parent dans la hiérarchie d’espaces de noms, et peut donc être un pointeur à plusieurs niveaux vers un **PIDL** relatif au dossier parent.</span><span class="sxs-lookup"><span data-stu-id="813df-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="813df-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="813df-115">Return value</span></span>

<span data-ttu-id="813df-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="813df-116">Type: **HRESULT**</span></span>

<span data-ttu-id="813df-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="813df-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="813df-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="813df-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="813df-119">Notes</span><span class="sxs-lookup"><span data-stu-id="813df-119">Remarks</span></span>

<span data-ttu-id="813df-120">La méthode **ISearchItem :: GetParentFolder** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="813df-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="813df-121">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**ISearchItem**](-search-isearchitem.md) et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)et [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="813df-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="813df-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="813df-122">Requirements</span></span>



| <span data-ttu-id="813df-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="813df-123">Requirement</span></span> | <span data-ttu-id="813df-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="813df-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="813df-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="813df-125">Minimum supported client</span></span><br/> | <span data-ttu-id="813df-126">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="813df-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="813df-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="813df-127">Minimum supported server</span></span><br/> | <span data-ttu-id="813df-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="813df-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="813df-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="813df-129">Redistributable</span></span><br/>          | <span data-ttu-id="813df-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="813df-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="813df-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="813df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813df-132">**ISearchItem**</span><span class="sxs-lookup"><span data-stu-id="813df-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
