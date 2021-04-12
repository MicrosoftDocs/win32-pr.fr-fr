---
title: Méthode ITSRemoteProgram ServerStartProgram
description: Spécifie un programme RemoteApp à démarrer dans la session à distance.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram2
- Services Bureau à distance de l’interface ITSRemoteProgram2, méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, méthode ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508753"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="99117-110">ITSRemoteProgram :: ServerStartProgram, méthode</span><span class="sxs-lookup"><span data-stu-id="99117-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="99117-111">Spécifie un programme RemoteApp à démarrer dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="99117-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="99117-112">Cette fonction doit être appelée dans une session connectée (après la réception de la notification de session connectée au client).</span><span class="sxs-lookup"><span data-stu-id="99117-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="99117-113">Un nombre quelconque de programmes RemoteApp peuvent être démarrés dans une session.</span><span class="sxs-lookup"><span data-stu-id="99117-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="99117-114">Une session RemoteApp expire si aucun programme RemoteApp n’est démarré dans la session dans le délai imparti, soit deux minutes pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="99117-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="99117-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99117-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="99117-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99117-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99117-117">*bstrExecutablePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-118">Chemin d’accès du fichier exécutable du programme RemoteApp sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="99117-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="99117-119">*bstrFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-120">Chemin d’accès d’un fichier à ouvrir sur le serveur par le biais d’une association de fichier, par exemple « C : \\ \\ documents \\ \\MyReport.docx ».</span><span class="sxs-lookup"><span data-stu-id="99117-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="99117-121">Si vous spécifiez *bstrFilePath*, vous ne devez pas spécifier le paramètre *bstrExecutablePath* , et vice versa.</span><span class="sxs-lookup"><span data-stu-id="99117-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="99117-122">Vous devez uniquement spécifier l’un des paramètres.</span><span class="sxs-lookup"><span data-stu-id="99117-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="99117-123">*bstrWorkingDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-124">Répertoire de travail sur le serveur pour le programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="99117-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="99117-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-126">Indique si le serveur doit développer les variables d’environnement dans le chemin d’accès du répertoire de travail.</span><span class="sxs-lookup"><span data-stu-id="99117-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="99117-127">Affectez à ce paramètre la **\_ valeur variant true** si le chemin d’accès du répertoire de travail contient des variables d’environnement ou **\_ false** si le chemin d’accès du répertoire de travail ne contient pas de variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="99117-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="99117-128">*bstrArguments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-129">Arguments de ligne de commande pour le programme RemoteApp spécifiés dans *bstrExecutablePath*.</span><span class="sxs-lookup"><span data-stu-id="99117-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="99117-130">Affectez la valeur **null** si *bstrExecutablePath* n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="99117-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="99117-131">*vbExpandEnvVarInArgumentsOnServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99117-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99117-132">Indique si le serveur doit développer les variables d’environnement dans les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="99117-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="99117-133">Affectez à ce paramètre la **\_ valeur variant true** si les arguments contiennent des variables d’environnement, ou **\_ false** si les arguments ne contiennent pas de variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="99117-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99117-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99117-134">Return value</span></span>

<span data-ttu-id="99117-135">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="99117-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="99117-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99117-136">Requirements</span></span>



| <span data-ttu-id="99117-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99117-137">Requirement</span></span> | <span data-ttu-id="99117-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="99117-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99117-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99117-139">Minimum supported client</span></span><br/> | <span data-ttu-id="99117-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99117-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="99117-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99117-141">Minimum supported server</span></span><br/> | <span data-ttu-id="99117-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99117-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="99117-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99117-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="99117-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99117-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="99117-145">DLL</span><span class="sxs-lookup"><span data-stu-id="99117-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99117-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99117-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="99117-147">IID</span><span class="sxs-lookup"><span data-stu-id="99117-147">IID</span></span><br/>                      | <span data-ttu-id="99117-148">IID \_ ITSRemoteProgram est défini en tant que FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="99117-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="99117-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99117-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99117-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="99117-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="99117-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="99117-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="99117-152">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="99117-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





