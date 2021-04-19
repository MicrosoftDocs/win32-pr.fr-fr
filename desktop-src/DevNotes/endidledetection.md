---
description: Termine l’analyse de l’inactivité.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539684"
---
# <a name="endidledetection-function"></a><span data-ttu-id="cbea0-103">EndIdleDetection fonction)</span><span class="sxs-lookup"><span data-stu-id="cbea0-103">EndIdleDetection function</span></span>

<span data-ttu-id="cbea0-104">\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="cbea0-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="cbea0-105">Utilisez plutôt la fonction **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="cbea0-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="cbea0-106">Termine l’analyse de l’inactivité.</span><span class="sxs-lookup"><span data-stu-id="cbea0-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbea0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbea0-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="cbea0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbea0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbea0-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="cbea0-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="cbea0-110">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="cbea0-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbea0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbea0-111">Return value</span></span>

<span data-ttu-id="cbea0-112">Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="cbea0-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbea0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cbea0-113">Remarks</span></span>

<span data-ttu-id="cbea0-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cbea0-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="cbea0-115">Cette fonction n’est pas exportée par nom ; Spécifiez l’ordinal 4 lors de l’appel de **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="cbea0-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbea0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbea0-116">Requirements</span></span>



| <span data-ttu-id="cbea0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbea0-117">Requirement</span></span> | <span data-ttu-id="cbea0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbea0-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbea0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="cbea0-119">DLL</span></span><br/> | <dl> <span data-ttu-id="cbea0-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbea0-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbea0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbea0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbea0-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="cbea0-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
