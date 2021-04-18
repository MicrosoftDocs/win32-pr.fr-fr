---
description: L’interface ITablet3 active l’interrogation multipoint pour l’entrée.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interface ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536622"
---
# <a name="itablet3-interface"></a><span data-ttu-id="d57e8-103">Interface ITablet3</span><span class="sxs-lookup"><span data-stu-id="d57e8-103">ITablet3 interface</span></span>

<span data-ttu-id="d57e8-104">L’interface ITablet3 active l’interrogation multipoint pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="d57e8-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="d57e8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d57e8-105">Members</span></span>

<span data-ttu-id="d57e8-106">L’interface **ITablet3** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d57e8-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d57e8-107">**ITablet3** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d57e8-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="d57e8-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d57e8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d57e8-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d57e8-109">Methods</span></span>

<span data-ttu-id="d57e8-110">L’interface **ITablet3** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d57e8-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="d57e8-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d57e8-111">Method</span></span>                                                  | <span data-ttu-id="d57e8-112">Description</span><span class="sxs-lookup"><span data-stu-id="d57e8-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="d57e8-113">**GetMaximumCursors**</span><span class="sxs-lookup"><span data-stu-id="d57e8-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="d57e8-114">Récupère le nombre maximal d’entrées prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d57e8-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="d57e8-115">**isMultiTouch**</span><span class="sxs-lookup"><span data-stu-id="d57e8-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="d57e8-116">Indique si l’interaction tactile est activée pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="d57e8-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d57e8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d57e8-117">Remarks</span></span>

<span data-ttu-id="d57e8-118">Les développeurs ne doivent pas utiliser cette interface</span><span class="sxs-lookup"><span data-stu-id="d57e8-118">Developers should not use this interface</span></span>

<span data-ttu-id="d57e8-119">Le code suivant décrit comment l’interface **ITablet3** est définie.</span><span class="sxs-lookup"><span data-stu-id="d57e8-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="d57e8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d57e8-120">Requirements</span></span>



| <span data-ttu-id="d57e8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57e8-121">Requirement</span></span> | <span data-ttu-id="d57e8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57e8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d57e8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d57e8-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57e8-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d57e8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d57e8-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57e8-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d57e8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d57e8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d57e8-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d57e8-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

