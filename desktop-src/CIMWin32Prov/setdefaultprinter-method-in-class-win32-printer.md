---
description: La méthode de classe WMI SetDefaultPrinter définit l’imprimante système par défaut pour l’utilisateur appelant la méthode.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Méthode SetDefaultPrinter de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861738"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="f9277-103">Méthode SetDefaultPrinter de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="f9277-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="f9277-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** définit l’imprimante système par défaut pour l’utilisateur appelant la méthode.</span><span class="sxs-lookup"><span data-stu-id="f9277-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="f9277-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9277-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9277-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9277-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9277-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9277-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="f9277-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9277-108">Parameters</span></span>

<span data-ttu-id="f9277-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9277-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9277-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9277-110">Return value</span></span>

<span data-ttu-id="f9277-111">Retourne 0 (zéro) en cas de réussite, et une autre valeur si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="f9277-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="f9277-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f9277-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f9277-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f9277-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="f9277-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="f9277-114">Examples</span></span>

<span data-ttu-id="f9277-115">L’exemple d' [installation d’un port imprimante TCP/IP et](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) d’une imprimante VBScript installe un port imprimante TCP/IP, installe une imprimante, puis définit l’imprimante comme étant la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f9277-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="f9277-116">L’exemple de code VBScript suivant définit l’imprimante par défaut sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f9277-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="f9277-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9277-117">Requirements</span></span>



| <span data-ttu-id="f9277-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9277-118">Requirement</span></span> | <span data-ttu-id="f9277-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9277-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9277-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9277-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9277-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9277-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f9277-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9277-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9277-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9277-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f9277-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f9277-124">Namespace</span></span><br/>                | <span data-ttu-id="f9277-125">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f9277-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f9277-126">MOF</span><span class="sxs-lookup"><span data-stu-id="f9277-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9277-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9277-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9277-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f9277-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9277-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9277-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f9277-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9277-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9277-131">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="f9277-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f9277-132">Tâches WMI : imprimantes et impression</span><span class="sxs-lookup"><span data-stu-id="f9277-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="f9277-133">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="f9277-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

