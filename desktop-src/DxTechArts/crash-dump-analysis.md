---
title: 'Analyse de vidage sur plantage '
description: Cet article technique fournit des informations sur l’écriture et l’utilisation d’un minidump.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031493"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="af9f4-103">Analyse de vidage sur plantage </span><span class="sxs-lookup"><span data-stu-id="af9f4-103">Crash Dump Analysis</span></span>

<span data-ttu-id="af9f4-104">Tous les bogues ne peuvent pas être détectés avant la mise en version, ce qui signifie que tous les bogues qui lèvent des exceptions peuvent être détectés avant la publication.</span><span class="sxs-lookup"><span data-stu-id="af9f4-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="af9f4-105">Heureusement, Microsoft a inclus dans le kit de développement logiciel (SDK) de plate-forme une fonction pour aider les développeurs à collecter des informations sur les exceptions découvertes par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="af9f4-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="af9f4-106">La fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) écrit les informations de vidage sur incident nécessaires dans un fichier sans enregistrer la totalité de l’espace de traitement.</span><span class="sxs-lookup"><span data-stu-id="af9f4-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="af9f4-107">Ce fichier d’informations de vidage sur incident est appelé minidump.</span><span class="sxs-lookup"><span data-stu-id="af9f4-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="af9f4-108">Cet article technique fournit des informations sur l’écriture et l’utilisation d’un minidump.</span><span class="sxs-lookup"><span data-stu-id="af9f4-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="af9f4-109">Écriture d’un minidump</span><span class="sxs-lookup"><span data-stu-id="af9f4-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="af9f4-110">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="af9f4-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="af9f4-111">Écriture d’un minidump avec du code</span><span class="sxs-lookup"><span data-stu-id="af9f4-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="af9f4-112">Utilisation de Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="af9f4-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="af9f4-113">Analyse d’un minidump</span><span class="sxs-lookup"><span data-stu-id="af9f4-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="af9f4-114">Utilisation du serveur de symboles publics Microsoft</span><span class="sxs-lookup"><span data-stu-id="af9f4-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="af9f4-115">Débogage d’un minidump avec WinDbg</span><span class="sxs-lookup"><span data-stu-id="af9f4-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="af9f4-116">Utilisation d’outils de Copy-Protection avec minidumps</span><span class="sxs-lookup"><span data-stu-id="af9f4-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="af9f4-117">Résumé</span><span class="sxs-lookup"><span data-stu-id="af9f4-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="af9f4-118">Écriture d’un minidump</span><span class="sxs-lookup"><span data-stu-id="af9f4-118">Writing a Minidump</span></span>

<span data-ttu-id="af9f4-119">Les options de base pour l’écriture d’un minidump sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="af9f4-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="af9f4-120">Ne rien faire.</span><span class="sxs-lookup"><span data-stu-id="af9f4-120">Do nothing.</span></span> <span data-ttu-id="af9f4-121">Windows génère automatiquement un minidump chaque fois qu’un programme lève une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="af9f4-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="af9f4-122">La génération automatique d’un minidump est disponible depuis Windows XP.</span><span class="sxs-lookup"><span data-stu-id="af9f4-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="af9f4-123">Si l’utilisateur l’autorise, le Minidump sera envoyé à Microsoft, et non pas au développeur, via Rapport d’erreurs Windows (WER).</span><span class="sxs-lookup"><span data-stu-id="af9f4-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="af9f4-124">Les développeurs peuvent accéder à ces minidumps via le [programme d’application de bureau Windows](../appxpkg/windows-desktop-application-program.md).</span><span class="sxs-lookup"><span data-stu-id="af9f4-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="af9f4-125">L’utilisation de WER requiert les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="af9f4-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="af9f4-126">Développeurs pour signer leurs applications à l’aide d’Authenticode</span><span class="sxs-lookup"><span data-stu-id="af9f4-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="af9f4-127">Les applications ont une ressource VERSIONINFO valide dans chaque fichier exécutable et DLL</span><span class="sxs-lookup"><span data-stu-id="af9f4-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="af9f4-128">Si vous implémentez une routine personnalisée pour les exceptions non gérées, vous êtes fortement invité à utiliser la fonction [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) dans le gestionnaire d’exceptions pour envoyer également un minidump automatisé à wer.</span><span class="sxs-lookup"><span data-stu-id="af9f4-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="af9f4-129">La fonction **ReportFault** gère tous les problèmes de connexion et d’envoi du Minidump à wer.</span><span class="sxs-lookup"><span data-stu-id="af9f4-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="af9f4-130">Ne pas envoyer de minidumps à WER ne respecte pas les exigences des jeux pour Windows.</span><span class="sxs-lookup"><span data-stu-id="af9f4-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="af9f4-131">Pour plus d’informations sur le fonctionnement de WER, consultez fonctionnement de [rapport d’erreurs Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="af9f4-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="af9f4-132">Pour obtenir une explication des détails de l’inscription, consultez [Présentation de rapport d’erreurs Windows](https://msdn.microsoft.com/) dans la [zone ISV](https://msdn.microsoft.com/)de MSDN.</span><span class="sxs-lookup"><span data-stu-id="af9f4-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="af9f4-133">Utilisez un produit de la Microsoft Visual Studio Team System.</span><span class="sxs-lookup"><span data-stu-id="af9f4-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="af9f4-134">Dans le menu **Déboguer** , cliquez sur **enregistrer le dump sous** pour enregistrer une copie d’un vidage.</span><span class="sxs-lookup"><span data-stu-id="af9f4-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="af9f4-135">L’utilisation d’un vidage enregistré localement n’est qu’une option de test et de débogage interne.</span><span class="sxs-lookup"><span data-stu-id="af9f4-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="af9f4-136">Ajoutez du code à votre projet.</span><span class="sxs-lookup"><span data-stu-id="af9f4-136">Add code to your project.</span></span> <span data-ttu-id="af9f4-137">Ajoutez la fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) et le code de gestion des exceptions approprié pour enregistrer et envoyer un minidump directement au développeur.</span><span class="sxs-lookup"><span data-stu-id="af9f4-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="af9f4-138">Cet article montre comment implémenter cette option.</span><span class="sxs-lookup"><span data-stu-id="af9f4-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="af9f4-139">Toutefois, Notez que **entrée** ne fonctionne pas actuellement avec du code managé et n’est disponible que sur Windows XP, Windows Vista, Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af9f4-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="af9f4-140">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="af9f4-140">Thread safety</span></span>

<span data-ttu-id="af9f4-141">[**Entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fait partie de la bibliothèque dbghelp.</span><span class="sxs-lookup"><span data-stu-id="af9f4-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="af9f4-142">Cette bibliothèque n’est pas thread-safe, donc tout programme qui utilise **entrée** doit synchroniser tous les threads avant de tenter d’appeler **entrée**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="af9f4-143">Écriture d’un minidump avec du code</span><span class="sxs-lookup"><span data-stu-id="af9f4-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="af9f4-144">L’implémentation réelle est simple.</span><span class="sxs-lookup"><span data-stu-id="af9f4-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="af9f4-145">Voici un exemple simple d’utilisation de [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="af9f4-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



<span data-ttu-id="af9f4-146">Cet exemple illustre l’utilisation de base de [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) et les informations minimales nécessaires pour l’appeler.</span><span class="sxs-lookup"><span data-stu-id="af9f4-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="af9f4-147">Le nom du fichier de vidage est celui du développeur. Toutefois, pour éviter les collisions de noms de fichiers, il est recommandé de générer le nom de fichier à partir du nom et du numéro de version de l’application, des ID de processus et de thread, ainsi que de la date et de l’heure.</span><span class="sxs-lookup"><span data-stu-id="af9f4-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="af9f4-148">Cela permet également de conserver les minidumps regroupés par application et par version.</span><span class="sxs-lookup"><span data-stu-id="af9f4-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="af9f4-149">Il revient au développeur de déterminer la quantité d’informations qui est utilisée pour différencier les noms de fichiers minidump.</span><span class="sxs-lookup"><span data-stu-id="af9f4-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="af9f4-150">Notez que le nom du chemin d’accès dans l’exemple précédent a été généré en appelant la fonction [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) pour récupérer le chemin d’accès du répertoire désigné pour les fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="af9f4-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="af9f4-151">L’utilisation de ce répertoire fonctionne même avec les comptes d’utilisateur dotés de privilèges minimum, et il empêche également le Minidump d’occuper de l’espace disque après qu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af9f4-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="af9f4-152">Si vous archivez le produit pendant votre processus de génération quotidien, veillez également à inclure des symboles pour la build afin de pouvoir déboguer une ancienne version du produit, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af9f4-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="af9f4-153">Vous devez également prendre des mesures pour gérer les optimisations complètes du compilateur tout en générant des symboles.</span><span class="sxs-lookup"><span data-stu-id="af9f4-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="af9f4-154">Pour ce faire, ouvrez les propriétés de votre projet dans l’environnement de développement et, pour la configuration Release, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="af9f4-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="af9f4-155">Sur le côté gauche de la page de propriétés du projet, cliquez sur C/C++.</span><span class="sxs-lookup"><span data-stu-id="af9f4-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="af9f4-156">Par défaut, cette option affiche les paramètres **généraux** .</span><span class="sxs-lookup"><span data-stu-id="af9f4-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="af9f4-157">Sur le côté droit de la page de propriétés du projet, définissez **format des informations de débogage** sur **base de données du programme (/ZI)**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="af9f4-158">Sur le côté gauche de la page de propriétés, développez **éditeur de liens**, puis cliquez sur **débogage**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="af9f4-159">Sur le côté droit de la page de propriétés, affectez à **générer des informations de débogage** la valeur **Oui (/Debug)**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="af9f4-160">Cliquez sur **optimisation**, puis définissez les **références** à E liminate les **données non référencées (/OPT : REF)**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="af9f4-161">Définissez **activer le repli COMDAT** pour **Supprimer les COMDAT redondants (/OPT : ICF)**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="af9f4-162">MSDN contient des informations plus détaillées sur la structure d’informations sur les [**\_ exceptions \_ de Minidump**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) et la fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .</span><span class="sxs-lookup"><span data-stu-id="af9f4-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="af9f4-163">Utilisation de Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="af9f4-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="af9f4-164">Dumpchk.exe est un utilitaire de ligne de commande qui peut être utilisé pour vérifier qu’un fichier de vidage a été créé correctement.</span><span class="sxs-lookup"><span data-stu-id="af9f4-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="af9f4-165">Si Dumpchk.exe génère une erreur, cela signifie que le fichier de vidage est endommagé et ne peut pas être analysé.</span><span class="sxs-lookup"><span data-stu-id="af9f4-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="af9f4-166">Pour plus d’informations sur l’utilisation de Dumpchk.exe, consultez [comment utiliser Dumpchk.exe pour vérifier un fichier d’image mémoire](https://support.microsoft.com/kb/315271/).</span><span class="sxs-lookup"><span data-stu-id="af9f4-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="af9f4-167">Dumpchk.exe est inclus sur le CD-ROM du produit Windows XP et peut être installé sur les outils de support des fichiers programme du lecteur système \\ \\ \\ en exécutant Setup.exe dans le \\ dossier Outils de support du \\ CD-ROM du produit Windows XP.</span><span class="sxs-lookup"><span data-stu-id="af9f4-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="af9f4-168">Vous pouvez également vous procurer la dernière version de Dumpchk.exe en téléchargeant et en installant les outils de débogage disponibles à partir des outils de débogage [Windows](https://www.microsoft.com/whdc/devtools/debugging/) sur [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="af9f4-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="af9f4-169">Analyse d’un minidump</span><span class="sxs-lookup"><span data-stu-id="af9f4-169">Analyzing a Minidump</span></span>

<span data-ttu-id="af9f4-170">L’ouverture d’un minidump pour l’analyse est aussi simple que d’en créer un.</span><span class="sxs-lookup"><span data-stu-id="af9f4-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="af9f4-171">**Pour analyser un minidump**</span><span class="sxs-lookup"><span data-stu-id="af9f4-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="af9f4-172">Ouvrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="af9f4-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="af9f4-173">Dans le menu **fichier** , cliquez sur **ouvrir un projet**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="af9f4-174">Définissez **fichiers de type** sur **fichiers dump**, accédez au fichier dump, sélectionnez-le, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="af9f4-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="af9f4-175">Exécutez le débogueur.</span><span class="sxs-lookup"><span data-stu-id="af9f4-175">Run the debugger.</span></span>

<span data-ttu-id="af9f4-176">Le débogueur crée un processus simulé.</span><span class="sxs-lookup"><span data-stu-id="af9f4-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="af9f4-177">Le processus simulé sera arrêté au niveau de l’instruction qui a provoqué l’incident.</span><span class="sxs-lookup"><span data-stu-id="af9f4-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="af9f4-178">Utilisation du serveur de symboles publics Microsoft</span><span class="sxs-lookup"><span data-stu-id="af9f4-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="af9f4-179">Pour obtenir la pile pour les pannes au niveau du pilote ou du système, il peut être nécessaire de configurer Visual Studio pour qu’il pointe vers le serveur de symboles publics Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af9f4-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="af9f4-180">**Pour définir un chemin d’accès au serveur de symboles Microsoft**</span><span class="sxs-lookup"><span data-stu-id="af9f4-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="af9f4-181">Dans le menu **Déboguer** , cliquez sur **options**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="af9f4-182">Dans la boîte de dialogue **options** , ouvrez le nœud **débogage** , puis cliquez sur **symboles**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="af9f4-183">Assurez **-vous que la recherche dans les emplacements ci-dessus uniquement lorsque les symboles sont chargés manuellement** n’est pas sélectionnée, à moins que vous ne souhaitiez charger manuellement les symboles lors du débogage.</span><span class="sxs-lookup"><span data-stu-id="af9f4-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="af9f4-184">Si vous utilisez des symboles sur un serveur de symboles distant, vous pouvez améliorer les performances en spécifiant un répertoire local dans lequel les symboles peuvent être copiés.</span><span class="sxs-lookup"><span data-stu-id="af9f4-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="af9f4-185">Pour ce faire, entrez un chemin d’accès pour les **symboles de cache du serveur de symboles vers ce répertoire**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="af9f4-186">Pour vous connecter au serveur de symboles publics Microsoft, vous devez activer ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="af9f4-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="af9f4-187">Notez que si vous déboguez un programme sur un ordinateur distant, le répertoire de cache fait référence à un répertoire sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="af9f4-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="af9f4-188">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-188">Click **OK**.</span></span>
6.  <span data-ttu-id="af9f4-189">Étant donné que vous utilisez le serveur de symboles publics Microsoft, une boîte de dialogue contrat de licence utilisateur final s’affiche.</span><span class="sxs-lookup"><span data-stu-id="af9f4-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="af9f4-190">Cliquez sur **Oui** pour accepter le contrat et télécharger des symboles dans votre cache local.</span><span class="sxs-lookup"><span data-stu-id="af9f4-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="af9f4-191">Débogage d’un minidump avec WinDbg</span><span class="sxs-lookup"><span data-stu-id="af9f4-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="af9f4-192">Vous pouvez également utiliser WinDbg, un débogueur qui fait partie des outils de débogage Windows, pour déboguer un minidump.</span><span class="sxs-lookup"><span data-stu-id="af9f4-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="af9f4-193">WinDbg vous permet de déboguer sans avoir à utiliser Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="af9f4-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="af9f4-194">Pour télécharger les outils de débogage Windows, consultez [outils de débogage Windows](https://www.microsoft.com/whdc/devtools/debugging/) sur [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="af9f4-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="af9f4-195">Après avoir installé les outils de débogage Windows, vous devez entrer le chemin d’accès aux symboles dans WinDbg.</span><span class="sxs-lookup"><span data-stu-id="af9f4-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="af9f4-196">**Pour entrer un chemin d’accès aux symboles dans WinDbg**</span><span class="sxs-lookup"><span data-stu-id="af9f4-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="af9f4-197">Dans le menu **fichier** , cliquez sur **chemin d’accès aux symboles**.</span><span class="sxs-lookup"><span data-stu-id="af9f4-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="af9f4-198">Dans la fenêtre **chemin de recherche de symboles** , entrez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="af9f4-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="af9f4-199">« SRV \* c : \\ cache \* https://msdl.microsoft.com/download/symbols ; »</span><span class="sxs-lookup"><span data-stu-id="af9f4-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="af9f4-200">Utilisation d’outils de Copy-Protection avec minidumps</span><span class="sxs-lookup"><span data-stu-id="af9f4-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="af9f4-201">Les développeurs doivent également savoir comment leur schéma de protection contre la copie peut affecter le minidump.</span><span class="sxs-lookup"><span data-stu-id="af9f4-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="af9f4-202">La plupart des schémas de protection contre la copie ont leurs propres outils de déchiffrement, et il appartient au développeur d’apprendre à utiliser ces outils avec [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="af9f4-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="af9f4-203">Résumé</span><span class="sxs-lookup"><span data-stu-id="af9f4-203">Summary</span></span>

<span data-ttu-id="af9f4-204">La fonction [**entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) peut être un outil extrêmement utile pour la collecte et la résolution des bogues une fois que le produit a été publié.</span><span class="sxs-lookup"><span data-stu-id="af9f4-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="af9f4-205">L’écriture d’un gestionnaire d’exceptions personnalisé qui utilise **entrée** permet au développeur de personnaliser la collection d’informations et d’améliorer le processus de débogage.</span><span class="sxs-lookup"><span data-stu-id="af9f4-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="af9f4-206">La fonction est suffisamment flexible pour être utilisée dans n’importe quel projet basé sur C++ et doit être considérée comme faisant partie du processus de stabilité du projet.</span><span class="sxs-lookup"><span data-stu-id="af9f4-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 