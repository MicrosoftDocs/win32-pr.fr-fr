---
description: Place le service représenté par l' \_ objet Win32 PrinterDriver dans l’état arrêté.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Méthode StopService de la classe Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033693"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="9faa2-103">Méthode StopService de la \_ classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="9faa2-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="9faa2-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** place le service représenté par l’objet [**Win32 \_ PrinterDriver**](win32-printerdriver.md) à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="9faa2-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="9faa2-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9faa2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9faa2-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9faa2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9faa2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9faa2-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="9faa2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9faa2-108">Parameters</span></span>

<span data-ttu-id="9faa2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9faa2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9faa2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9faa2-110">Return value</span></span>

<span data-ttu-id="9faa2-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="9faa2-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="9faa2-112">Pour obtenir des valeurs différentes de celles répertoriées dans la liste suivante, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="9faa2-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="9faa2-113">**0**</span><span class="sxs-lookup"><span data-stu-id="9faa2-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9faa2-114">Le service s’est arrêté correctement.</span><span class="sxs-lookup"><span data-stu-id="9faa2-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="9faa2-115">**1**</span><span class="sxs-lookup"><span data-stu-id="9faa2-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9faa2-116">Demande non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9faa2-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9faa2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9faa2-117">Requirements</span></span>



| <span data-ttu-id="9faa2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9faa2-118">Requirement</span></span> | <span data-ttu-id="9faa2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9faa2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9faa2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9faa2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9faa2-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9faa2-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9faa2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9faa2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9faa2-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9faa2-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9faa2-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9faa2-124">Namespace</span></span><br/>                | <span data-ttu-id="9faa2-125">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9faa2-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="9faa2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9faa2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9faa2-127"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="9faa2-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="9faa2-128">MOF</span><span class="sxs-lookup"><span data-stu-id="9faa2-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9faa2-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9faa2-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="9faa2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9faa2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9faa2-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9faa2-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="9faa2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9faa2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9faa2-133">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="9faa2-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9faa2-134">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="9faa2-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

