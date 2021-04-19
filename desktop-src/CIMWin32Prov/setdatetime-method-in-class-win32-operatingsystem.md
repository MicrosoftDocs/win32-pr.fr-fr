---
description: SetDateTime&\# 8194 ; La méthode de classe WMI définit l’heure système actuelle sur l’ordinateur.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Méthode SetDateTime de la classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515145"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="f6165-103">Méthode SetDateTime de la \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f6165-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="f6165-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDateTime** définit l’heure système actuelle sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f6165-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="f6165-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f6165-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6165-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6165-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6165-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6165-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="f6165-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6165-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6165-109">*LocalDatetime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6165-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6165-110">Valeur de l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="f6165-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6165-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6165-111">Return value</span></span>

<span data-ttu-id="f6165-112">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f6165-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="f6165-113">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="f6165-113">Any other number indicates an error.</span></span> <span data-ttu-id="f6165-114">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6165-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6165-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6165-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6165-116">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="f6165-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6165-117">**Autre** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="f6165-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f6165-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f6165-118">Remarks</span></span>

<span data-ttu-id="f6165-119">Le processus appelant doit avoir le \_ privilège se SYSTEMTIME \_ Name.</span><span class="sxs-lookup"><span data-stu-id="f6165-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6165-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6165-120">Requirements</span></span>



| <span data-ttu-id="f6165-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6165-121">Requirement</span></span> | <span data-ttu-id="f6165-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6165-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6165-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6165-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6165-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6165-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6165-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6165-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6165-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6165-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6165-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f6165-127">Namespace</span></span><br/>                | <span data-ttu-id="f6165-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f6165-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6165-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f6165-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6165-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6165-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6165-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f6165-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6165-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6165-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6165-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6165-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6165-134">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6165-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6165-135">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="f6165-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="f6165-136">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="f6165-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

