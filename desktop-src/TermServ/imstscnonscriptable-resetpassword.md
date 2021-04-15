---
title: Méthode IMsTscNonScriptable ResetPassword
description: Réinitialise tous les États de mot de passe dans le contrôle ActiveX Bureau à distance.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ResetPassword
- Méthode ResetPassword Services Bureau à distance, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, méthode ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466751"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="ad42a-106">IMsTscNonScriptable :: ResetPassword, méthode</span><span class="sxs-lookup"><span data-stu-id="ad42a-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="ad42a-107">Réinitialise tous les États de mot de passe dans le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ad42a-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="ad42a-108">Vous pouvez appeler cette méthode pour effacer les mots de passe qui sont stockés dans l’un des trois formats pris en charge : texte en clair, encodé portable ou encodé binaire (non transférable).</span><span class="sxs-lookup"><span data-stu-id="ad42a-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="ad42a-109">Notez que les mots de passe encodés ne doivent pas être considérés comme étant chiffrés de manière sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ad42a-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad42a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad42a-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="ad42a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad42a-111">Parameters</span></span>

<span data-ttu-id="ad42a-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad42a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad42a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad42a-113">Return value</span></span>

<span data-ttu-id="ad42a-114">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ad42a-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad42a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ad42a-115">Remarks</span></span>

<span data-ttu-id="ad42a-116">Vous pouvez appeler cette méthode pour réinitialiser le mot de passe du contrôle après la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="ad42a-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="ad42a-117">Cela garantit que les connexions suivantes qui utilisent la même instance du contrôle ne se connectent pas automatiquement avec un mot de passe défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="ad42a-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="ad42a-118">Vous pouvez appeler cette méthode uniquement lorsque le Bureau à distance contrôle ActiveX n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="ad42a-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="ad42a-119">Cette méthode retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="ad42a-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="ad42a-120">Pour vérifier l’état connecté, appelez la méthode [**obtenir la \_ connexion**](imstscax-connected.md) par le biais de l’interface [**IMsTscAx**](imstscax-interface.md) ou de l’une des interfaces qui en hérite.</span><span class="sxs-lookup"><span data-stu-id="ad42a-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="ad42a-121">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ad42a-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad42a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad42a-122">Requirements</span></span>



| <span data-ttu-id="ad42a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad42a-123">Requirement</span></span> | <span data-ttu-id="ad42a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad42a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad42a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad42a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad42a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad42a-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ad42a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad42a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad42a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad42a-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ad42a-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ad42a-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad42a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad42a-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad42a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ad42a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad42a-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad42a-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad42a-133">IID</span><span class="sxs-lookup"><span data-stu-id="ad42a-133">IID</span></span><br/>                      | <span data-ttu-id="ad42a-134">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="ad42a-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad42a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad42a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad42a-136">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="ad42a-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





