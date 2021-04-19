---
description: Détermine si le Terminal Server est en mode d’installation (uniquement sur Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526827"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="40aa1-103">CtxGetIniMapping fonction)</span><span class="sxs-lookup"><span data-stu-id="40aa1-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="40aa1-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="40aa1-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="40aa1-105">Elle peut changer ou disparaître complètement sans préavis.</span><span class="sxs-lookup"><span data-stu-id="40aa1-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="40aa1-106">Utilisez plutôt **VerifyVersionInfo**.\]</span><span class="sxs-lookup"><span data-stu-id="40aa1-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="40aa1-107">Détermine si le Terminal Server est en mode d’installation (uniquement sur Windows Terminal Server 4,0).</span><span class="sxs-lookup"><span data-stu-id="40aa1-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="40aa1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40aa1-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="40aa1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40aa1-109">Parameters</span></span>

<span data-ttu-id="40aa1-110">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="40aa1-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40aa1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40aa1-111">Return value</span></span>

<span data-ttu-id="40aa1-112">Cette fonction retourne **false** si le Terminal Server est en mode d’installation, **true** s’il est en mode exécution.</span><span class="sxs-lookup"><span data-stu-id="40aa1-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="40aa1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40aa1-113">Requirements</span></span>



| <span data-ttu-id="40aa1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40aa1-114">Requirement</span></span> | <span data-ttu-id="40aa1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="40aa1-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40aa1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="40aa1-116">DLL</span></span><br/> | <dl> <span data-ttu-id="40aa1-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40aa1-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40aa1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40aa1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40aa1-119">**VerifyVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="40aa1-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
