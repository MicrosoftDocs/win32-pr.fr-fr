---
description: Imprime une page de test.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Méthode PrintTestPage de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513159"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="457f8-103">Méthode PrintTestPage de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="457f8-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="457f8-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PrintTestPage** imprime une page de test.</span><span class="sxs-lookup"><span data-stu-id="457f8-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="457f8-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="457f8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="457f8-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="457f8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="457f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="457f8-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="457f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="457f8-108">Parameters</span></span>

<span data-ttu-id="457f8-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="457f8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="457f8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="457f8-110">Return value</span></span>

<span data-ttu-id="457f8-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="457f8-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="457f8-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="457f8-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="457f8-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="457f8-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="457f8-114">**0**</span><span class="sxs-lookup"><span data-stu-id="457f8-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="457f8-115">Succès</span><span class="sxs-lookup"><span data-stu-id="457f8-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="457f8-116">**5**</span><span class="sxs-lookup"><span data-stu-id="457f8-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="457f8-117">accès refusé</span><span class="sxs-lookup"><span data-stu-id="457f8-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="457f8-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="457f8-118">Examples</span></span>

<span data-ttu-id="457f8-119">L’exemple de code PowerShell suivant imprime une page de test.</span><span class="sxs-lookup"><span data-stu-id="457f8-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="457f8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="457f8-120">Requirements</span></span>



| <span data-ttu-id="457f8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="457f8-121">Requirement</span></span> | <span data-ttu-id="457f8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="457f8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="457f8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="457f8-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="457f8-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="457f8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="457f8-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="457f8-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="457f8-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="457f8-127">Namespace</span></span><br/>                | <span data-ttu-id="457f8-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="457f8-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="457f8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="457f8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="457f8-130"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="457f8-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="457f8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="457f8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="457f8-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="457f8-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="457f8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="457f8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457f8-134">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="457f8-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="457f8-135">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="457f8-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

