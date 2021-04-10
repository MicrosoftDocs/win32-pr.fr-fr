---
description: Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111175"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="35f8f-103">DvdLauncher fonction)</span><span class="sxs-lookup"><span data-stu-id="35f8f-103">DvdLauncher function</span></span>

<span data-ttu-id="35f8f-104">Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="35f8f-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35f8f-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="35f8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f8f-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35f8f-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f8f-108">Handle de la fenêtre de niveau supérieur à utiliser pour toute interface utilisateur requise.</span><span class="sxs-lookup"><span data-stu-id="35f8f-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="35f8f-109">Lettre de *lecteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35f8f-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f8f-110">Lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="35f8f-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f8f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35f8f-111">Return value</span></span>

<span data-ttu-id="35f8f-112">Si la fonction est réussie et que les régions correspondent, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="35f8f-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="35f8f-113">Sinon, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="35f8f-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35f8f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="35f8f-114">Remarks</span></span>

<span data-ttu-id="35f8f-115">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="35f8f-115">This function has no associated import library.</span></span> <span data-ttu-id="35f8f-116">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à StorProp.dll.</span><span class="sxs-lookup"><span data-stu-id="35f8f-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f8f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35f8f-117">Requirements</span></span>



| <span data-ttu-id="35f8f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35f8f-118">Requirement</span></span> | <span data-ttu-id="35f8f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="35f8f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f8f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35f8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35f8f-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="35f8f-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="35f8f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35f8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35f8f-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35f8f-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="35f8f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="35f8f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f8f-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f8f-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f8f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35f8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f8f-127">Fonctions de gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="35f8f-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

