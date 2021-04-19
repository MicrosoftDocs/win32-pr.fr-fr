---
description: Détermine si le Terminal Server est en mode d’installation.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525357"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="71ae5-103">TermsrvAppInstallMode fonction)</span><span class="sxs-lookup"><span data-stu-id="71ae5-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="71ae5-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="71ae5-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="71ae5-105">Elle peut changer ou disparaître complètement sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="71ae5-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="71ae5-106">Détermine si le Terminal Server est en mode d’installation.</span><span class="sxs-lookup"><span data-stu-id="71ae5-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ae5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71ae5-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="71ae5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71ae5-108">Parameters</span></span>

<span data-ttu-id="71ae5-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="71ae5-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71ae5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71ae5-110">Return value</span></span>

<span data-ttu-id="71ae5-111">Cette fonction renvoie la **valeur true** si le Terminal Server est en mode d’installation et **false** s’il est en mode exécution.</span><span class="sxs-lookup"><span data-stu-id="71ae5-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ae5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71ae5-112">Requirements</span></span>



| <span data-ttu-id="71ae5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71ae5-113">Requirement</span></span> | <span data-ttu-id="71ae5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="71ae5-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ae5-115">DLL</span><span class="sxs-lookup"><span data-stu-id="71ae5-115">DLL</span></span><br/> | <dl> <span data-ttu-id="71ae5-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ae5-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




