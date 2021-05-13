---
description: Expose des méthodes qui permettent à un dossier de Shell de prendre en charge différentes vues sur son contenu (différentes dispositions hiérarchiques de ses données).
title: Interface IShellFolderViewType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: f3ccb4073d59e0ebe9b840bd6f8f592f463e1e46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842690"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="71c44-103">Interface IShellFolderViewType</span><span class="sxs-lookup"><span data-stu-id="71c44-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="71c44-104">Expose des méthodes qui permettent à un dossier de Shell de prendre en charge différentes vues sur son contenu (différentes dispositions hiérarchiques de ses données).</span><span class="sxs-lookup"><span data-stu-id="71c44-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="71c44-105">Membres</span><span class="sxs-lookup"><span data-stu-id="71c44-105">Members</span></span>

<span data-ttu-id="71c44-106">L’interface **IShellFolderViewType** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71c44-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="71c44-107">**IShellFolderViewType** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71c44-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="71c44-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71c44-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="71c44-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71c44-109">Methods</span></span>

<span data-ttu-id="71c44-110">L’interface **IShellFolderViewType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="71c44-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="71c44-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="71c44-111">Method</span></span>                                                                      | <span data-ttu-id="71c44-112">Description</span><span class="sxs-lookup"><span data-stu-id="71c44-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71c44-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="71c44-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="71c44-114">Récupère un énumérateur qui retourne un PIDL pour chaque vue étendue.</span><span class="sxs-lookup"><span data-stu-id="71c44-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="71c44-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="71c44-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="71c44-116">Obtient le nom de la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="71c44-116">Gets the name of the default view.</span></span> <span data-ttu-id="71c44-117">Appelez [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer les noms des autres vues.</span><span class="sxs-lookup"><span data-stu-id="71c44-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="71c44-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="71c44-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="71c44-119">Obtient les propriétés de la vue.</span><span class="sxs-lookup"><span data-stu-id="71c44-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="71c44-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="71c44-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="71c44-121">Reconstruit un PIDL à partir d’une représentation hiérarchique du dossier Shell dans une représentation différente.</span><span class="sxs-lookup"><span data-stu-id="71c44-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="71c44-122">Notes</span><span class="sxs-lookup"><span data-stu-id="71c44-122">Remarks</span></span>

<span data-ttu-id="71c44-123">Cet énumérateur retourne des PIDL qui sont des dossiers masqués spéciaux au niveau supérieur du dossier shell, qui ne sont pas énumérés autrement.</span><span class="sxs-lookup"><span data-stu-id="71c44-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="71c44-124">La vue par défaut est celle qui s’affiche normalement dans le dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="71c44-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="71c44-125">Cette interface n’est définie dans aucun fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="71c44-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="71c44-126">Si vous choisissez d’implémenter cette interface, vous pouvez utiliser le code C/C++ suivant pour déclarer ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="71c44-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="71c44-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71c44-127">Requirements</span></span>



| <span data-ttu-id="71c44-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c44-128">Requirement</span></span> | <span data-ttu-id="71c44-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c44-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71c44-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c44-130">Minimum supported client</span></span><br/> | <span data-ttu-id="71c44-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c44-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71c44-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71c44-132">Minimum supported server</span></span><br/> | <span data-ttu-id="71c44-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71c44-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71c44-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71c44-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c44-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71c44-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
