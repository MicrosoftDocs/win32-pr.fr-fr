---
description: Crée un objet énumérateur et passe un pointeur vers son interface IEnumWiaItem2 pour les dossiers contenant des éléments dans l’arborescence IWiaItem2 d’un appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2 :: EnumChildItems, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485065"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="9e1c0-103">IWiaItem2 :: EnumChildItems, méthode</span><span class="sxs-lookup"><span data-stu-id="9e1c0-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="9e1c0-104">Crée un objet énumérateur et passe un pointeur vers son interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) pour les dossiers contenant des éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) d’un appareil WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e1c0-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="9e1c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e1c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1c0-107">*pCategoryGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e1c0-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1c0-108">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="9e1c0-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="9e1c0-109">Spécifie un pointeur vers une catégorie pour laquelle les nœuds enfants sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="9e1c0-110">Si _ \* NULL \* \*, tous les nœuds enfants sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="9e1c0-111">*ppIEnumWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e1c0-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1c0-112">Type : **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e1c0-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="9e1c0-113">Reçoit l’adresse d’un pointeur vers l’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) créée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1c0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e1c0-114">Return value</span></span>

<span data-ttu-id="9e1c0-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e1c0-115">Type: **HRESULT**</span></span>

<span data-ttu-id="9e1c0-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e1c0-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e1c0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1c0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9e1c0-118">Remarks</span></span>

<span data-ttu-id="9e1c0-119">Le système d’exécution WIA 2,0 représente chaque périphérique matériel WIA 2,0 sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="9e1c0-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="9e1c0-120">La méthode **IWiaItem2 :: EnumChildItems** permet aux applications d’énumérer les éléments enfants dans l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="9e1c0-121">Toutefois, il ne peut être appliqué qu’aux éléments qui sont des dossiers.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="9e1c0-122">Si le dossier n’est pas vide, il contient une sous-arborescence d’objets [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="9e1c0-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="9e1c0-123">La méthode **IWiaItem2 :: EnumChildItems** énumère tous les éléments contenus dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="9e1c0-124">Elle stocke un pointeur vers un énumérateur dans le paramètre *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="9e1c0-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="9e1c0-125">Les applications utilisent le pointeur d’énumérateur pour effectuer l’énumération des éléments enfants d’un objet.</span><span class="sxs-lookup"><span data-stu-id="9e1c0-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="9e1c0-126">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="9e1c0-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e1c0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e1c0-127">Requirements</span></span>



| <span data-ttu-id="9e1c0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e1c0-128">Requirement</span></span> | <span data-ttu-id="9e1c0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1c0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1c0-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e1c0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1c0-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e1c0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9e1c0-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e1c0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1c0-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e1c0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9e1c0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e1c0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1c0-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1c0-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e1c0-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="9e1c0-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e1c0-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e1c0-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
