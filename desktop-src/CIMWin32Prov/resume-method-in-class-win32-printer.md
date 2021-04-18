---
description: Reprend une file d’attente à l’impression en pause.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Méthode Resume de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519209"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="a11cd-103">Méthode Resume de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="a11cd-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="a11cd-104">La méthode de **reprise** de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) reprend une file d’attente à l’impression en pause.</span><span class="sxs-lookup"><span data-stu-id="a11cd-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="a11cd-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a11cd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a11cd-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a11cd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a11cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a11cd-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="a11cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a11cd-108">Parameters</span></span>

<span data-ttu-id="a11cd-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a11cd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a11cd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a11cd-110">Return value</span></span>

<span data-ttu-id="a11cd-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a11cd-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a11cd-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a11cd-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a11cd-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a11cd-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a11cd-114">**0**</span><span class="sxs-lookup"><span data-stu-id="a11cd-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a11cd-115">Succès</span><span class="sxs-lookup"><span data-stu-id="a11cd-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="a11cd-116">**5**</span><span class="sxs-lookup"><span data-stu-id="a11cd-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a11cd-117">accès refusé</span><span class="sxs-lookup"><span data-stu-id="a11cd-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a11cd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a11cd-118">Requirements</span></span>



| <span data-ttu-id="a11cd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a11cd-119">Requirement</span></span> | <span data-ttu-id="a11cd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a11cd-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11cd-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a11cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a11cd-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a11cd-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a11cd-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a11cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a11cd-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a11cd-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a11cd-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a11cd-125">Namespace</span></span><br/>                | <span data-ttu-id="a11cd-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a11cd-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a11cd-127">MOF</span><span class="sxs-lookup"><span data-stu-id="a11cd-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a11cd-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a11cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a11cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a11cd-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a11cd-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a11cd-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a11cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11cd-132">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="a11cd-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a11cd-133">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="a11cd-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="a11cd-134">**Pause, méthode**</span><span class="sxs-lookup"><span data-stu-id="a11cd-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

