---
description: Transfère le travail en résolvant les importations à chargement différé à partir du fichier binaire parent vers un fichier binaire cible.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540060"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="12c33-103">ResolveDelayLoadsFromDll fonction)</span><span class="sxs-lookup"><span data-stu-id="12c33-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="12c33-104">Transfère le travail en résolvant les importations à chargement différé à partir du fichier binaire parent vers un fichier binaire cible.</span><span class="sxs-lookup"><span data-stu-id="12c33-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12c33-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="12c33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c33-107">*ParentBase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12c33-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c33-108">Adresse de base du module qui retarde le chargement d’un autre binaire.</span><span class="sxs-lookup"><span data-stu-id="12c33-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="12c33-109">*TargetDllName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12c33-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c33-110">Nom de la DLL cible.</span><span class="sxs-lookup"><span data-stu-id="12c33-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="12c33-111">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="12c33-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="12c33-112">Réservé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="12c33-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c33-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12c33-113">Return value</span></span>

<span data-ttu-id="12c33-114">Adresse du descripteur de chargement différé, s’il est trouvé ; Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="12c33-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c33-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12c33-115">Requirements</span></span>



| <span data-ttu-id="12c33-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12c33-116">Requirement</span></span> | <span data-ttu-id="12c33-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="12c33-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c33-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12c33-118">Library</span></span><br/> | <dl> <span data-ttu-id="12c33-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="12c33-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="12c33-120">DLL</span><span class="sxs-lookup"><span data-stu-id="12c33-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="12c33-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c33-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c33-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12c33-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="12c33-123">[Prise en charge de l’éditeur de liens pour les dll Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="12c33-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




