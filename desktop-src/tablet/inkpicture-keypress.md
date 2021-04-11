---
description: Se produit lorsqu’une touche est enfoncée alors que le contrôle InkPicture a le focus.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Événement InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951292"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="93c35-103">Événement InkPicture. KeyPress</span><span class="sxs-lookup"><span data-stu-id="93c35-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="93c35-104">Se produit lorsqu’une touche est enfoncée alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="93c35-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93c35-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="93c35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93c35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c35-107">*KeyAscii* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="93c35-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c35-108">Valeur ASCII de la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="93c35-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c35-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93c35-109">Return value</span></span>

<span data-ttu-id="93c35-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="93c35-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c35-111">Notes</span><span class="sxs-lookup"><span data-stu-id="93c35-111">Remarks</span></span>

<span data-ttu-id="93c35-112">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="93c35-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="93c35-113">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEKeyPress.</span><span class="sxs-lookup"><span data-stu-id="93c35-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c35-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93c35-114">Requirements</span></span>



| <span data-ttu-id="93c35-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93c35-115">Requirement</span></span> | <span data-ttu-id="93c35-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="93c35-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c35-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c35-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93c35-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93c35-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="93c35-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c35-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93c35-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c35-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="93c35-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="93c35-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c35-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93c35-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="93c35-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93c35-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="93c35-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c35-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="93c35-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c35-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="93c35-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

