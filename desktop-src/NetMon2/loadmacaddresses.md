---
description: La fonction LoadMACAddresses est appelée par l’analyse pour remplir une liste d’adresses MAC avec les adresses tirées d’une variable de chaîne de configuration HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: LoadMACAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526769"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="f68f5-103">LoadMACAddresses fonction)</span><span class="sxs-lookup"><span data-stu-id="f68f5-103">LoadMACAddresses function</span></span>

<span data-ttu-id="f68f5-104">La fonction **LoadMACAddresses** est appelée par l’analyse pour remplir une liste d’adresses Mac avec les adresses tirées d’une variable de chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="f68f5-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f68f5-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="f68f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f68f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68f5-107">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68f5-108">Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="f68f5-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f68f5-109">*pVarName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68f5-110">Pointeur vers le nom de la variable dans la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="f68f5-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="f68f5-111">*ppAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68f5-112">Pointeur vers un pointeur vers un tableau d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f68f5-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="f68f5-113">Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, la fonction alloue suffisamment d’espace (à l’aide de **HeapAllocMemory**) et stocke toutes les adresses Mac sous la forme d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="f68f5-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="f68f5-114">*pNumAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68f5-115">Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses Mac prises à partir de la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="f68f5-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68f5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f68f5-116">Return value</span></span>

<span data-ttu-id="f68f5-117">Si la fonction réussit, (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représentait des adresses MAC), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="f68f5-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="f68f5-118">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="f68f5-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f68f5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f68f5-119">Requirements</span></span>



| <span data-ttu-id="f68f5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f68f5-120">Requirement</span></span> | <span data-ttu-id="f68f5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f68f5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f68f5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f68f5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f68f5-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f68f5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f68f5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f68f5-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f68f5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f68f5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f68f5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f68f5-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f68f5-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f68f5-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f68f5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f68f5-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f68f5-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f68f5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f68f5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f68f5-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f68f5-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




