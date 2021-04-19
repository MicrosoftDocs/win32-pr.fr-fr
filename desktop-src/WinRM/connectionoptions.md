---
title: Objet ConnectionOptions (WSManDisp. h)
description: L’objet ConnectionOptions est passé à la méthode CreateSession pour fournir le nom d’utilisateur et le mot de passe associés au compte local sur l’ordinateur distant.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objet ConnectionOptions Windows Remote Management
- Windows Remote Management d’objets ConnectionOptions, Description
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509534"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="fc536-105">Objet ConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="fc536-105">ConnectionOptions object</span></span>

<span data-ttu-id="fc536-106">L’objet **ConnectionOptions** est passé à la méthode [**CreateSession**](wsman-createsession.md) pour fournir le nom d’utilisateur et le mot de passe associés au compte local sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="fc536-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="fc536-107">Si aucun paramètre n’est fourni, les informations d’identification du compte qui exécute le script sont définies sur les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc536-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="fc536-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fc536-108">Members</span></span>

<span data-ttu-id="fc536-109">L’objet **ConnectionOptions** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fc536-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="fc536-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc536-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc536-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc536-111">Properties</span></span>

<span data-ttu-id="fc536-112">L’objet **ConnectionOptions** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc536-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="fc536-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="fc536-113">Property</span></span>                                                  | <span data-ttu-id="fc536-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="fc536-114">Access type</span></span>           | <span data-ttu-id="fc536-115">Description</span><span class="sxs-lookup"><span data-stu-id="fc536-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc536-116">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="fc536-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="fc536-117">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="fc536-117">Write-only</span></span><br/> | <span data-ttu-id="fc536-118">Définit le mot de passe d’un compte local ou de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="fc536-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="fc536-119">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="fc536-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="fc536-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fc536-120">Read/write</span></span><br/> | <span data-ttu-id="fc536-121">Définit et obtient le nom d’utilisateur d’un compte local ou de domaine sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="fc536-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fc536-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fc536-122">Remarks</span></span>

<span data-ttu-id="fc536-123">L’objet **ConnectionOptions** correspond à l’interface [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="fc536-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="fc536-124">Si une application cliente Windows Remote Management s’exécute avec l’emprunt d’identité, un échec se produit si vous définissez la propriété [**de mot de passe**](connectionoptions-password.md) .</span><span class="sxs-lookup"><span data-stu-id="fc536-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="fc536-125">Une application cliente est un script ou tout autre programme qui envoie une demande à WinRM sur l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="fc536-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="fc536-126">L’application cliente peut s’exécuter sous emprunt d’identité, car elle a appelé une fonction telle que [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc536-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="fc536-127">Une page de Active Server (ASP) ou un service ne peut pas demander un nom d’utilisateur et un mot de passe si le processus ASP s’exécute sous un compte qui emprunte l’identité d’un client.</span><span class="sxs-lookup"><span data-stu-id="fc536-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="fc536-128">L’indicateur **WSManFlagCredUserNamePassword** doit être défini sur l’appel de [**WSman. CreateSession**](wsman-createsession.md) lors de l’utilisation du [**nom d’utilisateur**](connectionoptions-username.md) et du [**mot de passe**](connectionoptions-password.md) pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="fc536-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="fc536-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="fc536-129">Examples</span></span>

<span data-ttu-id="fc536-130">L’exemple de code VBScript suivant montre comment créer un objet **ConnectionOptions** , définir les propriétés du compte sur l’ordinateur distant et l’utiliser pour créer un objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="fc536-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="fc536-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc536-131">Requirements</span></span>



| <span data-ttu-id="fc536-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc536-132">Requirement</span></span> | <span data-ttu-id="fc536-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc536-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc536-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc536-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fc536-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc536-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fc536-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc536-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fc536-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc536-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fc536-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc536-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc536-139"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc536-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc536-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="fc536-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc536-141"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc536-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fc536-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc536-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc536-143"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc536-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc536-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fc536-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc536-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc536-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc536-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc536-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc536-147">Authentification des connexions à distance</span><span class="sxs-lookup"><span data-stu-id="fc536-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="fc536-148">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="fc536-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="fc536-149">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="fc536-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc536-150">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="fc536-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc536-151">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="fc536-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="fc536-152">Obtention de données à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="fc536-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="fc536-153">Obtention de données à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="fc536-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

