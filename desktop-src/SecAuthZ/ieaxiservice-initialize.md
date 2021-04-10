---
description: Vérifie et télécharge un objet ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'IeAxiService :: Initialize, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210438"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="d2ea4-103">IeAxiService :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="d2ea4-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="d2ea4-104">La méthode **Initialize** vérifie et télécharge un objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="d2ea4-105">Si l’objet satisfait aux exigences de stratégie, cette méthode initialise un objet système qui installe l’objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ea4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2ea4-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="d2ea4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2ea4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ea4-108">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-109">Handle vers la fenêtre parente de la fenêtre qui tente d’installer le contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-110">*dwClientPID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-111">ID de processus du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-112">*bstrDesktop* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-113">Bureau de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-114">*bstrClsID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-115">ID de classe de l’objet ActiveX à installer.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-116">*du bstrURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-117">URL de l’objet ActiveX à installer.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-118">*pbstrNonce* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-119">Contexte qui peut être utilisé pour partager des informations d’État dans les appels à d’autres méthodes utilisées pour vérifier et télécharger l’objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea4-120">*ppISyncBrokerInterface* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea4-121">Pointeur vers l’instance de l’interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) qui installe le contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ea4-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2ea4-122">Return value</span></span>

<span data-ttu-id="d2ea4-123">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="d2ea4-124">Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="d2ea4-125">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d2ea4-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="d2ea4-126">Description</span><span class="sxs-lookup"><span data-stu-id="d2ea4-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="d2ea4-127">Niveau de <dt>**confiance \_ E \_ sujet \_ non \_ approuvé**</dt> <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea4-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="d2ea4-128">L’objet ActiveX ne doit pas être installé.</span><span class="sxs-lookup"><span data-stu-id="d2ea4-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d2ea4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2ea4-129">Requirements</span></span>



| <span data-ttu-id="d2ea4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2ea4-130">Requirement</span></span> | <span data-ttu-id="d2ea4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ea4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ea4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ea4-133">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2ea4-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2ea4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ea4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ea4-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ea4-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="d2ea4-136">IID</span><span class="sxs-lookup"><span data-stu-id="d2ea4-136">IID</span></span><br/>                      | <span data-ttu-id="d2ea4-137">IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="d2ea4-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d2ea4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2ea4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ea4-139">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="d2ea4-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




