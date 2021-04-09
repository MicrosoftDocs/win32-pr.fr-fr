---
description: Démarre le débogueur actuellement inscrit pour ce processus.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Méthode AttachDebugger de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860769"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="3978d-103">Méthode AttachDebugger de la \_ classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="3978d-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="3978d-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** démarre le débogueur actuellement inscrit pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="3978d-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="3978d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3978d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3978d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3978d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3978d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3978d-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="3978d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3978d-108">Parameters</span></span>

<span data-ttu-id="3978d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3978d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3978d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3978d-110">Return value</span></span>

<span data-ttu-id="3978d-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3978d-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="3978d-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3978d-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3978d-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3978d-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3978d-114">**Opération réussie**</span><span class="sxs-lookup"><span data-stu-id="3978d-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-115">0</span><span class="sxs-lookup"><span data-stu-id="3978d-115">0</span></span>

<span data-ttu-id="3978d-116">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="3978d-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-117">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="3978d-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-118">2</span><span class="sxs-lookup"><span data-stu-id="3978d-118">2</span></span>

<span data-ttu-id="3978d-119">L’utilisateur n’a pas accès aux informations demandées.</span><span class="sxs-lookup"><span data-stu-id="3978d-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-120">**Privilèges insuffisants**</span><span class="sxs-lookup"><span data-stu-id="3978d-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-121">3</span><span class="sxs-lookup"><span data-stu-id="3978d-121">3</span></span>

<span data-ttu-id="3978d-122">L’utilisateur ne dispose pas de privilèges suffisants.</span><span class="sxs-lookup"><span data-stu-id="3978d-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="3978d-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-124">8</span><span class="sxs-lookup"><span data-stu-id="3978d-124">8</span></span>

<span data-ttu-id="3978d-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="3978d-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-126">**Chemin d'accès introuvable**</span><span class="sxs-lookup"><span data-stu-id="3978d-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-127">9</span><span class="sxs-lookup"><span data-stu-id="3978d-127">9</span></span>

<span data-ttu-id="3978d-128">Le chemin d'accès spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="3978d-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-129">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="3978d-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-130">21</span><span class="sxs-lookup"><span data-stu-id="3978d-130">21</span></span>

<span data-ttu-id="3978d-131">Le paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3978d-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3978d-132">**Autres**</span><span class="sxs-lookup"><span data-stu-id="3978d-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3978d-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="3978d-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3978d-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3978d-134">Requirements</span></span>



| <span data-ttu-id="3978d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3978d-135">Requirement</span></span> | <span data-ttu-id="3978d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="3978d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3978d-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3978d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3978d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3978d-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3978d-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3978d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3978d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3978d-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3978d-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3978d-141">Namespace</span></span><br/>                | <span data-ttu-id="3978d-142">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3978d-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3978d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="3978d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3978d-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3978d-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3978d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3978d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3978d-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3978d-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3978d-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3978d-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="3978d-148">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3978d-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3978d-149">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="3978d-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

