---
description: Installe l’objet ActiveX spécifié.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'IeAxiSystemInstaller :: InitializeSystemInstaller, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867813"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="56c1c-103">IeAxiSystemInstaller :: InitializeSystemInstaller, méthode</span><span class="sxs-lookup"><span data-stu-id="56c1c-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="56c1c-104">La méthode **InitializeSystemInstaller** installe l’objet ActiveX spécifié.</span><span class="sxs-lookup"><span data-stu-id="56c1c-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c1c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56c1c-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="56c1c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c1c-107">*du bstrURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56c1c-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c1c-108">URL de l’objet ActiveX à installer.</span><span class="sxs-lookup"><span data-stu-id="56c1c-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="56c1c-109">*dwClientPID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56c1c-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c1c-110">ID de processus du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="56c1c-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="56c1c-111">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56c1c-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c1c-112">Pointeur vers une instance de l’interface [**IeAxiServiceCallback**](ieaxiservicecallback.md) qui vérifie si l’objet ActiveX est autorisé à être installé.</span><span class="sxs-lookup"><span data-stu-id="56c1c-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="56c1c-113">*pbstrNonce* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="56c1c-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56c1c-114">Contexte qui peut être utilisé pour partager des informations d’État dans les appels à d’autres méthodes utilisées pour vérifier et télécharger l’objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="56c1c-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c1c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56c1c-115">Return value</span></span>

<span data-ttu-id="56c1c-116">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56c1c-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="56c1c-117">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="56c1c-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="56c1c-118">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="56c1c-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="56c1c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56c1c-119">Requirements</span></span>



| <span data-ttu-id="56c1c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56c1c-120">Requirement</span></span> | <span data-ttu-id="56c1c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56c1c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c1c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56c1c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56c1c-123">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56c1c-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="56c1c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56c1c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56c1c-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="56c1c-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="56c1c-126">IID</span><span class="sxs-lookup"><span data-stu-id="56c1c-126">IID</span></span><br/>                      | <span data-ttu-id="56c1c-127">IID \_ IeAxiSystemInstaller est défini en tant que a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="56c1c-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="56c1c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56c1c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c1c-129">**IeAxiSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="56c1c-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

