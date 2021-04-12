---
description: Crée un nouveau pilote d’imprimante.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Méthode AddPrinterDriver de la classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392967"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="cf8f6-103">Méthode AddPrinterDriver de la \_ classe Win32 PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="cf8f6-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="cf8f6-104">La méthode de la classe **AddPrinterDriver** crée un nouveau pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="cf8f6-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cf8f6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf8f6-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf8f6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf8f6-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cf8f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf8f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf8f6-109">*DriverInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf8f6-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf8f6-110">Instance de la classe [**\_ PrinterDriver Win32**](win32-printerdriver.md) qui représente le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf8f6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf8f6-111">Return value</span></span>

<span data-ttu-id="cf8f6-112">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="cf8f6-113">Pour obtenir des valeurs différentes de celles répertoriées dans la liste suivante, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="cf8f6-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="cf8f6-114">**0**</span><span class="sxs-lookup"><span data-stu-id="cf8f6-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cf8f6-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cf8f6-116">**5**</span><span class="sxs-lookup"><span data-stu-id="cf8f6-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="cf8f6-117">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cf8f6-118">**87**</span><span class="sxs-lookup"><span data-stu-id="cf8f6-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="cf8f6-119">Le paramètre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-119">The parameter is incorrect.</span></span> <span data-ttu-id="cf8f6-120">Peut se produire lorsque l’objet n’est pas correctement rempli ou lorsque le pilote ne peut pas être trouvé dans le système.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="cf8f6-121">L’attribut Name peut également être différent du modèle spécifié dans le fichier. inf.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="cf8f6-122">Ou il se peut qu’il y ait une barre oblique inverse (« \\ ») manquante sur un attribut PathFile.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="cf8f6-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="cf8f6-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="cf8f6-124">Le pilote d’imprimante est inconnu.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8f6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cf8f6-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf8f6-126">Lorsque vous utilisez la méthode **AddPrinterDriver** , vous devez utiliser **SeLoadDriverPrivilege** pour charger ou décharger un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cf8f6-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="cf8f6-127">Examples</span></span>

<span data-ttu-id="cf8f6-128">L’exemple de code de l'[installation d’un pilote d’imprimante introuvable dans les pilotes CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) en VBScript installe une imprimante hypothétique à l’aide d’un pilote d’impression introuvable dans Drivers.cab.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="cf8f6-129">L’exemple VBScript suivant installe le pilote d’imprimante pour une imprimante Apple LaserWriter 8500.</span><span class="sxs-lookup"><span data-stu-id="cf8f6-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="cf8f6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf8f6-130">Requirements</span></span>



| <span data-ttu-id="cf8f6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf8f6-131">Requirement</span></span> | <span data-ttu-id="cf8f6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf8f6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8f6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf8f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8f6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf8f6-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="cf8f6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf8f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8f6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf8f6-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="cf8f6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf8f6-137">Namespace</span></span><br/>                | <span data-ttu-id="cf8f6-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cf8f6-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="cf8f6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cf8f6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf8f6-140"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf8f6-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf8f6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cf8f6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf8f6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf8f6-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cf8f6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf8f6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8f6-144">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="cf8f6-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cf8f6-145">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="cf8f6-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

