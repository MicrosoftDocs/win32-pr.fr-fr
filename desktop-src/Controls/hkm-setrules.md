---
title: Message HKM_SETRULES (commctrl. h)
description: Définit les combinaisons non valides et la combinaison de modificateur par défaut pour un contrôle de touche d’accès rapide.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES les contrôles de message Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465694"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="81a9f-104">\_Message hkm SETRULES</span><span class="sxs-lookup"><span data-stu-id="81a9f-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="81a9f-105">Définit les combinaisons non valides et la combinaison de modificateur par défaut pour un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="81a9f-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="81a9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81a9f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81a9f-108">Tableau d’indicateurs qui spécifient des combinaisons de touches non valides.</span><span class="sxs-lookup"><span data-stu-id="81a9f-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="81a9f-109">Ce paramètre peut être une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="81a9f-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="81a9f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="81a9f-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="81a9f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="81a9f-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="81a9f-112"><dt>**HKCOMB \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="81a9f-113">Alt</span><span class="sxs-lookup"><span data-stu-id="81a9f-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="81a9f-114"><dt>**HKCOMB \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="81a9f-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="81a9f-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="81a9f-116"><dt>**\_autorité de certification HKCOMB**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="81a9f-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="81a9f-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="81a9f-118"><dt>**HKCOMB \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="81a9f-119">Clés non modifiées</span><span class="sxs-lookup"><span data-stu-id="81a9f-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="81a9f-120"><dt>**HKCOMB \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="81a9f-121">MAJUSCULE</span><span class="sxs-lookup"><span data-stu-id="81a9f-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="81a9f-122"><dt>**HKCOMB \_ sa**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="81a9f-123">Maj+Alt</span><span class="sxs-lookup"><span data-stu-id="81a9f-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="81a9f-124"><dt>**HKCOMB \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="81a9f-125">MAJ + CTRL</span><span class="sxs-lookup"><span data-stu-id="81a9f-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="81a9f-126"><dt>**HKCOMB \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="81a9f-127">MAJ + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="81a9f-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="81a9f-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81a9f-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81a9f-129">Tableau d’indicateurs qui spécifient la combinaison de touches à utiliser lorsque l’utilisateur entre une combinaison non valide.</span><span class="sxs-lookup"><span data-stu-id="81a9f-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="81a9f-130">Pour obtenir la liste des valeurs d’indicateur de modification, consultez la description du message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="81a9f-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a9f-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81a9f-131">Return value</span></span>

<span data-ttu-id="81a9f-132">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="81a9f-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a9f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="81a9f-133">Remarks</span></span>

<span data-ttu-id="81a9f-134">Lorsqu’un utilisateur entre une combinaison de touches non valide, comme défini par les indicateurs spécifiés dans *wParam*, le système utilise l’opérateur or au niveau du bit pour combiner les clés entrées par l’utilisateur avec les indicateurs spécifiés dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="81a9f-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="81a9f-135">La combinaison de touches obtenue est convertie en chaîne, puis affichée dans le contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="81a9f-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a9f-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81a9f-136">Requirements</span></span>



| <span data-ttu-id="81a9f-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81a9f-137">Requirement</span></span> | <span data-ttu-id="81a9f-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="81a9f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81a9f-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81a9f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="81a9f-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81a9f-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81a9f-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81a9f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="81a9f-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81a9f-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81a9f-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="81a9f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a9f-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a9f-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





