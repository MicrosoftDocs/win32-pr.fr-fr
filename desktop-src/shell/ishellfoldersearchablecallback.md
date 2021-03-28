---
description: Expose des routines de rappel pour surveiller le processus de recherche.
title: Interface IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: aac648861f3bf9dc5ae8fdcc7173792e427b234f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991133"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="67f89-103">Interface IShellFolderSearchableCallback</span><span class="sxs-lookup"><span data-stu-id="67f89-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="67f89-104">Expose des routines de rappel pour surveiller le processus de recherche.</span><span class="sxs-lookup"><span data-stu-id="67f89-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="67f89-105">Membres</span><span class="sxs-lookup"><span data-stu-id="67f89-105">Members</span></span>

<span data-ttu-id="67f89-106">L’interface **IShellFolderSearchableCallback** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67f89-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67f89-107">**IShellFolderSearchableCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67f89-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="67f89-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67f89-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67f89-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67f89-109">Methods</span></span>

<span data-ttu-id="67f89-110">L’interface **IShellFolderSearchableCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="67f89-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="67f89-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="67f89-111">Method</span></span>                                                      | <span data-ttu-id="67f89-112">Description</span><span class="sxs-lookup"><span data-stu-id="67f89-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="67f89-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="67f89-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="67f89-114">Indique qu’une recherche a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="67f89-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="67f89-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="67f89-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="67f89-116">Indique qu’une recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="67f89-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67f89-117">Notes</span><span class="sxs-lookup"><span data-stu-id="67f89-117">Remarks</span></span>

<span data-ttu-id="67f89-118">Cette interface n’est définie dans aucun fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="67f89-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="67f89-119">Si vous choisissez d’implémenter cette interface, vous pouvez utiliser le code C/C++ suivant pour déclarer ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="67f89-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchableCallback Methods _**

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="67f89-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="67f89-120">Requirements</span></span>



| <span data-ttu-id="67f89-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67f89-121">Requirement</span></span> | <span data-ttu-id="67f89-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f89-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f89-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f89-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67f89-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f89-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67f89-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f89-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67f89-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f89-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="67f89-127">DLL</span><span class="sxs-lookup"><span data-stu-id="67f89-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f89-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f89-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
