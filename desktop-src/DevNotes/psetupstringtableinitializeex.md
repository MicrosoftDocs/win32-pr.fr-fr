---
description: Initialise une table de chaînes.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532942"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="a4b09-103">pSetupStringTableInitializeEx fonction)</span><span class="sxs-lookup"><span data-stu-id="a4b09-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="a4b09-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="a4b09-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="a4b09-105">Initialise une table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="a4b09-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b09-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b09-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="a4b09-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b09-108">*ExtraDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4b09-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b09-109">Taille de l’objet de données supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a4b09-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="a4b09-110">*Réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4b09-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b09-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a4b09-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4b09-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b09-112">Remarks</span></span>

<span data-ttu-id="a4b09-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a4b09-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b09-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b09-114">Requirements</span></span>



| <span data-ttu-id="a4b09-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4b09-115">Requirement</span></span> | <span data-ttu-id="a4b09-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4b09-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b09-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b09-117">DLL</span></span><br/> | <dl> <span data-ttu-id="a4b09-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b09-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
