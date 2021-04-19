---
description: Supprime l’objet IWiaItem2 actuel de l’arborescence d’objets de l’appareil.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2 ::D méthode eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516676"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="3544f-103">IWiaItem2 ::D méthode eleteItem</span><span class="sxs-lookup"><span data-stu-id="3544f-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="3544f-104">Supprime l’objet [**IWiaItem2**](-wia-iwiaitem2.md) actuel de l’arborescence d’objets de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3544f-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="3544f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3544f-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3544f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3544f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3544f-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3544f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3544f-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="3544f-108">Type: **LONG**</span></span>

<span data-ttu-id="3544f-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="3544f-109">Currently unused.</span></span> <span data-ttu-id="3544f-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="3544f-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3544f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3544f-111">Return value</span></span>

<span data-ttu-id="3544f-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3544f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3544f-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3544f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3544f-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3544f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3544f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3544f-115">Remarks</span></span>

<span data-ttu-id="3544f-116">Le système d’exécution Windows Image Acquisition (WIA) 2,0 représente chaque périphérique matériel WIA 2,0 connecté à l’ordinateur de l’utilisateur sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3544f-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="3544f-117">Un périphérique WIA 2,0 donné peut ou non autoriser les applications à supprimer des objets **IWiaItem2** de son arborescence.</span><span class="sxs-lookup"><span data-stu-id="3544f-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="3544f-118">Les éléments qui ont des enfants ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="3544f-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="3544f-119">L’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) doit être utilisée pour interroger l’appareil à la fonctionnalité de suppression d’éléments.</span><span class="sxs-lookup"><span data-stu-id="3544f-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="3544f-120">Si l’appareil prend en charge la suppression d’élément dans son arborescence [**IWiaItem2**](-wia-iwiaitem2.md) , appelez la méthode **IWiaItem2 ::D eleteitem** pour supprimer l’objet **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="3544f-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="3544f-121">Notez que cette méthode supprime uniquement un objet une fois que toutes les références à l’objet ont été libérées.</span><span class="sxs-lookup"><span data-stu-id="3544f-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="3544f-122">Si la suppression d’un élément a échoué, E \_ DELETEITEM est retourné.</span><span class="sxs-lookup"><span data-stu-id="3544f-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="3544f-123">La valeur numérique de cette erreur n’est pas encore définie.</span><span class="sxs-lookup"><span data-stu-id="3544f-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="3544f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3544f-124">Requirements</span></span>



| <span data-ttu-id="3544f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3544f-125">Requirement</span></span> | <span data-ttu-id="3544f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3544f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3544f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3544f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3544f-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3544f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3544f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3544f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3544f-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3544f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3544f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3544f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3544f-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3544f-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3544f-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3544f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3544f-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3544f-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




