---
description: La fonction LoadDWORD est appelée par l’analyse pour définir une variable DWORD avec une valeur extraite d’une variable de chaîne de configuration HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: LoadDWORD, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526315"
---
# <a name="loaddword-function"></a><span data-ttu-id="e6281-103">LoadDWORD fonction)</span><span class="sxs-lookup"><span data-stu-id="e6281-103">LoadDWORD function</span></span>

<span data-ttu-id="e6281-104">La fonction **LoadDWORD** est appelée par l’analyse pour définir une variable **DWORD** avec une valeur extraite d’une variable de chaîne de configuration html.</span><span class="sxs-lookup"><span data-stu-id="e6281-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6281-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6281-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e6281-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6281-107">*pConfig* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6281-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6281-108">Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="e6281-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e6281-109">*pVarName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6281-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6281-110">Pointeur vers le nom de la variable dans la chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6281-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="e6281-111">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6281-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6281-112">Pointeur vers la variable **DWORD** qui est définie sur la valeur de la variable de chaîne de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6281-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6281-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6281-113">Return value</span></span>

<span data-ttu-id="e6281-114">Si la fonction réussit (si le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro), la valeur **DWORD** est insérée et la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="e6281-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="e6281-115">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="e6281-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6281-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6281-116">Requirements</span></span>



| <span data-ttu-id="e6281-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6281-117">Requirement</span></span> | <span data-ttu-id="e6281-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6281-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6281-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6281-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6281-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6281-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e6281-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6281-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6281-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6281-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e6281-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6281-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6281-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6281-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e6281-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6281-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6281-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6281-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6281-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e6281-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6281-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6281-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




