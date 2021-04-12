---
description: Représente des informations générales sur un bouton sur un appareil de stylet.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interface ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319722"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="4fb68-103">Interface ITabletCursorButton</span><span class="sxs-lookup"><span data-stu-id="4fb68-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="4fb68-104">Représente des informations générales sur un bouton sur un appareil de stylet.</span><span class="sxs-lookup"><span data-stu-id="4fb68-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="4fb68-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4fb68-105">Members</span></span>

<span data-ttu-id="4fb68-106">L’interface **ITabletCursorButton** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4fb68-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4fb68-107">**ITabletCursorButton** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4fb68-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="4fb68-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4fb68-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4fb68-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4fb68-109">Methods</span></span>

<span data-ttu-id="4fb68-110">L’interface **ITabletCursorButton** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4fb68-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="4fb68-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="4fb68-111">Method</span></span>                                         | <span data-ttu-id="4fb68-112">Description</span><span class="sxs-lookup"><span data-stu-id="4fb68-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="4fb68-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="4fb68-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="4fb68-114">Récupère l’identificateur unique du bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="4fb68-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="4fb68-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="4fb68-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="4fb68-116">Récupère le nom du bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="4fb68-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="4fb68-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4fb68-117">Remarks</span></span>

<span data-ttu-id="4fb68-118">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="4fb68-118">Developers should not use this interface.</span></span>

<span data-ttu-id="4fb68-119">Le code suivant illustre la définition de l’interface **ITabletCursorButton** .</span><span class="sxs-lookup"><span data-stu-id="4fb68-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="4fb68-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fb68-120">Requirements</span></span>



| <span data-ttu-id="4fb68-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fb68-121">Requirement</span></span> | <span data-ttu-id="4fb68-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fb68-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb68-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fb68-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb68-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fb68-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4fb68-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fb68-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb68-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fb68-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4fb68-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4fb68-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fb68-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fb68-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb68-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fb68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb68-130">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="4fb68-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

