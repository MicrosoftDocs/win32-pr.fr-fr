---
description: Représente un objet stylet.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interface ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868682"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="a5669-103">Interface ITabletCursor</span><span class="sxs-lookup"><span data-stu-id="a5669-103">ITabletCursor interface</span></span>

<span data-ttu-id="a5669-104">Représente un objet stylet.</span><span class="sxs-lookup"><span data-stu-id="a5669-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="a5669-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a5669-105">Members</span></span>

<span data-ttu-id="a5669-106">L’interface **ITabletCursor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a5669-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a5669-107">**ITabletCursor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a5669-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="a5669-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5669-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a5669-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5669-109">Methods</span></span>

<span data-ttu-id="a5669-110">L’interface **ITabletCursor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a5669-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="a5669-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="a5669-111">Method</span></span>                                                 | <span data-ttu-id="a5669-112">Description</span><span class="sxs-lookup"><span data-stu-id="a5669-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="a5669-113">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="a5669-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="a5669-114">Récupère l’objet bouton spécifié à partir d’un stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="a5669-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="a5669-115">**GetButtonCount**</span><span class="sxs-lookup"><span data-stu-id="a5669-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="a5669-116">Récupère le nombre de boutons sur le stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="a5669-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="a5669-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="a5669-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="a5669-118">Récupère l’identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="a5669-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="a5669-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a5669-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="a5669-120">Récupère le nom du stylet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="a5669-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="a5669-121">**IsInverted**</span><span class="sxs-lookup"><span data-stu-id="a5669-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="a5669-122">Indique si le stylet est à l’envers.</span><span class="sxs-lookup"><span data-stu-id="a5669-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="a5669-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a5669-123">Remarks</span></span>

<span data-ttu-id="a5669-124">N'utilisez pas cette interface.</span><span class="sxs-lookup"><span data-stu-id="a5669-124">Do not use this interface.</span></span>

<span data-ttu-id="a5669-125">Le code suivant décrit comment l’interface **ITabletCursor** est définie.</span><span class="sxs-lookup"><span data-stu-id="a5669-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="a5669-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5669-126">Requirements</span></span>



| <span data-ttu-id="a5669-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5669-127">Requirement</span></span> | <span data-ttu-id="a5669-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5669-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5669-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5669-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a5669-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5669-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5669-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5669-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a5669-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5669-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a5669-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a5669-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5669-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5669-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

