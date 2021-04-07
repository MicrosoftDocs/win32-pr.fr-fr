---
description: Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre de Windows Vista ou Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Détection du remplacement des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759010"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="62ee2-103">Détection du remplacement des ressources</span><span class="sxs-lookup"><span data-stu-id="62ee2-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="62ee2-104">Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre de Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="62ee2-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="62ee2-105">WRP protège les fichiers, dossiers et clés de Registre sur Windows Vista ou Windows Server 2008 en détectant et en empêchant les tentatives de remplacement des ressources protégées.</span><span class="sxs-lookup"><span data-stu-id="62ee2-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="62ee2-106">Cette protection est basée sur une liste de contrôle d’accès discrétionnaire (DACL) et des listes de contrôle d’accès (ACL) Windows définies pour les ressources protégées.</span><span class="sxs-lookup"><span data-stu-id="62ee2-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="62ee2-107">L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="62ee2-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="62ee2-108">Les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des modules Windows.</span><span class="sxs-lookup"><span data-stu-id="62ee2-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="62ee2-109">Les applications tentant de modifier une ressource protégée par WRP ne changent jamais la ressource et peuvent recevoir un message d’erreur indiquant que l’accès à la ressource a été refusé.</span><span class="sxs-lookup"><span data-stu-id="62ee2-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="62ee2-110">Les applications et les programmes d’installation peuvent utiliser les fonctions [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) et [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) pour déterminer si un fichier ou une clé de Registre est protégé.</span><span class="sxs-lookup"><span data-stu-id="62ee2-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="62ee2-111">\* \* Windows Server 2003 et Windows XP : \* \*</span><span class="sxs-lookup"><span data-stu-id="62ee2-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="62ee2-112">La protection des fichiers Windows (WFP) protège les fichiers système en détectant les tentatives de remplacement des fichiers système protégés.</span><span class="sxs-lookup"><span data-stu-id="62ee2-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="62ee2-113">Cette protection est déclenchée lorsque WFP reçoit une notification de modification de répertoire pour un fichier dans un répertoire protégé.</span><span class="sxs-lookup"><span data-stu-id="62ee2-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="62ee2-114">Lorsque WFP reçoit cette notification, il détermine quel fichier a changé.</span><span class="sxs-lookup"><span data-stu-id="62ee2-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="62ee2-115">Si le fichier est protégé, WFP recherche la signature de fichier dans un fichier catalogue pour déterminer si le nouveau fichier est la version correcte.</span><span class="sxs-lookup"><span data-stu-id="62ee2-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="62ee2-116">Si la version du fichier n’est pas correcte, le système remplace le fichier par la version appropriée à partir du média de distribution ou du cache, selon que le fichier se trouve dans le cache ou non.</span><span class="sxs-lookup"><span data-stu-id="62ee2-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="62ee2-117">La plateforme WFP recherche le fichier approprié dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="62ee2-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="62ee2-118">Recherchez dans le répertoire du cache.</span><span class="sxs-lookup"><span data-stu-id="62ee2-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="62ee2-119">Recherchez le chemin d’installation réseau si le système a été installé à l’aide de l’installation réseau.</span><span class="sxs-lookup"><span data-stu-id="62ee2-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="62ee2-120">Recherchez sur un CD-ROM Windows si le système a été installé à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="62ee2-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="62ee2-121">Si la protection de code à distance ne peut pas trouver automatiquement le fichier aux deux premiers emplacements, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="62ee2-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![message WFP affiché lorsqu’un fichier est introuvable dans le répertoire du cache ou le chemin d’installation réseau](images/wfp-1.png)

<span data-ttu-id="62ee2-123">Si le système a été installé à l’aide d’un CD-ROM, WFP affiche le message suivant :</span><span class="sxs-lookup"><span data-stu-id="62ee2-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![message WFP affiché pour inviter l’utilisateur à insérer un CD-ROM Windows](images/wfp-2.png)

<span data-ttu-id="62ee2-125">Si un administrateur n’est pas connecté, WFP ne peut pas afficher l’une de ces boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="62ee2-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="62ee2-126">WFP affiche la boîte de dialogue lorsqu’un administrateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="62ee2-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="62ee2-127">La protection des fichiers journaux enregistre également la tentative de remplacement de fichier dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="62ee2-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="62ee2-128">Si l’administrateur a annulé la restauration du fichier approprié, WFP journalise l’annulation.</span><span class="sxs-lookup"><span data-stu-id="62ee2-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="62ee2-129">Récupération de la liste des fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="62ee2-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="62ee2-130">L’exemple suivant montre comment les applications et les programmes d’installation peuvent utiliser la fonction [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) pour obtenir la liste complète des fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="62ee2-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



