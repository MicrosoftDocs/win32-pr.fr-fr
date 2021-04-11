---
description: Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI :: ScanProfileDialog, méthode (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202889"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="42579-103">IScanProfileUI :: ScanProfileDialog, méthode</span><span class="sxs-lookup"><span data-stu-id="42579-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="42579-104">Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.</span><span class="sxs-lookup"><span data-stu-id="42579-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="42579-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42579-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="42579-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42579-107">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42579-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42579-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="42579-108">Type: **HWND**</span></span>

<span data-ttu-id="42579-109">Handle de la fenêtre parente qui possède la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="42579-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42579-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42579-110">Return value</span></span>

<span data-ttu-id="42579-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42579-111">Type: **HRESULT**</span></span>

<span data-ttu-id="42579-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42579-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42579-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42579-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42579-114">Notes</span><span class="sxs-lookup"><span data-stu-id="42579-114">Remarks</span></span>

<span data-ttu-id="42579-115">La boîte de dialogue est modale. l’utilisateur ne peut pas basculer vers la fenêtre parente tant que la boîte de dialogue n’est pas fermée.</span><span class="sxs-lookup"><span data-stu-id="42579-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="42579-116">Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="42579-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="42579-117">L' `<Default>` élément peut être ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="42579-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="42579-118">Aucune autre modification du profil d’analyse ne peut être effectuée dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="42579-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="42579-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42579-119">Requirements</span></span>



| <span data-ttu-id="42579-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42579-120">Requirement</span></span> | <span data-ttu-id="42579-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="42579-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="42579-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42579-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42579-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42579-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="42579-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42579-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42579-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42579-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42579-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="42579-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="42579-127"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="42579-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="42579-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="42579-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42579-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42579-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42579-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42579-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42579-131">**IScanProfileUI**</span><span class="sxs-lookup"><span data-stu-id="42579-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="42579-132">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="42579-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




