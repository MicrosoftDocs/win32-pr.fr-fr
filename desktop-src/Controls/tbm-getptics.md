---
title: Message TBM_GETPTICS (commctrl. h)
description: Récupère l’adresse d’un tableau qui contient les positions des graduations d’un TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942161"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="44730-104">\_Message TBM GETPTICS</span><span class="sxs-lookup"><span data-stu-id="44730-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="44730-105">Récupère l’adresse d’un tableau qui contient les positions des graduations d’un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="44730-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="44730-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44730-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44730-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44730-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="44730-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="44730-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="44730-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44730-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="44730-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="44730-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44730-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44730-111">Return value</span></span>

<span data-ttu-id="44730-112">Retourne l’adresse d’un tableau de valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="44730-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="44730-113">Les éléments du tableau spécifient les positions logiques des graduations de la barre de suivi, à l’exclusion des première et dernière graduations créées par le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="44730-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="44730-114">Les positions logiques peuvent être n’importe laquelle des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="44730-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="44730-115">Notes</span><span class="sxs-lookup"><span data-stu-id="44730-115">Remarks</span></span>

<span data-ttu-id="44730-116">Le nombre d’éléments dans le tableau est inférieur au nombre de cycles renvoyé par le message [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="44730-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="44730-117">Notez que les valeurs du tableau peuvent inclure des positions en double et peuvent ne pas être dans l’ordre séquentiel.</span><span class="sxs-lookup"><span data-stu-id="44730-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="44730-118">Le pointeur retourné est valide jusqu’à ce que vous modifiiez les graduations de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="44730-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="44730-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44730-119">Requirements</span></span>



| <span data-ttu-id="44730-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44730-120">Requirement</span></span> | <span data-ttu-id="44730-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="44730-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44730-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44730-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44730-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44730-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44730-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44730-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44730-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44730-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44730-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="44730-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44730-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44730-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





