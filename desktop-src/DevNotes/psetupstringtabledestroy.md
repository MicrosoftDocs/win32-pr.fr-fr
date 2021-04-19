---
description: Supprime une table de chaînes.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527291"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="c240b-103">pSetupStringTableDestroy fonction)</span><span class="sxs-lookup"><span data-stu-id="c240b-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="c240b-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="c240b-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="c240b-105">Supprime une table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c240b-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c240b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c240b-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="c240b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c240b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c240b-108">*STRINGTABLE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c240b-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c240b-109">Pointeur vers la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c240b-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c240b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c240b-110">Return value</span></span>

<span data-ttu-id="c240b-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c240b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c240b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c240b-112">Remarks</span></span>

<span data-ttu-id="c240b-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c240b-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c240b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c240b-114">Requirements</span></span>



| <span data-ttu-id="c240b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c240b-115">Requirement</span></span> | <span data-ttu-id="c240b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c240b-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c240b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c240b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c240b-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c240b-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
