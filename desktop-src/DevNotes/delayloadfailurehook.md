---
description: Retourne l’adresse d’une fonction de rappel d’échec de chargement différé pour la DLL et le processus spécifiés.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533041"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="0e952-103">DelayLoadFailureHook fonction)</span><span class="sxs-lookup"><span data-stu-id="0e952-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="0e952-104">Retourne l’adresse d’une fonction de rappel d’échec de chargement différé pour la DLL et le processus spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0e952-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e952-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e952-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="0e952-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e952-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e952-107">*pszDllName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e952-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e952-108">Nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="0e952-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="0e952-109">*pszProcName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e952-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e952-110">Nom du processus.</span><span class="sxs-lookup"><span data-stu-id="0e952-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e952-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e952-111">Return value</span></span>

<span data-ttu-id="0e952-112">Adresse de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="0e952-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e952-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e952-113">Requirements</span></span>



| <span data-ttu-id="0e952-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e952-114">Requirement</span></span> | <span data-ttu-id="0e952-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e952-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e952-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e952-116">Library</span></span><br/> | <dl> <span data-ttu-id="0e952-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e952-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e952-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0e952-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e952-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e952-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e952-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e952-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e952-121">[Raccordements de défaillance](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="0e952-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




