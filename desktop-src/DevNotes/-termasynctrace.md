---
description: Met fin à la trace.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: TermAsyncTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526618"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="eb4ac-103">TermAsyncTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="eb4ac-103">TermAsyncTrace function</span></span>

<span data-ttu-id="eb4ac-104">Met fin à la trace.</span><span class="sxs-lookup"><span data-stu-id="eb4ac-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb4ac-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="eb4ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb4ac-106">Parameters</span></span>

<span data-ttu-id="eb4ac-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eb4ac-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb4ac-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb4ac-108">Return value</span></span>

<span data-ttu-id="eb4ac-109">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="eb4ac-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4ac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="eb4ac-110">Remarks</span></span>

<span data-ttu-id="eb4ac-111">Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="eb4ac-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="eb4ac-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="eb4ac-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4ac-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb4ac-113">Requirements</span></span>



| <span data-ttu-id="eb4ac-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb4ac-114">Requirement</span></span> | <span data-ttu-id="eb4ac-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb4ac-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4ac-116">DLL</span><span class="sxs-lookup"><span data-stu-id="eb4ac-116">DLL</span></span><br/> | <dl> <span data-ttu-id="eb4ac-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4ac-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
