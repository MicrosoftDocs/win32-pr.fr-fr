---
description: La méthode StartService place le service dans l’état Démarré.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Méthode StartService de la classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514350"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="1f1a0-103">Méthode StartService de la \_ classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="1f1a0-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="1f1a0-104">La méthode **StartService** place le service dans l’état Démarré.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="1f1a0-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1f1a0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1f1a0-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1f1a0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1a0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f1a0-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="1f1a0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f1a0-108">Parameters</span></span>

<span data-ttu-id="1f1a0-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f1a0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f1a0-110">Return value</span></span>

<span data-ttu-id="1f1a0-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="1f1a0-112">Pour obtenir des valeurs différentes de celles répertoriées dans la liste suivante, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="1f1a0-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="1f1a0-113">**0**</span><span class="sxs-lookup"><span data-stu-id="1f1a0-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1f1a0-114">Le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="1f1a0-115">**1**</span><span class="sxs-lookup"><span data-stu-id="1f1a0-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1f1a0-116">Demande non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f1a0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f1a0-117">Requirements</span></span>



| <span data-ttu-id="1f1a0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f1a0-118">Requirement</span></span> | <span data-ttu-id="1f1a0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f1a0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1a0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f1a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1a0-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f1a0-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1f1a0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f1a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1a0-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f1a0-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1f1a0-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f1a0-124">Namespace</span></span><br/>                | <span data-ttu-id="1f1a0-125">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1f1a0-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1f1a0-126">MOF</span><span class="sxs-lookup"><span data-stu-id="1f1a0-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f1a0-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f1a0-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f1a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1a0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f1a0-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1a0-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1f1a0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f1a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1a0-131">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="1f1a0-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1f1a0-132">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="1f1a0-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

