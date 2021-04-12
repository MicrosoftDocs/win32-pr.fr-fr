---
description: Obtient un nombre aléatoire 128 bits et sécurisé par chiffrement à partir d’un objet de sortie protégé.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: GetOPMRandomNumber fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317957"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="863d2-103">GetOPMRandomNumber fonction)</span><span class="sxs-lookup"><span data-stu-id="863d2-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="863d2-104">Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="863d2-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="863d2-105">Les applications ne doivent pas appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="863d2-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="863d2-106">Obtient un nombre aléatoire 128 bits et sécurisé par chiffrement à partir d’un objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="863d2-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="863d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="863d2-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="863d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="863d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="863d2-109">*opoOPMProtectedOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="863d2-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="863d2-110">Handle de l’objet de sortie protégé.</span><span class="sxs-lookup"><span data-stu-id="863d2-110">A handle to the protected output object.</span></span> <span data-ttu-id="863d2-111">Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="863d2-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="863d2-112">*prnRandomNumber* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="863d2-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="863d2-113">Pointeur vers une structure **de \_ \_ \_ nombres aléatoires OPM DXGKMDT** qui reçoit le nombre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="863d2-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="863d2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="863d2-114">Return value</span></span>

<span data-ttu-id="863d2-115">Si la méthode réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="863d2-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="863d2-116">Sinon, elle retourne un code d’erreur **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="863d2-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="863d2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="863d2-117">Remarks</span></span>

<span data-ttu-id="863d2-118">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="863d2-118">This function has no associated import library.</span></span> <span data-ttu-id="863d2-119">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="863d2-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="863d2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="863d2-120">Requirements</span></span>



| <span data-ttu-id="863d2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="863d2-121">Requirement</span></span> | <span data-ttu-id="863d2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="863d2-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="863d2-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="863d2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="863d2-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="863d2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="863d2-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="863d2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="863d2-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="863d2-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="863d2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="863d2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="863d2-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="863d2-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="863d2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="863d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863d2-130">Fonctions OPM</span><span class="sxs-lookup"><span data-stu-id="863d2-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="863d2-131">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="863d2-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
