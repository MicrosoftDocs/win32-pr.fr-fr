---
description: Le programme FhManagew.exe supprime les versions de fichiers qui dépassent un âge spécifié de l’appareil cible de l’historique des fichiers actuellement attribué.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483241"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="a0051-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="a0051-103">FhManagew.exe</span></span>

<span data-ttu-id="a0051-104">Le programme FhManagew.exe supprime les versions de fichiers qui dépassent un âge spécifié de l’appareil cible de l’historique des fichiers actuellement attribué.</span><span class="sxs-lookup"><span data-stu-id="a0051-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="a0051-105">Ce programme est disponible dans Windows 8 et Windows Server 2012 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a0051-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="a0051-106">Pour exécuter ce programme, accédez au menu **Démarrer** , cliquez sur **exécuter**, puis tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="a0051-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="a0051-107">**FhManagew.exe-âge de nettoyage** </span><span class="sxs-lookup"><span data-stu-id="a0051-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0051-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0051-108">Parameter</span></span></th>
<th><span data-ttu-id="a0051-109">Description</span><span class="sxs-lookup"><span data-stu-id="a0051-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0051-110"><span id="age"></span><span id="AGE"></span><em>vieillissement</em></span><span class="sxs-lookup"><span data-stu-id="a0051-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="a0051-111">Ce paramètre spécifie l’âge minimal, en jours, des versions de fichiers qui peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="a0051-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="a0051-112">Une version de fichier est supprimée si les deux conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="a0051-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="a0051-113">La version du fichier est antérieure à l’ancienneté spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a0051-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="a0051-114">Le fichier n’est plus inclus dans l’étendue de protection ou il existe une version plus récente du même fichier sur l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="a0051-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="a0051-115">Si le paramètre <em>Age</em> a la valeur zéro, toutes les versions de fichier sont supprimées, à l’exception de la version la plus récente de chaque fichier actuellement présent dans l’étendue de protection.</span><span class="sxs-lookup"><span data-stu-id="a0051-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0051-116">Pour supprimer toutes les sorties de ce programme, utilisez l’option de ligne de commande **Quiet** comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0051-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="a0051-117">**FhManagew.exe-nettoyer** *Age* **-Quiet**</span><span class="sxs-lookup"><span data-stu-id="a0051-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="a0051-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0051-118">Examples</span></span>



| <span data-ttu-id="a0051-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0051-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="a0051-120">Description</span><span class="sxs-lookup"><span data-stu-id="a0051-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0051-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-nettoyage 30**</span><span class="sxs-lookup"><span data-stu-id="a0051-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="a0051-122">Supprimer toutes les versions de fichiers datant de plus d’un mois.</span><span class="sxs-lookup"><span data-stu-id="a0051-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="a0051-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-quiet**</span><span class="sxs-lookup"><span data-stu-id="a0051-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="a0051-124">Supprimer toutes les versions de fichiers datant de plus d’un an et supprimer toutes les sorties.</span><span class="sxs-lookup"><span data-stu-id="a0051-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




