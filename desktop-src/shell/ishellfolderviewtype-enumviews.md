---
description: Récupère un énumérateur qui retourne un pointeur vers une liste d’identificateurs d’élément (PIDL) pour chaque vue étendue.
title: 'IShellFolderViewType :: EnumViews, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991136"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="4b14a-103">IShellFolderViewType :: EnumViews, méthode</span><span class="sxs-lookup"><span data-stu-id="4b14a-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="4b14a-104">Récupère un énumérateur qui retourne un pointeur vers une liste d’identificateurs d’élément (PIDL) pour chaque vue étendue.</span><span class="sxs-lookup"><span data-stu-id="4b14a-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b14a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b14a-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="4b14a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b14a-107">*grfFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b14a-108">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="4b14a-108">Type: **ULONG**</span></span>

<span data-ttu-id="4b14a-109">Indicateurs spécifiant les éléments à inclure dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="4b14a-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="4b14a-110">Pour obtenir la liste des valeurs possibles, consultez le type énuméré [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) .</span><span class="sxs-lookup"><span data-stu-id="4b14a-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="4b14a-111">Ce paramètre peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="4b14a-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="4b14a-112">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b14a-113">Type : **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="4b14a-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="4b14a-114">Adresse d’une variable pointeur de type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) qui reçoit l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4b14a-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b14a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b14a-115">Return value</span></span>

<span data-ttu-id="4b14a-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b14a-116">Type: **HRESULT**</span></span>

<span data-ttu-id="4b14a-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4b14a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b14a-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b14a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b14a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4b14a-119">Remarks</span></span>

<span data-ttu-id="4b14a-120">Les vues sont représentées à l’utilisateur en tant que dossiers masqués dans le répertoire racine (représenté par PIDL).</span><span class="sxs-lookup"><span data-stu-id="4b14a-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="4b14a-121">Le cas échéant, l’affichage par défaut (à partir du dossier racine) est représenté sous la forme **null**, ou vide, PIDL.</span><span class="sxs-lookup"><span data-stu-id="4b14a-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b14a-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4b14a-122">Requirements</span></span>



| <span data-ttu-id="4b14a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b14a-123">Requirement</span></span> | <span data-ttu-id="4b14a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b14a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b14a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b14a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4b14a-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4b14a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b14a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4b14a-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b14a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4b14a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b14a-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b14a-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




