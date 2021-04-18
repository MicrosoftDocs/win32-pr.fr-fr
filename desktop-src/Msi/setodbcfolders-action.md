---
description: L’action SetODBCFolders recherche les pilotes ODBC existants sur le système et définit le répertoire cible de chaque nouveau pilote à l’emplacement d’un pilote existant.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Action SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515977"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="84e40-103">Action SetODBCFolders</span><span class="sxs-lookup"><span data-stu-id="84e40-103">SetODBCFolders Action</span></span>

<span data-ttu-id="84e40-104">L’action SetODBCFolders recherche les pilotes ODBC existants sur le système et définit le répertoire cible de chaque nouveau pilote à l’emplacement d’un pilote existant.</span><span class="sxs-lookup"><span data-stu-id="84e40-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="84e40-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="84e40-105">Sequence Restrictions</span></span>

<span data-ttu-id="84e40-106">L’action SetODBCFolders doit venir après l' [action CostFinalize](costfinalize-action.md) et avant l' [action InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="84e40-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="84e40-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="84e40-107">ActionData Messages</span></span>



| <span data-ttu-id="84e40-108">Champ</span><span class="sxs-lookup"><span data-stu-id="84e40-108">Field</span></span> | <span data-ttu-id="84e40-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="84e40-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="84e40-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="84e40-110">\[1\]</span></span> | <span data-ttu-id="84e40-111">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="84e40-111">Driver description.</span></span> <span data-ttu-id="84e40-112">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="84e40-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="84e40-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="84e40-113">\[2\]</span></span> | <span data-ttu-id="84e40-114">Emplacement du dossier d’origine du nouveau pilote.</span><span class="sxs-lookup"><span data-stu-id="84e40-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="84e40-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="84e40-115">\[3\]</span></span> | <span data-ttu-id="84e40-116">Nouvel emplacement du dossier pour le nouveau pilote.</span><span class="sxs-lookup"><span data-stu-id="84e40-116">New folder location for the new driver.</span></span> <span data-ttu-id="84e40-117">Il s’agit de l’emplacement d’un pilote existant.</span><span class="sxs-lookup"><span data-stu-id="84e40-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="84e40-118">Notes</span><span class="sxs-lookup"><span data-stu-id="84e40-118">Remarks</span></span>

<span data-ttu-id="84e40-119">Cette action place un nouveau pilote dans le même répertoire que le pilote existant en cours de remplacement.</span><span class="sxs-lookup"><span data-stu-id="84e40-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="84e40-120">L’action SetODBCFolders utilise la [table Directory](directory-table.md) pour définir les emplacements des pilotes existants à remplacer.</span><span class="sxs-lookup"><span data-stu-id="84e40-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



