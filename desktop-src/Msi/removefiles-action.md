---
description: L’action RemoveFiles supprime les fichiers précédemment installés par l’action InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Action RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544288"
---
# <a name="removefiles-action"></a><span data-ttu-id="79e76-103">Action RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="79e76-103">RemoveFiles Action</span></span>

<span data-ttu-id="79e76-104">L’action RemoveFiles supprime les fichiers précédemment installés par l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="79e76-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="79e76-105">Chacun de ces fichiers est contrôlé par un lien vers une entrée de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="79e76-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="79e76-106">Seuls les fichiers dont les composants sont résolus à l’état *msiInstallStateAbsent* ou *msiInstallStateLocal* si le composant est installé localement sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="79e76-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="79e76-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="79e76-107">Sequence Restrictions</span></span>

<span data-ttu-id="79e76-108">L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="79e76-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="79e76-109">Si une action [InstallFiles](installfiles-action.md) est utilisée, elle doit apparaître après RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="79e76-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="79e76-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="79e76-110">ActionData Messages</span></span>



| <span data-ttu-id="79e76-111">Champ</span><span class="sxs-lookup"><span data-stu-id="79e76-111">Field</span></span> | <span data-ttu-id="79e76-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="79e76-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="79e76-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="79e76-113">\[1\]</span></span> | <span data-ttu-id="79e76-114">Identificateur du fichier supprimé.</span><span class="sxs-lookup"><span data-stu-id="79e76-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="79e76-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="79e76-115">\[9\]</span></span> | <span data-ttu-id="79e76-116">Identificateur du répertoire contenant le fichier supprimé.</span><span class="sxs-lookup"><span data-stu-id="79e76-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="79e76-117">Notes</span><span class="sxs-lookup"><span data-stu-id="79e76-117">Remarks</span></span>

<span data-ttu-id="79e76-118">La table [RemoveFile](removefile-table.md) peut être omise de la base de données du programme d’installation s’il n’y a pas de fichiers divers à supprimer.</span><span class="sxs-lookup"><span data-stu-id="79e76-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="79e76-119">L’action RemoveFiles peut également supprimer les fichiers spécifiés par l’auteur qui ne sont pas installés par l’action InstallFiles.</span><span class="sxs-lookup"><span data-stu-id="79e76-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="79e76-120">Ces fichiers sont spécifiés dans la table [RemoveFile](removefile-table.md) .</span><span class="sxs-lookup"><span data-stu-id="79e76-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="79e76-121">Chacun de ces fichiers est contrôlé par un lien vers une entrée de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="79e76-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="79e76-122">Les fichiers dont les composants sont résolus en un état d’action actif (autrement dit, qui n’est pas à l’état désactivé ou null) sont supprimés si le fichier existe dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="79e76-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="79e76-123">La suppression des fichiers spécifiés dans la table RemoveFile est tentée lorsque le composant lié est installé pour la première fois, lors d’une réinstallation, puis à nouveau lorsque le composant lié est supprimé.</span><span class="sxs-lookup"><span data-stu-id="79e76-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="79e76-124">L’action RemoveFiles peut également supprimer des dossiers.</span><span class="sxs-lookup"><span data-stu-id="79e76-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="79e76-125">Un dossier vide est supprimé si la valeur de la colonne FileName de la table RemoveFile est null.</span><span class="sxs-lookup"><span data-stu-id="79e76-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="79e76-126">Lors de la suppression des fichiers installés précédemment, l’action RemoveFiles interroge les mêmes champs dans les mêmes tables que ceux interrogés par l’action [InstallFiles](installfiles-action.md) , à l’exception du fait que la [table multimédia](media-table.md) n’est pas utilisée par l’action RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="79e76-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="79e76-127">Le nom du fichier cible peut être spécifié dans le texte localisé dans la colonne FileName de la table RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="79e76-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



