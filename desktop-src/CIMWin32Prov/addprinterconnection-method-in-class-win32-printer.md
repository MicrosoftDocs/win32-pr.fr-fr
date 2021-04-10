---
description: Fournit une connexion à une imprimante existante sur le réseau et l’ajoute à la liste des imprimantes disponibles.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Méthode AddPrinterConnection de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860773"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="18d1e-103">Méthode AddPrinterConnection de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="18d1e-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="18d1e-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** fournit une connexion à une imprimante existante sur le réseau et l’ajoute à la liste des imprimantes disponibles.</span><span class="sxs-lookup"><span data-stu-id="18d1e-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="18d1e-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="18d1e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="18d1e-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="18d1e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="18d1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18d1e-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="18d1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18d1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d1e-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18d1e-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1e-110">Nom convivial de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="18d1e-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d1e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18d1e-111">Return value</span></span>

<span data-ttu-id="18d1e-112">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="18d1e-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="18d1e-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="18d1e-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="18d1e-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="18d1e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="18d1e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="18d1e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="18d1e-116">Succès</span><span class="sxs-lookup"><span data-stu-id="18d1e-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="18d1e-117">**5**</span><span class="sxs-lookup"><span data-stu-id="18d1e-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="18d1e-118">accès refusé</span><span class="sxs-lookup"><span data-stu-id="18d1e-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="18d1e-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="18d1e-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="18d1e-120">Nom d’imprimante non valide</span><span class="sxs-lookup"><span data-stu-id="18d1e-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="18d1e-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="18d1e-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="18d1e-122">Pilote d’imprimante incompatible</span><span class="sxs-lookup"><span data-stu-id="18d1e-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="18d1e-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="18d1e-123">Examples</span></span>

<span data-ttu-id="18d1e-124">L’exemple de code PowerShell [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) installe tous les pilotes d’imprimante à partir d’un serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="18d1e-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="18d1e-125">L’exemple [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell répertorie les imprimantes partagées sur un ordinateur distant et vous donne la possibilité d’ajouter une connexion d’imprimante entre l’ordinateur distant et votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="18d1e-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="18d1e-126">L’exemple de code VBScript suivant ajoute une imprimante locale.</span><span class="sxs-lookup"><span data-stu-id="18d1e-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="18d1e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d1e-127">Requirements</span></span>



| <span data-ttu-id="18d1e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d1e-128">Requirement</span></span> | <span data-ttu-id="18d1e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d1e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d1e-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d1e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="18d1e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18d1e-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="18d1e-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d1e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="18d1e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18d1e-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="18d1e-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18d1e-134">Namespace</span></span><br/>                | <span data-ttu-id="18d1e-135">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="18d1e-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="18d1e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="18d1e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18d1e-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18d1e-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="18d1e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="18d1e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d1e-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d1e-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="18d1e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d1e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d1e-141">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="18d1e-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="18d1e-142">Tâches WMI : imprimantes et impression</span><span class="sxs-lookup"><span data-stu-id="18d1e-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="18d1e-143">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="18d1e-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

