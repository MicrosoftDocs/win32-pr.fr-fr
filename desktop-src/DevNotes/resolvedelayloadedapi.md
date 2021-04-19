---
description: Localise la fonction cible de l’importation spécifiée et remplace le pointeur de fonction dans le thunk d’importation par la cible de l’implémentation de fonction.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532682"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="e2b13-103">ResolveDelayLoadedAPI fonction)</span><span class="sxs-lookup"><span data-stu-id="e2b13-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="e2b13-104">Localise la fonction cible de l’importation spécifiée et remplace le pointeur de fonction dans le thunk d’importation par la cible de l’implémentation de fonction.</span><span class="sxs-lookup"><span data-stu-id="e2b13-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2b13-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e2b13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2b13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b13-107">*ParentModuleBase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2b13-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b13-108">Adresse de la base du module qui importe une fonction à chargement différé.</span><span class="sxs-lookup"><span data-stu-id="e2b13-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="e2b13-109">*DelayloadDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2b13-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b13-110">Descripteur du module à charger.</span><span class="sxs-lookup"><span data-stu-id="e2b13-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e2b13-111">*FailureDllHook* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e2b13-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b13-112">Adresse du raccordement de l’échec.</span><span class="sxs-lookup"><span data-stu-id="e2b13-112">The address of the failure hook.</span></span> <span data-ttu-id="e2b13-113">Consultez [**DelayLoadFailureHook**](delayloadfailurehook.md).</span><span class="sxs-lookup"><span data-stu-id="e2b13-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2b13-114">*FailureSystemHook* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e2b13-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b13-115">Adresse du hook d’échec système.</span><span class="sxs-lookup"><span data-stu-id="e2b13-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="e2b13-116">*ThunkAddress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e2b13-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b13-117">Données de thunk pour la fonction cible.</span><span class="sxs-lookup"><span data-stu-id="e2b13-117">The thunk data for the target function.</span></span> <span data-ttu-id="e2b13-118">Utilisé pour Rechercher l’entrée de table de noms spécifique de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e2b13-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="e2b13-119">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="e2b13-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b13-120">Réservé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e2b13-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b13-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2b13-121">Return value</span></span>

<span data-ttu-id="e2b13-122">Adresse de l’importation, ou stub d’échec pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e2b13-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b13-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2b13-123">Requirements</span></span>



| <span data-ttu-id="e2b13-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2b13-124">Requirement</span></span> | <span data-ttu-id="e2b13-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2b13-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b13-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2b13-126">Library</span></span><br/> | <dl> <span data-ttu-id="e2b13-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2b13-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e2b13-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b13-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2b13-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2b13-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b13-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2b13-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2b13-131">[Prise en charge de l’éditeur de liens pour les dll Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="e2b13-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




