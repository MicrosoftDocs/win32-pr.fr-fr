---
description: Pause la file d'attente à l'impression.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Méthode pause de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393203"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="bd3e6-103">Méthode pause de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="bd3e6-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="bd3e6-104">La méthode de classe **interrompre** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) interrompt la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="bd3e6-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="bd3e6-105">Aucun travail ne peut être imprimé tant que la file d’attente n’a pas repris.</span><span class="sxs-lookup"><span data-stu-id="bd3e6-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="bd3e6-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="bd3e6-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bd3e6-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bd3e6-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd3e6-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="bd3e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd3e6-109">Parameters</span></span>

<span data-ttu-id="bd3e6-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd3e6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd3e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd3e6-111">Return value</span></span>

<span data-ttu-id="bd3e6-112">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="bd3e6-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="bd3e6-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bd3e6-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bd3e6-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bd3e6-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bd3e6-115">**0**</span><span class="sxs-lookup"><span data-stu-id="bd3e6-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bd3e6-116">Succès</span><span class="sxs-lookup"><span data-stu-id="bd3e6-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="bd3e6-117">**5**</span><span class="sxs-lookup"><span data-stu-id="bd3e6-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="bd3e6-118">accès refusé</span><span class="sxs-lookup"><span data-stu-id="bd3e6-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd3e6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd3e6-119">Requirements</span></span>



| <span data-ttu-id="bd3e6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd3e6-120">Requirement</span></span> | <span data-ttu-id="bd3e6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd3e6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3e6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd3e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3e6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd3e6-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bd3e6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd3e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3e6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd3e6-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bd3e6-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bd3e6-126">Namespace</span></span><br/>                | <span data-ttu-id="bd3e6-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bd3e6-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="bd3e6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bd3e6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd3e6-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd3e6-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd3e6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bd3e6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd3e6-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd3e6-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bd3e6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd3e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3e6-133">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="bd3e6-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="bd3e6-134">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="bd3e6-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="bd3e6-135">**Resume, méthode**</span><span class="sxs-lookup"><span data-stu-id="bd3e6-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

