---
description: La fonction LoadIPAddresses est appelée par l’analyse pour remplir une liste d’adresses IP avec les adresses tirées d’une variable de chaîne de configuration HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: LoadIPAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535078"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="40d2a-103">LoadIPAddresses fonction)</span><span class="sxs-lookup"><span data-stu-id="40d2a-103">LoadIPAddresses function</span></span>

<span data-ttu-id="40d2a-104">La fonction **LoadIPAddresses** est appelée par l’analyse pour remplir une liste d’adresses IP avec les adresses tirées d’une variable de chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="40d2a-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40d2a-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="40d2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40d2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d2a-107">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d2a-108">Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="40d2a-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="40d2a-109">*pVarName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d2a-110">Pointeur vers le nom de la variable dans la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="40d2a-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="40d2a-111">*ppAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40d2a-112">Pointeur vers un pointeur vers un tableau d’adresses.</span><span class="sxs-lookup"><span data-stu-id="40d2a-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="40d2a-113">Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, la fonction alloue suffisamment d’espace et stocke toutes les adresses IP sous la forme d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="40d2a-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="40d2a-114">*pNumAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40d2a-115">Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses IP prises à partir de la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="40d2a-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d2a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40d2a-116">Return value</span></span>

<span data-ttu-id="40d2a-117">Si la fonction réussit (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représentait des adresses IP), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="40d2a-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="40d2a-118">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="40d2a-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d2a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="40d2a-119">Remarks</span></span>

<span data-ttu-id="40d2a-120">Les adresses IP doivent être au format x. x. x (par exemple, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="40d2a-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="40d2a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40d2a-121">Requirements</span></span>



| <span data-ttu-id="40d2a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40d2a-122">Requirement</span></span> | <span data-ttu-id="40d2a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d2a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40d2a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40d2a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40d2a-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="40d2a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40d2a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40d2a-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40d2a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="40d2a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="40d2a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d2a-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d2a-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="40d2a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40d2a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="40d2a-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40d2a-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="40d2a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="40d2a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d2a-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d2a-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




