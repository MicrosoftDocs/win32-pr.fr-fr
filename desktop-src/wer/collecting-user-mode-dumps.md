---
title: Collecte des vidages de User-Mode
description: À compter de Windows Server 2008 et de Windows Vista avec Service Pack 1 (SP1), Rapport d’erreurs Windows (WER) peut être configuré de sorte que les vidages en mode utilisateur complets soient collectés et stockés localement après une panne d’application en mode utilisateur.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842110"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="97817-103">Collecte des vidages de User-Mode</span><span class="sxs-lookup"><span data-stu-id="97817-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="97817-104">À compter de Windows Server 2008 et de Windows Vista avec Service Pack 1 (SP1), Rapport d’erreurs Windows (WER) peut être configuré de sorte que les vidages en mode utilisateur complets soient collectés et stockés localement après une panne d’application en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97817-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="97817-105">Les applications qui effectuent leurs propres rapports d’incident personnalisés, y compris les applications .NET, ne sont pas prises en charge par cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="97817-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="97817-106">Cette fonctionnalité n’est pas activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="97817-106">This feature is not enabled by default.</span></span> <span data-ttu-id="97817-107">L’activation de la fonctionnalité requiert des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="97817-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="97817-108">Pour activer et configurer la fonctionnalité, utilisez les valeurs de Registre suivantes sous la clé **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ rapport d’erreurs Windows \\ LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="97817-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97817-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="97817-109">Value</span></span></th>
<th><span data-ttu-id="97817-110">Description</span><span class="sxs-lookup"><span data-stu-id="97817-110">Description</span></span></th>
<th><span data-ttu-id="97817-111">Type</span><span class="sxs-lookup"><span data-stu-id="97817-111">Type</span></span></th>
<th><span data-ttu-id="97817-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="97817-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97817-113"><strong>DumpFolder</strong></span><span class="sxs-lookup"><span data-stu-id="97817-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="97817-114">Chemin d’accès où les fichiers de vidage doivent être stockés.</span><span class="sxs-lookup"><span data-stu-id="97817-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="97817-115">Si vous n’utilisez pas le chemin d’accès par défaut, assurez-vous que le dossier contient des listes de contrôle d’accès qui permettent au processus de blocage d’écrire des données dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="97817-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="97817-116">Pour les pannes de service, le vidage est écrit dans des dossiers de profil spécifiques au service en fonction du compte de service utilisé.</span><span class="sxs-lookup"><span data-stu-id="97817-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="97817-117">Par exemple, le dossier de profil des services système est%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="97817-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="97817-118">Pour les services réseau et locaux, le dossier est%WINDIR%\ServiceProfiles.</span><span class="sxs-lookup"><span data-stu-id="97817-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="97817-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="97817-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="97817-120">%LOCALAPPDATA%\CrashDumps</span><span class="sxs-lookup"><span data-stu-id="97817-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97817-121"><strong>DumpCount</strong></span><span class="sxs-lookup"><span data-stu-id="97817-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="97817-122">Nombre maximal de fichiers de vidage dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="97817-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="97817-123">Lorsque la valeur maximale est dépassée, le fichier de vidage le plus ancien dans le dossier sera remplacé par le nouveau fichier de vidage.</span><span class="sxs-lookup"><span data-stu-id="97817-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="97817-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97817-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="97817-125">10</span><span class="sxs-lookup"><span data-stu-id="97817-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97817-126"><strong>DumpType</strong></span><span class="sxs-lookup"><span data-stu-id="97817-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="97817-127">Spécifiez l’un des types de vidages suivants :</span><span class="sxs-lookup"><span data-stu-id="97817-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="97817-128">0 : vidage personnalisé</span><span class="sxs-lookup"><span data-stu-id="97817-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="97817-129">1 : mini-vidage</span><span class="sxs-lookup"><span data-stu-id="97817-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="97817-130">2 : vidage complet</span><span class="sxs-lookup"><span data-stu-id="97817-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="97817-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97817-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="97817-132">1</span><span class="sxs-lookup"><span data-stu-id="97817-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97817-133"><strong>CustomDumpFlags</strong></span><span class="sxs-lookup"><span data-stu-id="97817-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="97817-134">Options de vidage personnalisées à utiliser.</span><span class="sxs-lookup"><span data-stu-id="97817-134">The custom dump options to be used.</span></span> <span data-ttu-id="97817-135">Cette valeur est utilisée uniquement lorsque <strong>DumpType</strong> a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="97817-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="97817-136">Les options sont une combinaison au niveau du bit des valeurs d’énumération <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="97817-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="97817-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97817-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="97817-138">Un vidage sur incident n’est pas collecté lorsque vous définissez le [débogage automatique pour les blocages d' **application**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span><span class="sxs-lookup"><span data-stu-id="97817-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="97817-139">Ces valeurs de Registre représentent les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="97817-139">These registry values represent the global settings.</span></span> <span data-ttu-id="97817-140">Vous pouvez également fournir des paramètres par application qui remplacent les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="97817-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="97817-141">Pour créer un paramètre par application, créez une clé pour votre application sous **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ rapport d’erreurs Windows \\ LocalDumps** (par exemple, **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ rapport d’erreurs Windows \\ LocalDumps \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="97817-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="97817-142">Ajoutez vos paramètres de vidage sous la clé **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="97817-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="97817-143">Si votre application se bloque, le WER commence par lire les paramètres globaux, puis remplace l’un des paramètres par vos paramètres spécifiques à votre application.</span><span class="sxs-lookup"><span data-stu-id="97817-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="97817-144">Quand une application se bloque et avant son arrêt, le système vérifie les paramètres du Registre pour déterminer si un vidage local doit être collecté.</span><span class="sxs-lookup"><span data-stu-id="97817-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="97817-145">Une fois la collecte de vidage terminée, l’application est autorisée à se terminer normalement.</span><span class="sxs-lookup"><span data-stu-id="97817-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="97817-146">Si l’application prend en charge la récupération, le vidage local est collecté avant l’appel du rappel de récupération.</span><span class="sxs-lookup"><span data-stu-id="97817-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="97817-147">Ces vidages sont configurés et contrôlés indépendamment du reste de l’infrastructure WER.</span><span class="sxs-lookup"><span data-stu-id="97817-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="97817-148">Vous pouvez utiliser la collection de vidages locaux même si le rapport d’erreurs Windows est désactivé ou si l’utilisateur annule la création de rapports WER.</span><span class="sxs-lookup"><span data-stu-id="97817-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="97817-149">Le vidage local peut être différent de celui envoyé à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97817-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

