---
title: TaskService. Connect, méthode
description: Pour les scripts, se connecte à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Méthode Connect Planificateur de tâches
- Méthode Connect Planificateur de tâches, objet TaskService
- Planificateur de tâches objet TaskService, méthode Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941891"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="b2c04-106">TaskService. Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="b2c04-106">TaskService.Connect method</span></span>

<span data-ttu-id="b2c04-107">Pour les scripts, se connecte à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.</span><span class="sxs-lookup"><span data-stu-id="b2c04-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="b2c04-108">Si le paramètre serverName est vide, cette méthode s’exécute sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b2c04-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="b2c04-109">Si le userId n’est pas spécifié, le jeton actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b2c04-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c04-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2c04-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2c04-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2c04-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c04-112">*nom du serveur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c04-113">Nom de l’ordinateur auquel vous souhaitez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="b2c04-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="b2c04-114">Si le paramètre serverName est vide, cette méthode s’exécute sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b2c04-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="b2c04-115">*utilisateur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c04-116">Nom d’utilisateur utilisé lors de la connexion à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b2c04-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="b2c04-117">Si l’utilisateur n’est pas spécifié, le jeton actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b2c04-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="b2c04-118">*domaine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c04-119">Domaine de l’utilisateur spécifié dans le paramètre *User* .</span><span class="sxs-lookup"><span data-stu-id="b2c04-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2c04-120">*mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c04-121">Mot de passe utilisé pour se connecter à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b2c04-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="b2c04-122">Si le nom d’utilisateur et le mot de passe ne sont pas spécifiés, le jeton actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b2c04-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c04-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2c04-123">Return value</span></span>

<span data-ttu-id="b2c04-124">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b2c04-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c04-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b2c04-125">Remarks</span></span>

<span data-ttu-id="b2c04-126">La méthode **TaskService. Connect** doit être appelée avant d’appeler l’une des autres méthodes [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b2c04-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="b2c04-127">Si la méthode Connect échoue, vous pouvez collecter l’identificateur d’erreur pour déterminer la signification de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b2c04-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="b2c04-128">Le tableau suivant répertorie les identificateurs d’erreur et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="b2c04-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2c04-129">Identificateur d’erreur</span><span class="sxs-lookup"><span data-stu-id="b2c04-129">Error Identifier</span></span></th>
<th><span data-ttu-id="b2c04-130">Description</span><span class="sxs-lookup"><span data-stu-id="b2c04-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2c04-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="b2c04-131">0x80070005</span></span></td>
<td><span data-ttu-id="b2c04-132">L’accès est refusé pour la connexion au service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b2c04-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c04-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="b2c04-133">0x80041315</span></span></td>
<td><span data-ttu-id="b2c04-134">Le service Planificateur de tâches n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b2c04-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2c04-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="b2c04-135">0x8007000e</span></span></td>
<td><span data-ttu-id="b2c04-136">L’application ne dispose pas de suffisamment de mémoire pour terminer l’opération ou l' <em>utilisateur</em>, le <em>mot de passe</em>ou le <em>domaine</em> a au moins une valeur null et une valeur non null.</span><span class="sxs-lookup"><span data-stu-id="b2c04-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c04-137">53</span><span class="sxs-lookup"><span data-stu-id="b2c04-137">53</span></span></td>
<td><span data-ttu-id="b2c04-138">Cette erreur est retournée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="b2c04-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="b2c04-139">Le nom d’ordinateur spécifié dans le paramètre <em>ServerName</em> n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="b2c04-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="b2c04-140">Lorsque vous essayez de vous connecter à un ordinateur Windows Server 2003 ou Windows XP, et que l’exception de pare-feu de partage de fichiers et d’imprimantes n’est pas activée sur l’ordinateur distant ou que le service d’accès à distance au registre n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b2c04-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="b2c04-141">Lorsque vous essayez de vous connecter à un ordinateur Windows Vista et que l’exception de pare-feu de gestion des tâches planifiées distantes n’est pas activée pour l’ordinateur distant et que l’exception de pare-feu de partage de fichiers et d’imprimantes est activée ou que le service d’accès à distance au registre n’est pas en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="b2c04-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2c04-142">50</span><span class="sxs-lookup"><span data-stu-id="b2c04-142">50</span></span></td>
<td><span data-ttu-id="b2c04-143">Les paramètres <em>utilisateur</em>, <em>mot de passe</em>ou <em>domaine</em> ne peuvent pas être spécifiés lors de la connexion à un ordinateur Windows XP ou Windows Server 2003 distant à partir d’un ordinateur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2c04-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b2c04-144">Si vous vous connectez à un ordinateur Windows Vista distant à partir de Windows Vista, vous devez autoriser l’exception de pare-feu de gestion des tâches planifiées à distance sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="b2c04-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="b2c04-145">Pour autoriser cette exception, cliquez sur Démarrer, panneau de configuration, sécurité, autoriser un programme via le pare-feu Windows, puis activez la case à cocher gestion des tâches planifiées distantes.</span><span class="sxs-lookup"><span data-stu-id="b2c04-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="b2c04-146">Cliquez ensuite sur le bouton OK dans la boîte de dialogue Paramètres du pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="b2c04-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="b2c04-147">Si vous vous connectez à un ordinateur Windows XP ou Windows Server 2003 distant à partir d’un ordinateur Windows Vista, vous devez autoriser l’exception de pare-feu de partage de fichiers et d’imprimantes sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="b2c04-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="b2c04-148">Pour autoriser cette exception, cliquez sur Démarrer, panneau de configuration, double-cliquez sur pare-feu Windows, sélectionnez l’onglet exceptions, puis sélectionnez l’exception pare-feu de partage de fichiers et d’imprimantes.</span><span class="sxs-lookup"><span data-stu-id="b2c04-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="b2c04-149">Cliquez ensuite sur le bouton OK dans la boîte de dialogue pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="b2c04-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="b2c04-150">Le service d’accès à distance au registre doit également être en cours d’exécution sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="b2c04-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c04-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2c04-151">Requirements</span></span>



| <span data-ttu-id="b2c04-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2c04-152">Requirement</span></span> | <span data-ttu-id="b2c04-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2c04-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c04-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c04-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c04-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2c04-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c04-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c04-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2c04-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2c04-158">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b2c04-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2c04-159"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2c04-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2c04-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b2c04-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2c04-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2c04-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





