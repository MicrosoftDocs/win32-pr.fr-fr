---
description: La fonction LoadTCHAR est appelée par les analyses pour définir une variable de chaîne sur une chaîne tirée d’une chaîne de configuration HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: LoadTCHAR, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543091"
---
# <a name="loadtchar-function"></a><span data-ttu-id="fde63-103">LoadTCHAR fonction)</span><span class="sxs-lookup"><span data-stu-id="fde63-103">LoadTCHAR function</span></span>

<span data-ttu-id="fde63-104">La fonction **LoadTCHAR** est appelée par les analyses pour définir une variable de chaîne sur une chaîne tirée d’une chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="fde63-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fde63-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="fde63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fde63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde63-107">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde63-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde63-108">Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="fde63-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fde63-109">*pVarName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde63-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde63-110">Pointeur vers le nom de la variable dans la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="fde63-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="fde63-111">*ppszString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fde63-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fde63-112">Pointeur vers un pointeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fde63-112">Pointer to a string pointer.</span></span> <span data-ttu-id="fde63-113">Si le nom de la variable demandée est trouvé, la chaîne est allouée et assignée à ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="fde63-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="fde63-114">L’utilisateur est responsable de libérer la mémoire associée à la chaîne.</span><span class="sxs-lookup"><span data-stu-id="fde63-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde63-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fde63-115">Return value</span></span>

<span data-ttu-id="fde63-116">Si la fonction réussit (si le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="fde63-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="fde63-117">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="fde63-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde63-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fde63-118">Requirements</span></span>



| <span data-ttu-id="fde63-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fde63-119">Requirement</span></span> | <span data-ttu-id="fde63-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fde63-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fde63-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde63-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fde63-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fde63-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fde63-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde63-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fde63-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fde63-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fde63-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fde63-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde63-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde63-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fde63-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fde63-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="fde63-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fde63-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fde63-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fde63-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde63-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde63-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




