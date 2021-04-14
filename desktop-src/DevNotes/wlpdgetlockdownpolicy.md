---
description: Appelle la bibliothèque pour récupérer l’état de sécurité relatif à l’hôte, et script ou MSI à utiliser.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: WldpGetLockdownPolicy, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523463"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="6a949-103">WldpGetLockdownPolicy fonction)</span><span class="sxs-lookup"><span data-stu-id="6a949-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="6a949-104">Appelle la bibliothèque pour récupérer l’état de sécurité relatif à l’hôte, et script ou MSI à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6a949-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="6a949-105">La fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="6a949-105">The function has no associated import library.</span></span> <span data-ttu-id="6a949-106">Vous devez utiliser les fonctions LoadLibrary et GetProcAddress pour établir une liaison dynamique à wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="6a949-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a949-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a949-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6a949-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a949-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a949-109">*hostInformation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6a949-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a949-110">Structure [**d' \_ \_ informations de l’hôte WLDP**](wldp-host-information.md) identifiant l’hôte et le fichier source à évaluer.</span><span class="sxs-lookup"><span data-stu-id="6a949-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="6a949-111">*lockdownState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a949-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a949-112">Fournit la valeur sécurisée de la stratégie obtenue.</span><span class="sxs-lookup"><span data-stu-id="6a949-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="6a949-113">Que! WLDP_LOCKDOWN_IS_OFF, UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="6a949-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="6a949-114">Vous pouvez également vérifier WLDP_LOCKDOWN_IS_AUDIT et WLDP_LOCKDOWN_IS_ENFORCE pour déterminer si une stratégie est en mode d’audit ou d’application.</span><span class="sxs-lookup"><span data-stu-id="6a949-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="6a949-115">*lockdownFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a949-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a949-116">Les valeurs d’indicateur suivantes sont définies WLDP \_ Flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – When set, ignorent la validation SaferIdentifyLevel, qui ignore si un script est signé.</span><span class="sxs-lookup"><span data-stu-id="6a949-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a949-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a949-117">Return value</span></span>

<span data-ttu-id="6a949-118">Cette méthode retourne S \_ OK en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6a949-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a949-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6a949-119">Remarks</span></span>

<span data-ttu-id="6a949-120">En cas d’appel \_ avec \_ les informations de l’hôte WLDP. SZSOURCE = null, la stratégie générique pour l’hôte est retournée.</span><span class="sxs-lookup"><span data-stu-id="6a949-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="6a949-121">En cas d’appel avec les informations de l' \_ hôte WLDP \_ . dwHostId = \_ ID d’hôte WLDP \_ \_ global, \_ informations sur l’hôte WLDP \_ . szSource doit avoir la valeur null et la fonction renverra la stratégie système globale.</span><span class="sxs-lookup"><span data-stu-id="6a949-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="6a949-122">Le SKIPSIGNATUREVALIDATION dwFlag WLDP \_ Flags \_ peut être utilisé pour ignorer la validation de SaferIdentifyLevel (), qui ignore si un script est signé.</span><span class="sxs-lookup"><span data-stu-id="6a949-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a949-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a949-123">Requirements</span></span>



| <span data-ttu-id="6a949-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a949-124">Requirement</span></span> | <span data-ttu-id="6a949-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a949-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6a949-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a949-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6a949-127">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a949-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6a949-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a949-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6a949-129">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a949-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a949-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a949-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a949-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a949-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a949-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6a949-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a949-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a949-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




