---
description: Renomme une imprimante.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Méthode RenamePrinter de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200863"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="b2638-103">Méthode RenamePrinter de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="b2638-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="b2638-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** renomme une imprimante.</span><span class="sxs-lookup"><span data-stu-id="b2638-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="b2638-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b2638-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b2638-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b2638-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2638-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2638-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="b2638-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2638-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2638-109">*NewPrinterName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2638-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2638-110">Nouveau nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b2638-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2638-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2638-111">Return value</span></span>

<span data-ttu-id="b2638-112">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b2638-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="b2638-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b2638-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b2638-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b2638-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b2638-115">**0**</span><span class="sxs-lookup"><span data-stu-id="b2638-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b2638-116">Succès</span><span class="sxs-lookup"><span data-stu-id="b2638-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="b2638-117">**5**</span><span class="sxs-lookup"><span data-stu-id="b2638-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b2638-118">accès refusé</span><span class="sxs-lookup"><span data-stu-id="b2638-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="b2638-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="b2638-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="b2638-120">Nom d’imprimante non valide</span><span class="sxs-lookup"><span data-stu-id="b2638-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b2638-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="b2638-121">Examples</span></span>

<span data-ttu-id="b2638-122">L’exemple VBScript suivant renomme une imprimante et son nom de partage d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b2638-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b2638-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2638-123">Requirements</span></span>



| <span data-ttu-id="b2638-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2638-124">Requirement</span></span> | <span data-ttu-id="b2638-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2638-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2638-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2638-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2638-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2638-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="b2638-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2638-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2638-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2638-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="b2638-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2638-130">Namespace</span></span><br/>                | <span data-ttu-id="b2638-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b2638-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="b2638-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b2638-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2638-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2638-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2638-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b2638-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2638-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2638-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b2638-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2638-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2638-137">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b2638-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b2638-138">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="b2638-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

