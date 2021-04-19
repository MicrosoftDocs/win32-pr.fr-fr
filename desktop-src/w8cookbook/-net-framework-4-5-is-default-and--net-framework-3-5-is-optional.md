---
title: .NET Framework les paramètres par défaut
description: .NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "106510504"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="d5c06-103">.NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif</span><span class="sxs-lookup"><span data-stu-id="d5c06-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="d5c06-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="d5c06-104">Platforms</span></span>

<span data-ttu-id="d5c06-105">**Clients**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5c06-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="d5c06-106">**Serveurs**   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5c06-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="d5c06-107">Description</span><span class="sxs-lookup"><span data-stu-id="d5c06-107">Description</span></span>

<span data-ttu-id="d5c06-108">.NET Framework 4,5 est activé par défaut dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5c06-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="d5c06-109">Windows 8 n’inclut pas .NET 3,5 par défaut, mais les fichiers pour .NET 3,5 sont disponibles sur le support d’installation de Windows 8 en tant que fonctionnalité facultative.</span><span class="sxs-lookup"><span data-stu-id="d5c06-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="d5c06-110">Si l’utilisateur met à niveau Windows 7 vers Windows 8, .NET Framework 3,5 est entièrement activé pour s’assurer que toutes les applications sur l’ordinateur continuent de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="d5c06-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d5c06-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="d5c06-111">Manifestation</span></span>

<span data-ttu-id="d5c06-112">Si l’utilisateur effectue une nouvelle installation de Windows 8, puis installe les applications qui requièrent .NET Framework 3,5 (ou 2,0), il déclenche une demande pour les fichiers .NET 3,5 nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d5c06-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="d5c06-113">Normalement, les fichiers manquants seront téléchargés à partir de Windows Update (après avoir demandé l’autorisation à l’utilisateur), mais si l’accès à Windows Update n’est pas possible, l’activation de .NET Framework 3,5 échouera, sauf si une autre source pour les fichiers manquants a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d5c06-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="d5c06-114">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="d5c06-114">Mitigation</span></span>

<span data-ttu-id="d5c06-115">Pour activer .NET Framework 3,5 sur les ordinateurs de test uniquement avec des installations propres de Windows 8 :</span><span class="sxs-lookup"><span data-stu-id="d5c06-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="d5c06-116">Copiez \\ \\ les sources côte \\ à côte de l’image ISO de la build du système d’exploitation monté vers dotnet35 ou un dossier similaire.</span><span class="sxs-lookup"><span data-stu-id="d5c06-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="d5c06-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d5c06-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="d5c06-118">Exécutez cette ligne de commande en utilisant des privilèges d’administrateur :</span><span class="sxs-lookup"><span data-stu-id="d5c06-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="d5c06-119">Le dossier de sources \\ SxS ne doit pas être utilisé comme mécanisme de redistribution, car il ne s’agit pas d’un mécanisme pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d5c06-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="d5c06-120">Solution</span><span class="sxs-lookup"><span data-stu-id="d5c06-120">Solution</span></span>

<span data-ttu-id="d5c06-121">**Pour les consommateurs :**</span><span class="sxs-lookup"><span data-stu-id="d5c06-121">**For consumers:**</span></span>

<span data-ttu-id="d5c06-122">Windows 8 comprend un mécanisme qui active automatiquement .NET Framework 3,5 quand vous tentez d’installer le package redistribuable ou lorsqu’un programme d’installation d’application nécessitant .NET 3,5 appelle le package redistribuable.</span><span class="sxs-lookup"><span data-stu-id="d5c06-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="d5c06-123">**Pour les développeurs d’applications (et les administrateurs informatiques) :**</span><span class="sxs-lookup"><span data-stu-id="d5c06-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="d5c06-124">Les administrateurs informatiques peuvent configurer les applications .NET 3,5 pour qu’elles s’exécutent sur .NET 3,5 ou .NET 4,5 (en fonction de ce qui est déjà installé).</span><span class="sxs-lookup"><span data-stu-id="d5c06-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="d5c06-125">Pour exécuter une application gérée sur 3,5 ou 4,5, ajoutez simplement une section dans le fichier de configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5c06-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="d5c06-126">Cela permet de s’assurer que si .NET 3,5 est installé, l’application s’exécutera sur .NET 3,5. dans le cas contraire, l’application s’exécutera sur .NET 4,5.</span><span class="sxs-lookup"><span data-stu-id="d5c06-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="d5c06-127">Vous trouverez ci-dessous un exemple de la section supplémentaire dans le fichier de configuration :</span><span class="sxs-lookup"><span data-stu-id="d5c06-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="d5c06-128">**Pour les OEM d’entreprise :**</span><span class="sxs-lookup"><span data-stu-id="d5c06-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="d5c06-129">Pour activer .NET Framework 3,5 pour les builds EEAP et pour les applications qui n’ont pas accès à Windows Update :</span><span class="sxs-lookup"><span data-stu-id="d5c06-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="d5c06-130">Copiez les \\ sources \\ côte \\ à côte de l’image ISO de build de système d’exploitation montée dans le dossier dotnet35 ou similaire.</span><span class="sxs-lookup"><span data-stu-id="d5c06-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="d5c06-131">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d5c06-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="d5c06-132">Définissez la valeur de la RegKey :</span><span class="sxs-lookup"><span data-stu-id="d5c06-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="d5c06-133">**Pour les entreprises :**</span><span class="sxs-lookup"><span data-stu-id="d5c06-133">**For enterprises:**</span></span>

<span data-ttu-id="d5c06-134">Pour les ordinateurs configurés pour utiliser WSUS pour la maintenance, vous pouvez définir une entrée de Registre pour permettre à l’ordinateur d’utiliser Windows Update pour l’activation de .NET 3,5 au lieu de WSUS (la maintenance sera toujours effectuée à partir de WSUS si vous le faites).</span><span class="sxs-lookup"><span data-stu-id="d5c06-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="d5c06-135">Définissez la valeur de la RegKey :</span><span class="sxs-lookup"><span data-stu-id="d5c06-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="d5c06-136">Cette entrée de Registre peut également être définie via stratégie de groupe (stratégie de l’ordinateur local-> configuration de l’ordinateur-> système Modèles d’administration->.</span><span class="sxs-lookup"><span data-stu-id="d5c06-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="d5c06-137">Sélectionnez le paramètre spécifier les paramètres pour l’installation des composants facultatifs et la réparation des composants.</span><span class="sxs-lookup"><span data-stu-id="d5c06-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="d5c06-138">Si vous sélectionnez contacter Windows Update directement pour télécharger le contenu de réparation au lieu de Windows Server Update Services (WSUS), toute tentative d’ajouter des fonctionnalités Windows (par exemple, .NET Framework 3,5) ou des fonctionnalités de réparation déclenchera des téléchargements de fichiers à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d5c06-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="d5c06-139">Les ordinateurs cibles requièrent un accès Internet et WU pour cette option.</span><span class="sxs-lookup"><span data-stu-id="d5c06-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="d5c06-140">Les opérations de maintenance normales continuent à utiliser WSUS si elle a été configurée en tant que source.</span><span class="sxs-lookup"><span data-stu-id="d5c06-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="d5c06-141">**Note relative à la définition de l’emplacement source local via des entrées de Registre**</span><span class="sxs-lookup"><span data-stu-id="d5c06-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="d5c06-142">Les administrateurs informatiques peuvent définir des emplacements sources locaux pour les fichiers .NET 3,5 à l’aide d’une entrée de Registre, afin que les utilisateurs puissent utiliser la boîte de dialogue Ajouter/supprimer des fonctionnalités Windows pour activer des fonctionnalités avec une charge utile manquante sans avoir à spécifier un emplacement source.</span><span class="sxs-lookup"><span data-stu-id="d5c06-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="d5c06-143">La valeur de l’entrée de Registre peut être contrôlée via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d5c06-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="d5c06-144">Cette entrée de Registre est prise en charge :</span><span class="sxs-lookup"><span data-stu-id="d5c06-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5c06-145">Entrée</span><span class="sxs-lookup"><span data-stu-id="d5c06-145">Entry</span></span></th>
<th><span data-ttu-id="d5c06-146">Type</span><span class="sxs-lookup"><span data-stu-id="d5c06-146">Type</span></span></th>
<th><span data-ttu-id="d5c06-147">Description</span><span class="sxs-lookup"><span data-stu-id="d5c06-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5c06-148">Chemin de la source locale</span><span class="sxs-lookup"><span data-stu-id="d5c06-148">Local Source Path</span></span></td>
<td><span data-ttu-id="d5c06-149">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="d5c06-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="d5c06-150">Chemin (s) source local à utiliser par défaut.</span><span class="sxs-lookup"><span data-stu-id="d5c06-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="d5c06-151">Plusieurs chemins d’accès peuvent être spécifiés ; ils doivent être séparés par ;.</span><span class="sxs-lookup"><span data-stu-id="d5c06-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="d5c06-152">Les emplacements sont recherchés dans l’ordre dans lequel ils sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d5c06-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="d5c06-153">Les emplacements sources locaux qui sont spécifiés sur la ligne de commande DISM ont la priorité sur les emplacements spécifiés dans cette entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="d5c06-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="d5c06-154">Les emplacements de dossier peuvent être spécifiés dans cette entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="d5c06-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="d5c06-155">Les fichiers WIM peut être utilisé, mais le chemin d’accès doit être au fichier WIM ; Il n’est pas nécessaire de le monter, par exemple :</span><span class="sxs-lookup"><span data-stu-id="d5c06-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="d5c06-156">Wim : \\ machine\share\file.wim : 1</span><span class="sxs-lookup"><span data-stu-id="d5c06-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="d5c06-157">Notez le 1 à la fin.</span><span class="sxs-lookup"><span data-stu-id="d5c06-157">Notice the  1  at the end.</span></span> <span data-ttu-id="d5c06-158">Vous devez spécifier l’index numérique de l’image que vous souhaitez utiliser dans le fichier WIM.</span><span class="sxs-lookup"><span data-stu-id="d5c06-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="d5c06-159">Pour un fichier WIM monté, le chemin source doit faire référence au répertoire Windows de l’image montée, plutôt qu’au point de montage (par exemple:/source : <mount_point> \Windows plutôt que/source : <mount_point> ).</span><span class="sxs-lookup"><span data-stu-id="d5c06-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="d5c06-160">Ressources</span><span class="sxs-lookup"><span data-stu-id="d5c06-160">Resources</span></span>

<dl>

[<span data-ttu-id="d5c06-161">Implémentation d’une stratégie basée sur le registre</span><span class="sxs-lookup"><span data-stu-id="d5c06-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>