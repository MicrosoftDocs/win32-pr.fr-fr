---
description: La fonction LoadIPXAddresses est appelée par l’analyse pour remplir une liste d’adresses IPX tirée d’une variable de chaîne de configuration HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: LoadIPXAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210046"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="18f1e-103">LoadIPXAddresses fonction)</span><span class="sxs-lookup"><span data-stu-id="18f1e-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="18f1e-104">La fonction **LoadIPXAddresses** est appelée par l’analyse pour remplir une liste d’adresses IPX tirée d’une variable de chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="18f1e-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18f1e-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="18f1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f1e-107">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-108">Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="18f1e-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="18f1e-109">*pVarName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-110">Pointeur vers le nom de la variable dans la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="18f1e-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="18f1e-111">*ppAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-112">Pointeur vers un pointeur vers un tableau d’adresses.</span><span class="sxs-lookup"><span data-stu-id="18f1e-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="18f1e-113">Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, un espace suffisant est alloué (à l’aide de **HeapAllocMemory**), et toutes les adresses IPX sont stockées sous la forme d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="18f1e-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="18f1e-114">*pNumAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-115">Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses IPX prises à partir de la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="18f1e-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f1e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18f1e-116">Return value</span></span>

<span data-ttu-id="18f1e-117">Si la fonction réussit (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représente des adresses IPX), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="18f1e-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="18f1e-118">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="18f1e-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f1e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18f1e-119">Requirements</span></span>



| <span data-ttu-id="18f1e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18f1e-120">Requirement</span></span> | <span data-ttu-id="18f1e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f1e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18f1e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18f1e-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="18f1e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18f1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18f1e-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18f1e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="18f1e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f1e-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="18f1e-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="18f1e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18f1e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="18f1e-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18f1e-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="18f1e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="18f1e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18f1e-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f1e-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




