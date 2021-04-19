---
title: RoFailFastWithErrorContextInternal2 fonction)
description: Déclenche une exception non continuable dans le processus en cours et vous permet également d’inclure un contexte d’erreur supplémentaire qui n’a pas déjà été capturé par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511717"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="d5b19-103">RoFailFastWithErrorContextInternal2 fonction)</span><span class="sxs-lookup"><span data-stu-id="d5b19-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="d5b19-104">Déclenche une exception non continuable dans le processus en cours et vous permet également d’inclure un contexte d’erreur supplémentaire qui n’a pas déjà été capturé par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d5b19-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5b19-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="d5b19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5b19-106">Parameters</span></span>

`hrError`

<span data-ttu-id="d5b19-107">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b19-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="d5b19-108">**HRESULT** associé à l’erreur actuelle.</span><span class="sxs-lookup"><span data-stu-id="d5b19-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="d5b19-109">L’exception est levée pour toute valeur de *hrError*.</span><span class="sxs-lookup"><span data-stu-id="d5b19-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="d5b19-110">Type : **[ULong](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b19-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b19-111">Nombre d’éléments dans le tableau *aStowedExceptionPointers* .</span><span class="sxs-lookup"><span data-stu-id="d5b19-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="d5b19-112">Type : **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="d5b19-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="d5b19-113">Tableau de pointeurs vers des structures de [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="d5b19-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="d5b19-114">Chaque structure contient des informations qui décrivent une exception arrimée.</span><span class="sxs-lookup"><span data-stu-id="d5b19-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="d5b19-115">Les informations de ces structures sont ensuite envoyées à Rapport d’erreurs Windows (WER), ainsi que les informations sur les exceptions qui ont été capturées par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="d5b19-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5b19-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5b19-116">Return value</span></span>

<span data-ttu-id="d5b19-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d5b19-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b19-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d5b19-118">Remarks</span></span>

<span data-ttu-id="d5b19-119">**RoFailFastWithErrorContextInternal2** n’est pas associé à une bibliothèque d’importation ni à un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d5b19-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="d5b19-120">Vous pouvez l’appeler en utilisant d’abord la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (pour charger `ComBase.dll` ), puis en appelant la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse de **RoFailFastWithErrorContextInternal2**.</span><span class="sxs-lookup"><span data-stu-id="d5b19-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="d5b19-121">Pour plus d’informations, consultez [fonction RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="d5b19-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b19-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5b19-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d5b19-123">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="d5b19-123">**Target Platform**</span></span> | <span data-ttu-id="d5b19-124">Windows</span><span class="sxs-lookup"><span data-stu-id="d5b19-124">Windows</span></span> |
| <span data-ttu-id="d5b19-125">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="d5b19-125">**Header**</span></span> | <span data-ttu-id="d5b19-126">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b19-126">N/A</span></span> |
| <span data-ttu-id="d5b19-127">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="d5b19-127">**Library**</span></span> | <span data-ttu-id="d5b19-128">N/A</span><span class="sxs-lookup"><span data-stu-id="d5b19-128">N/A</span></span> |
| <span data-ttu-id="d5b19-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="d5b19-129">**DLL**</span></span> | <span data-ttu-id="d5b19-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="d5b19-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5b19-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5b19-131">See also</span></span>

* [<span data-ttu-id="d5b19-132">RoFailFastWithErrorContext fonction)</span><span class="sxs-lookup"><span data-stu-id="d5b19-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)