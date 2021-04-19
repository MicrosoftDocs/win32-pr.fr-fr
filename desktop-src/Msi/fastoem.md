---
description: La propriété FASTOEM est conçue pour permettre aux OEM de réduire le temps nécessaire à l’installation de Windows Installer applications pour un scénario spécifique.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533232"
---
# <a name="fastoem-property"></a><span data-ttu-id="ae2b9-103">FASTOEM, propriété</span><span class="sxs-lookup"><span data-stu-id="ae2b9-103">FASTOEM property</span></span>

<span data-ttu-id="ae2b9-104">La propriété **FASTOEM** est conçue pour permettre aux OEM de réduire le temps nécessaire à l’installation de Windows Installer applications pour un scénario spécifique.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="ae2b9-105">Ne créez pas la propriété **FASTOEM** dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b9-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="ae2b9-106">La propriété **FASTOEM** n’est applicable que si toutes les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="ae2b9-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="ae2b9-107">L’application est en cours d’installation sur le même volume que le dossier contenant les fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="ae2b9-108">Les fichiers sources sont supprimés après l’installation.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="ae2b9-109">Aucune interface utilisateur n’est affichée au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="ae2b9-110">Le [niveau de l’interface utilisateur](user-interface-levels.md) est aucun.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="ae2b9-111">L’installation est effectuée dans le [contexte d’installation](installation-context.md)par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="ae2b9-112">Il y a suffisamment d’espace sur l’ordinateur pour une installation réussie.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="ae2b9-113">Il s’agit de la première installation.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-113">This is first time installation.</span></span> <span data-ttu-id="ae2b9-114">L’installation n’a pas pour effet de publier, de réinstaller, de supprimer ou d’exécuter une installation administrative.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="ae2b9-115">Aucune fonctionnalité n’est installée pour être exécutée à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="ae2b9-116">Le package d’installation ne contient aucun [composant isolé](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b9-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="ae2b9-117">Étant donné que les composants isolés requièrent que les fichiers sources restent situés à la source, la propriété **FASTOEM** ne peut pas être utilisée actuellement avec des composants isolés.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="ae2b9-118">Si toutes les conditions précédentes sont remplies, la définition de la propriété **FASTOEM** permet à Windows Installer d’améliorer les performances en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae2b9-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="ae2b9-119">Déplacer au lieu de copier les fichiers sur le même volume.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="ae2b9-120">Cela ne garantit pas que tous les fichiers sont déplacés au lieu d’être copiés.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="ae2b9-121">Notez que si l’ordinateur comporte plusieurs disques durs, vous devez initialiser la propriété [**ROOTDRIVE**](rootdrive.md) sur la ligne de commande sur le même lecteur contenant la source d’installation.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="ae2b9-122">Omettez cette source dans la liste source de l’application afin que les installations de réinstallation ou de maintenance suivantes retrouvent par défaut les sources de CD-ROM spécifiées dans la [table des médias](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b9-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="ae2b9-123">Rationalisez les [coûts des fichiers](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b9-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="ae2b9-124">Supprime les messages de progression envoyés de Windows Installer au client.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2b9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ae2b9-125">Remarks</span></span>

<span data-ttu-id="ae2b9-126">Étant donné qu’aucun message de progression n’est envoyé lorsque **FASTOEM** est défini, il est recommandé que les auteurs écrivent manuellement la valeur 1800 pour le délai d’expiration dans la clé</span><span class="sxs-lookup"><span data-stu-id="ae2b9-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="ae2b9-127">**HKLM** \\ **Logiciel** \\ **Stratégies** \\ **Microsoft** \\ **Windows** \\ **Programme d’installation** \\ **Délai d’expiration**</span><span class="sxs-lookup"><span data-stu-id="ae2b9-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="ae2b9-128">Timeout est un type de **valeur de Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ae2b9-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="ae2b9-129">Pour afficher la taille de l’application dans Ajout/suppression de programmes dans le panneau de configuration de Windows 2000, vous devez écrire manuellement la valeur de EstimatedSize dans la clé</span><span class="sxs-lookup"><span data-stu-id="ae2b9-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="ae2b9-130">**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **<  Code > du produit**</span><span class="sxs-lookup"><span data-stu-id="ae2b9-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="ae2b9-131">Il s’agit d’un type de **valeur de Registre \_ DWORD** qui est égal à la taille de l’application, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="ae2b9-132">Le programme d’installation n’écrit pas automatiquement cette valeur.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="ae2b9-133">Utilisez l’exemple de ligne de commande suivant si le CD-ROM fourni aux utilisateurs finaux stocke le package d’installation de l’application à la racine du CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="ae2b9-134">Notez que le nom du volume dans la [table des médias](media-table.md) du fichier. msi doit correspondre au nom du volume du CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="ae2b9-135">**Msiexec/I C : \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 disablerollback = 1 ROOTDRIVE = C :\\**</span><span class="sxs-lookup"><span data-stu-id="ae2b9-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="ae2b9-136">Utilisez l’exemple de ligne de commande suivant si le package d’installation ne se trouve pas à la racine du CD-ROM fourni aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="ae2b9-137">Vous devez définir la propriété [**MEDIAPACKAGEPATH**](mediapackagepath.md) dans ce cas sur le chemin d’accès au package d’installation.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="ae2b9-138">Le nom du volume dans la [table des médias](media-table.md) du fichier. msi doit correspondre au nom du volume du CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="ae2b9-139">Dans ce cas, suivez cet exemple.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-139">In this case follow this example.</span></span>

<span data-ttu-id="ae2b9-140">**Msiexec/I C : \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 disablerollback = 1 MEDIAPACKAGEPATH = c : \\ TempImage \\package.msi ROOTDRIVE = c :\\**</span><span class="sxs-lookup"><span data-stu-id="ae2b9-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2b9-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae2b9-141">Requirements</span></span>



| <span data-ttu-id="ae2b9-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae2b9-142">Requirement</span></span> | <span data-ttu-id="ae2b9-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae2b9-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2b9-144">Version</span><span class="sxs-lookup"><span data-stu-id="ae2b9-144">Version</span></span><br/> | <span data-ttu-id="ae2b9-145">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae2b9-146">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae2b9-147">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae2b9-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ae2b9-148">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2b9-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae2b9-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae2b9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2b9-150">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae2b9-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




