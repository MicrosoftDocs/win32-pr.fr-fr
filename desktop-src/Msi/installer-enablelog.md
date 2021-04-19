---
description: La méthode EnableLog de l’objet installer active la journalisation du type de message sélectionné pour toutes les sessions d’installation suivantes dans l’espace de processus actuel.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538076"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="c8e37-103">Installer. EnableLog, méthode</span><span class="sxs-lookup"><span data-stu-id="c8e37-103">Installer.EnableLog method</span></span>

<span data-ttu-id="c8e37-104">La méthode **EnableLog** de l’objet [**installer**](installer-object.md) active la journalisation du type de message sélectionné pour toutes les sessions d’installation suivantes dans l’espace de processus actuel.</span><span class="sxs-lookup"><span data-stu-id="c8e37-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8e37-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="c8e37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e37-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="c8e37-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e37-108">Chaîne obligatoire qui contient des lettres représentant les types de messages à consigner.</span><span class="sxs-lookup"><span data-stu-id="c8e37-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="c8e37-109">La chaîne peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8e37-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="c8e37-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8e37-110">Value</span></span> | <span data-ttu-id="c8e37-111">Description</span><span class="sxs-lookup"><span data-stu-id="c8e37-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e37-112">I</span><span class="sxs-lookup"><span data-stu-id="c8e37-112">I</span></span>     | <span data-ttu-id="c8e37-113">Messages d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="c8e37-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="c8e37-114">w</span><span class="sxs-lookup"><span data-stu-id="c8e37-114">w</span></span>     | <span data-ttu-id="c8e37-115">Messages d’avertissement non récupérables.</span><span class="sxs-lookup"><span data-stu-id="c8e37-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="c8e37-116">e</span><span class="sxs-lookup"><span data-stu-id="c8e37-116">e</span></span>     | <span data-ttu-id="c8e37-117">Messages d’erreur pouvant être des erreurs irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="c8e37-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="c8e37-118">f</span><span class="sxs-lookup"><span data-stu-id="c8e37-118">f</span></span>     | <span data-ttu-id="c8e37-119">Liste des fichiers en cours d’utilisation qui doivent être remplacés.</span><span class="sxs-lookup"><span data-stu-id="c8e37-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="c8e37-120">a</span><span class="sxs-lookup"><span data-stu-id="c8e37-120">a</span></span>     | <span data-ttu-id="c8e37-121">Début de la notification d’action.</span><span class="sxs-lookup"><span data-stu-id="c8e37-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="c8e37-122">r</span><span class="sxs-lookup"><span data-stu-id="c8e37-122">r</span></span>     | <span data-ttu-id="c8e37-123">Enregistrement de données d’action contenant du contenu spécifique à l’action.</span><span class="sxs-lookup"><span data-stu-id="c8e37-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="c8e37-124">u</span><span class="sxs-lookup"><span data-stu-id="c8e37-124">u</span></span>     | <span data-ttu-id="c8e37-125">Messages de demande de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8e37-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="c8e37-126">c</span><span class="sxs-lookup"><span data-stu-id="c8e37-126">c</span></span>     | <span data-ttu-id="c8e37-127">Paramètres d’initialisation de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8e37-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="c8e37-128">m</span><span class="sxs-lookup"><span data-stu-id="c8e37-128">m</span></span>     | <span data-ttu-id="c8e37-129">Message d’insuffisance de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c8e37-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="c8e37-130">v</span><span class="sxs-lookup"><span data-stu-id="c8e37-130">v</span></span>     | <span data-ttu-id="c8e37-131">L’envoi de grandes quantités d’informations au fichier journal n’est généralement pas utile aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c8e37-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="c8e37-132">Peut être utilisé pour la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c8e37-132">May be used for support.</span></span> |
| <span data-ttu-id="c8e37-133">p</span><span class="sxs-lookup"><span data-stu-id="c8e37-133">p</span></span>     | <span data-ttu-id="c8e37-134">Table des propriétés de vidage ; « property = value » à l’arrêt du moteur</span><span class="sxs-lookup"><span data-stu-id="c8e37-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="c8e37-135">Ajouter au fichier journal existant.</span><span class="sxs-lookup"><span data-stu-id="c8e37-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="c8e37-136">!</span><span class="sxs-lookup"><span data-stu-id="c8e37-136">!</span></span>     | <span data-ttu-id="c8e37-137">Videz chaque ligne dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c8e37-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="c8e37-138">x</span><span class="sxs-lookup"><span data-stu-id="c8e37-138">x</span></span>     | <span data-ttu-id="c8e37-139">Informations supplémentaires sur le débogage.</span><span class="sxs-lookup"><span data-stu-id="c8e37-139">Extra debugging information.</span></span> <span data-ttu-id="c8e37-140">Cette option est disponible uniquement avec Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c8e37-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="c8e37-141">o</span><span class="sxs-lookup"><span data-stu-id="c8e37-141">o</span></span>     | <span data-ttu-id="c8e37-142">Messages d’espace disque insuffisants.</span><span class="sxs-lookup"><span data-stu-id="c8e37-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="c8e37-143">*Relog*</span><span class="sxs-lookup"><span data-stu-id="c8e37-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e37-144">Chaîne obligatoire contenant le chemin d’accès au fichier journal à créer.</span><span class="sxs-lookup"><span data-stu-id="c8e37-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="c8e37-145">Utilisez une chaîne vide ("") pour désactiver la journalisation.</span><span class="sxs-lookup"><span data-stu-id="c8e37-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e37-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8e37-146">Return value</span></span>

<span data-ttu-id="c8e37-147">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c8e37-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e37-148">Notes</span><span class="sxs-lookup"><span data-stu-id="c8e37-148">Remarks</span></span>

<span data-ttu-id="c8e37-149">Le chemin d’accès à l’emplacement du fichier journal doit déjà exister lors de l’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c8e37-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="c8e37-150">Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c8e37-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="c8e37-151">Les options de journalisation définies à l’aide de **EnableLog** remplacent les paramètres de stratégie de journalisation Windows Installer existants.</span><span class="sxs-lookup"><span data-stu-id="c8e37-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="c8e37-152">La journalisation remplace un fichier journal existant par défaut.</span><span class="sxs-lookup"><span data-stu-id="c8e37-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="c8e37-153">Vous devez utiliser la lettre « + » dans le mode de journalisation pour ajouter à un fichier journal existant.</span><span class="sxs-lookup"><span data-stu-id="c8e37-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="c8e37-154">L’option' ! 'n’est pas recommandée, car elle peut ralentir considérablement l’installation.</span><span class="sxs-lookup"><span data-stu-id="c8e37-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="c8e37-155">Cette option peut être utile lors du débogage d’une installation.</span><span class="sxs-lookup"><span data-stu-id="c8e37-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="c8e37-156">L’exemple de script suivant active la journalisation documentée pour une installation.</span><span class="sxs-lookup"><span data-stu-id="c8e37-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="c8e37-157">À la fin de l’installation, le fichier journal généré se trouve dans c : \\ temp \\ install. log.</span><span class="sxs-lookup"><span data-stu-id="c8e37-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="c8e37-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8e37-158">Requirements</span></span>



| <span data-ttu-id="c8e37-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8e37-159">Requirement</span></span> | <span data-ttu-id="c8e37-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8e37-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e37-161">Version</span><span class="sxs-lookup"><span data-stu-id="c8e37-161">Version</span></span><br/> | <span data-ttu-id="c8e37-162">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8e37-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c8e37-163">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8e37-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c8e37-164">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8e37-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c8e37-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c8e37-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8e37-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8e37-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c8e37-167">IID</span><span class="sxs-lookup"><span data-stu-id="c8e37-167">IID</span></span><br/>     | <span data-ttu-id="c8e37-168">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c8e37-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c8e37-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8e37-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e37-170">Journalisation Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c8e37-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




