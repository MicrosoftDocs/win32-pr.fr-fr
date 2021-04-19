---
description: Initialise la trace.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542485"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="d8fd2-103">InitAsyncTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="d8fd2-103">InitAsyncTrace function</span></span>

<span data-ttu-id="d8fd2-104">Initialise la trace.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8fd2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8fd2-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="d8fd2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8fd2-106">Parameters</span></span>

<span data-ttu-id="d8fd2-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8fd2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8fd2-108">Return value</span></span>

<span data-ttu-id="d8fd2-109">Cette fonction retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="d8fd2-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fd2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d8fd2-110">Remarks</span></span>

<span data-ttu-id="d8fd2-111">Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="d8fd2-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="d8fd2-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d8fd2-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fd2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8fd2-113">Requirements</span></span>



| <span data-ttu-id="d8fd2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8fd2-114">Requirement</span></span> | <span data-ttu-id="d8fd2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8fd2-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fd2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d8fd2-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d8fd2-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8fd2-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
