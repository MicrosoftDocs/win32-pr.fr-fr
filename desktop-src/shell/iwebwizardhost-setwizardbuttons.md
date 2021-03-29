---
description: Met à jour les boutons précédent, suivant et terminer dans le frame de l’Assistant du client.
title: Méthode WebWizardHost. SetWizardButtons (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973498"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="8a6e9-103">Méthode WebWizardHost. SetWizardButtons</span><span class="sxs-lookup"><span data-stu-id="8a6e9-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="8a6e9-104">Met à jour les boutons **précédent**, **suivant** et **Terminer** dans le frame de l’Assistant du client.</span><span class="sxs-lookup"><span data-stu-id="8a6e9-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a6e9-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="8a6e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a6e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6e9-107">*vbEnableBack* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6e9-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6e9-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8a6e9-108">Type: **Boolean**</span></span>

<span data-ttu-id="8a6e9-109">Active le bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="8a6e9-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="8a6e9-110">*vbEnableNext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6e9-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6e9-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8a6e9-111">Type: **Boolean**</span></span>

<span data-ttu-id="8a6e9-112">Active le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8a6e9-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="8a6e9-113">*vbLastPage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6e9-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6e9-114">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8a6e9-114">Type: **Boolean**</span></span>

<span data-ttu-id="8a6e9-115">Active le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="8a6e9-115">Enables the **Finish** button.</span></span> <span data-ttu-id="8a6e9-116">Indique qu’il s’agit de la dernière page côté serveur.</span><span class="sxs-lookup"><span data-stu-id="8a6e9-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a6e9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8a6e9-117">Remarks</span></span>

<span data-ttu-id="8a6e9-118">Veillez à implémenter des fonctions de gestionnaire dans chaque page côté serveur pour OnBack () et OnNext (), correspondant aux boutons d’Assistant **précédent** et **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8a6e9-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="8a6e9-119">Les fonctions OnBack () et OnNext () répondent à **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="8a6e9-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="8a6e9-120">Au moment opportun, la fonction OnNext () appelle **SetWizardButtons** avec *vbLastPage* = **true**, qui peut activer un bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="8a6e9-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="8a6e9-121">OnNext () appelle également [**FinalNext**](iwebwizardhost-finalnext.md) quand un utilisateur clique sur le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="8a6e9-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6e9-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8a6e9-122">Requirements</span></span>



| <span data-ttu-id="8a6e9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a6e9-123">Requirement</span></span> | <span data-ttu-id="8a6e9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a6e9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6e9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a6e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6e9-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a6e9-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8a6e9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a6e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6e9-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a6e9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a6e9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a6e9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a6e9-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a6e9-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a6e9-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="8a6e9-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a6e9-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a6e9-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




