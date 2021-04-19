---
description: GetOwnerSid&\# 8194 ; La méthode de classe WMI récupère l’identificateur de sécurité (SID) pour le propriétaire de ce processus.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Méthode GetOwnerSid de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544202"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="07384-103">Méthode GetOwnerSid de la \_ classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="07384-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="07384-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** récupère l’identificateur de sécurité (SID) pour le propriétaire de ce processus.</span><span class="sxs-lookup"><span data-stu-id="07384-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="07384-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="07384-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07384-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07384-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07384-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07384-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="07384-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07384-109">*Sid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="07384-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07384-110">Retourne le descripteur d’identificateur de sécurité pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="07384-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07384-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07384-111">Return value</span></span>

<span data-ttu-id="07384-112">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="07384-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="07384-113">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="07384-113">Any other number indicates an error.</span></span> <span data-ttu-id="07384-114">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="07384-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="07384-115">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="07384-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="07384-116">**Achèvement réussi** (0)</span><span class="sxs-lookup"><span data-stu-id="07384-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07384-117">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="07384-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="07384-118">**Privilèges insuffisants** (3)</span><span class="sxs-lookup"><span data-stu-id="07384-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="07384-119">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="07384-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="07384-120">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="07384-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="07384-121">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="07384-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="07384-122">**Autre** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="07384-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="07384-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="07384-123">Examples</span></span>

<span data-ttu-id="07384-124">L’exemple de code de [recherche des utilisateurs connectés sur un système distant/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell interroge les ordinateurs distants pour voir qui est connecté.</span><span class="sxs-lookup"><span data-stu-id="07384-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="07384-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07384-125">Requirements</span></span>



| <span data-ttu-id="07384-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07384-126">Requirement</span></span> | <span data-ttu-id="07384-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="07384-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07384-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07384-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07384-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07384-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07384-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07384-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07384-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07384-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07384-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="07384-132">Namespace</span></span><br/>                | <span data-ttu-id="07384-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="07384-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07384-134">MOF</span><span class="sxs-lookup"><span data-stu-id="07384-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07384-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07384-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07384-136">DLL</span><span class="sxs-lookup"><span data-stu-id="07384-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07384-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07384-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07384-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07384-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="07384-139">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07384-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="07384-140">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="07384-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

