---
description: Étend l’interface ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interface ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543529"
---
# <a name="itablet2-interface"></a><span data-ttu-id="0afcb-103">Interface ITablet2</span><span class="sxs-lookup"><span data-stu-id="0afcb-103">ITablet2 interface</span></span>

<span data-ttu-id="0afcb-104">Étend l' [**interface ITablet**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="0afcb-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="0afcb-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0afcb-105">Members</span></span>

<span data-ttu-id="0afcb-106">L’interface **ITablet2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0afcb-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0afcb-107">**ITablet2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0afcb-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="0afcb-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0afcb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0afcb-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0afcb-109">Methods</span></span>

<span data-ttu-id="0afcb-110">L’interface **ITablet2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0afcb-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="0afcb-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0afcb-111">Method</span></span>                                          | <span data-ttu-id="0afcb-112">Description</span><span class="sxs-lookup"><span data-stu-id="0afcb-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0afcb-113">**GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="0afcb-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="0afcb-114">Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.</span><span class="sxs-lookup"><span data-stu-id="0afcb-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0afcb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0afcb-115">Remarks</span></span>

<span data-ttu-id="0afcb-116">Cette interface a été introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0afcb-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="0afcb-117">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="0afcb-117">Developers should not use this interface.</span></span>

<span data-ttu-id="0afcb-118">Le code suivant décrit comment l’interface **ITablet2** est définie.</span><span class="sxs-lookup"><span data-stu-id="0afcb-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="0afcb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0afcb-119">Requirements</span></span>



| <span data-ttu-id="0afcb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0afcb-120">Requirement</span></span> | <span data-ttu-id="0afcb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0afcb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0afcb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0afcb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0afcb-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0afcb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0afcb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0afcb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0afcb-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0afcb-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0afcb-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0afcb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0afcb-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0afcb-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

