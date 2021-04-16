---
description: Si l’action InstallValidate détecte l’installation d’un fichier en cours d’utilisation, elle affiche la boîte de dialogue FilesInUse et enregistre les informations suivantes.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Journalisation des demandes de redémarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530232"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="1d172-103">Journalisation des demandes de redémarrage</span><span class="sxs-lookup"><span data-stu-id="1d172-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="1d172-104">Si l' [action InstallValidate](installvalidate-action.md) détecte l’installation d’un fichier en cours d’utilisation, elle affiche la [boîte de dialogue FilesInUse](filesinuse-dialog.md) et enregistre les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d172-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="1d172-105">Si le programme d’installation détecte qu’il va remplacer un fichier en cours d’utilisation, il enregistre les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d172-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="1d172-106">Le \[ jeton de nom de \] fichier peut en fait contenir un chemin d’accès à un fichier avec une extension. RBF.</span><span class="sxs-lookup"><span data-stu-id="1d172-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="1d172-107">Dans ce cas, le fichier. RBF est en fait le fichier d’origine journalisé par le message 1603, qui a été renommé en fichier. RBF.</span><span class="sxs-lookup"><span data-stu-id="1d172-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="1d172-108">Le fichier en cours d’utilisation est d’abord renommé avec une extension. RBF, puis supprimé.</span><span class="sxs-lookup"><span data-stu-id="1d172-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="1d172-109">Pour obtenir plus d’informations sur la raison pour laquelle le programme d’installation tente de remplacer ce fichier particulier, vous pouvez utiliser l’option de journalisation détaillée.</span><span class="sxs-lookup"><span data-stu-id="1d172-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="1d172-110">Utilisez la \_ valeur de commentaires INSTALLLOGMODE dans un appel à [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou utilisez l’option de sortie verbose des [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="1d172-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="1d172-111">Les informations suivantes sont consignées dans le journal.</span><span class="sxs-lookup"><span data-stu-id="1d172-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="1d172-112">Le journal inclut un message tel que « le fichier existant est une version antérieure » ou « le fichier existant est endommagé (somme de contrôle non valide) »</span><span class="sxs-lookup"><span data-stu-id="1d172-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



