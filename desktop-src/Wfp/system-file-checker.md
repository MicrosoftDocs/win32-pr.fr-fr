---
description: L’utilitaire Vérificateur des fichiers système, Sfc.exe, permet aux administrateurs d’analyser toutes les ressources protégées pour vérifier leurs versions.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: Vérificateur des fichiers système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525726"
---
# <a name="system-file-checker"></a><span data-ttu-id="9d597-103">Vérificateur des fichiers système</span><span class="sxs-lookup"><span data-stu-id="9d597-103">System File Checker</span></span>

<span data-ttu-id="9d597-104">L’utilitaire Vérificateur des fichiers système, Sfc.exe, permet aux administrateurs d’analyser toutes les ressources protégées pour vérifier leurs versions.</span><span class="sxs-lookup"><span data-stu-id="9d597-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="9d597-105">Les fichiers essentiels pour redémarrer Windows qui ne correspondent pas à la version Windows attendue peuvent être remplacés par les versions appropriées.</span><span class="sxs-lookup"><span data-stu-id="9d597-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="9d597-106">Si un fichier est réparé, les données de registre correspondantes sont également réparées.</span><span class="sxs-lookup"><span data-stu-id="9d597-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="9d597-107">Les fichiers protégés non critiques pour redémarrer Windows ne sont pas réparés.</span><span class="sxs-lookup"><span data-stu-id="9d597-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d597-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d597-108">Syntax</span></span>

<span data-ttu-id="9d597-109">Voici la syntaxe de la ligne de commande pour SFC.</span><span class="sxs-lookup"><span data-stu-id="9d597-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="9d597-110">**Options SFC \[ = chemin d’accès complet au fichier\]**</span><span class="sxs-lookup"><span data-stu-id="9d597-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="9d597-111">Options</span><span class="sxs-lookup"><span data-stu-id="9d597-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="9d597-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*</span><span class="sxs-lookup"><span data-stu-id="9d597-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="9d597-113">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-113">This value is not supported.</span></span>

<span data-ttu-id="9d597-114">**Windows Server 2003 et Windows XP :** Définit la taille du cache de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9d597-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="9d597-115">La taille par défaut du cache est 0x32 (50 Mo).</span><span class="sxs-lookup"><span data-stu-id="9d597-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="9d597-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="9d597-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="9d597-117">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="9d597-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="9d597-119">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="9d597-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="9d597-121">Vérifiez ou réparez uniquement les fichiers.</span><span class="sxs-lookup"><span data-stu-id="9d597-121">Verify or repair only files.</span></span> <span data-ttu-id="9d597-122">Ne vérifiez pas ou ne réparez pas les clés de registre.</span><span class="sxs-lookup"><span data-stu-id="9d597-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="9d597-123">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="9d597-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="9d597-125">Utilisez cette option pour les réparations hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9d597-125">Use this option for offline repairs.</span></span> <span data-ttu-id="9d597-126">Spécifiez l’emplacement du répertoire de démarrage hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9d597-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="9d597-127">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="9d597-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="9d597-129">Utilisez cette option pour les réparations hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9d597-129">Use this option for offline repairs.</span></span> <span data-ttu-id="9d597-130">Spécifiez l’emplacement du répertoire Windows hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9d597-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="9d597-131">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="9d597-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="9d597-133">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-133">This value is not supported.</span></span>

<span data-ttu-id="9d597-134">**Windows Server 2003 et Windows XP :** Vide le cache de fichiers et analyse tous les fichiers système protégés.</span><span class="sxs-lookup"><span data-stu-id="9d597-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="9d597-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="9d597-136">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="9d597-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="9d597-138">Revenez aux paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d597-138">Return to default settings.</span></span>

<span data-ttu-id="9d597-139">**Windows Server 2008 et Windows Vista :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>Vérifie</span><span class="sxs-lookup"><span data-stu-id="9d597-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="9d597-141">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-141">This value is not supported.</span></span>

<span data-ttu-id="9d597-142">**Windows Server 2003 et Windows XP :** Analyse tous les fichiers système protégés à chaque démarrage.</span><span class="sxs-lookup"><span data-stu-id="9d597-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="9d597-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="9d597-144">Analyse et répare le fichier situé dans le chemin d’accès complet spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d597-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="9d597-145">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="9d597-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="9d597-147">Analyse immédiatement tous les fichiers système protégés.</span><span class="sxs-lookup"><span data-stu-id="9d597-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="9d597-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="9d597-149">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-149">This value is not supported.</span></span>

<span data-ttu-id="9d597-150">**Windows Server 2003 et Windows XP :** Analyse tous les fichiers système protégés au prochain démarrage.</span><span class="sxs-lookup"><span data-stu-id="9d597-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="9d597-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="9d597-152">Vérifie le fichier au chemin d’accès complet spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d597-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="9d597-153">Cette option ne répare pas le fichier.</span><span class="sxs-lookup"><span data-stu-id="9d597-153">This option does not repair the file.</span></span>

<span data-ttu-id="9d597-154">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d597-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span><span class="sxs-lookup"><span data-stu-id="9d597-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="9d597-156">Analyse tous les fichiers système protégés, mais ne répare pas les fichiers.</span><span class="sxs-lookup"><span data-stu-id="9d597-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="9d597-157">**Windows XP :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d597-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="9d597-158">SFC définit la valeur de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="9d597-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="9d597-159">= HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SfcScan</span><span class="sxs-lookup"><span data-stu-id="9d597-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="9d597-160">Pour plus d’informations, consultez [valeurs de Registre WFP](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="9d597-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d597-161">Notes</span><span class="sxs-lookup"><span data-stu-id="9d597-161">Remarks</span></span>

<span data-ttu-id="9d597-162">Sur Windows Vista uniquement, vous pouvez définir la variable d’environnement du **\_ \_ Journal de suivi Windows** sur l’emplacement d’un répertoire valide pour recevoir un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="9d597-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="9d597-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d597-163">Examples</span></span>

<span data-ttu-id="9d597-164">Les exemples de lignes de commande suivants sont des exemples de syntaxe de sfc.exe.</span><span class="sxs-lookup"><span data-stu-id="9d597-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="9d597-165">**sfc/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="9d597-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="9d597-166">**SFC/VERIFYFILE = c : \\ Windows \\ system32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="9d597-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="9d597-167">**SFC/SCANFILE = d : \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d : \\ /OFFWINDIR = d : \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="9d597-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="9d597-168">**SFC/VERIFYONLY/FILESONLY**</span><span class="sxs-lookup"><span data-stu-id="9d597-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



