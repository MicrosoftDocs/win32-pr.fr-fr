---
description: Initialise une table de chaînes.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537959"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="22ea9-103">pSetupStringTableInitialize fonction)</span><span class="sxs-lookup"><span data-stu-id="22ea9-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="22ea9-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="22ea9-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="22ea9-105">Initialise une table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="22ea9-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ea9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22ea9-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="22ea9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22ea9-107">Parameters</span></span>

<span data-ttu-id="22ea9-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="22ea9-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ea9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="22ea9-109">Remarks</span></span>

<span data-ttu-id="22ea9-110">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="22ea9-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ea9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22ea9-111">Requirements</span></span>



| <span data-ttu-id="22ea9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22ea9-112">Requirement</span></span> | <span data-ttu-id="22ea9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="22ea9-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ea9-114">DLL</span><span class="sxs-lookup"><span data-stu-id="22ea9-114">DLL</span></span><br/> | <dl> <span data-ttu-id="22ea9-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ea9-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
