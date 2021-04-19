---
description: L’action CreateFolders crée des dossiers vides pour les composants qui sont configurés pour être installés.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Action CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523707"
---
# <a name="createfolders-action"></a><span data-ttu-id="54ccc-103">Action CreateFolders</span><span class="sxs-lookup"><span data-stu-id="54ccc-103">CreateFolders Action</span></span>

<span data-ttu-id="54ccc-104">L’action CreateFolders crée des dossiers vides pour les composants qui sont configurés pour être installés.</span><span class="sxs-lookup"><span data-stu-id="54ccc-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="54ccc-105">Le programme d’installation crée des dossiers pour les composants qui s’exécutent localement et qui s’exécutent à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="54ccc-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="54ccc-106">Les dossiers nouvellement créés sont inscrits avec l’identificateur de composant approprié.</span><span class="sxs-lookup"><span data-stu-id="54ccc-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="54ccc-107">L’action CreateFolders interroge la [table CreateFolder](createfolder-table.md) et la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="54ccc-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="54ccc-108">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="54ccc-108">Sequence Restrictions</span></span>

<span data-ttu-id="54ccc-109">L’action CreateFolders doit être exécutée avant l’action [InstallFiles](installfiles-action.md) ou avant toute action qui ajoute des fichiers aux dossiers.</span><span class="sxs-lookup"><span data-stu-id="54ccc-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="54ccc-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="54ccc-110">ActionData Messages</span></span>



| <span data-ttu-id="54ccc-111">Champ</span><span class="sxs-lookup"><span data-stu-id="54ccc-111">Field</span></span> | <span data-ttu-id="54ccc-112">Description de la description des données d’action</span><span class="sxs-lookup"><span data-stu-id="54ccc-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="54ccc-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="54ccc-113">\[1\]</span></span> | <span data-ttu-id="54ccc-114">Identificateur de répertoire du dossier.</span><span class="sxs-lookup"><span data-stu-id="54ccc-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="54ccc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="54ccc-115">Remarks</span></span>

<span data-ttu-id="54ccc-116">Le programme d’installation ne supprime pas automatiquement les dossiers créés par l’action CreateFolders pendant la désinstallation de l’application.</span><span class="sxs-lookup"><span data-stu-id="54ccc-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="54ccc-117">Le programme d’installation supprime uniquement les dossiers si l' [action RemoveFolders](removefolders-action.md) est incluse dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="54ccc-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



