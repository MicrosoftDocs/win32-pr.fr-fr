---
description: Tente d’envoyer un code de contrôle défini par l’utilisateur à un service géré par un pilote système.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Méthode UserControlService de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950797"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="78e8b-103">Méthode UserControlService de la \_ classe Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="78e8b-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="78e8b-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tente d’envoyer un code de contrôle défini par l’utilisateur à un service géré par un pilote système.</span><span class="sxs-lookup"><span data-stu-id="78e8b-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="78e8b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="78e8b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="78e8b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="78e8b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="78e8b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78e8b-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="78e8b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78e8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e8b-109">*ControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78e8b-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78e8b-110">Spécifie des valeurs définies (de 128 à 255) qui fournissent des commandes de contrôle spécifiques à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78e8b-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e8b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78e8b-111">Return value</span></span>

<span data-ttu-id="78e8b-112">Retourne la valeur 0 (zéro) si la demande **UserControlService** a été acceptée, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="78e8b-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e8b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78e8b-113">Requirements</span></span>



| <span data-ttu-id="78e8b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78e8b-114">Requirement</span></span> | <span data-ttu-id="78e8b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="78e8b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78e8b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e8b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78e8b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78e8b-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78e8b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e8b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78e8b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78e8b-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78e8b-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="78e8b-120">Namespace</span></span><br/>                | <span data-ttu-id="78e8b-121">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="78e8b-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78e8b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="78e8b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78e8b-123"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78e8b-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78e8b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="78e8b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e8b-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e8b-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78e8b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78e8b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="78e8b-127">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78e8b-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="78e8b-128">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="78e8b-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

