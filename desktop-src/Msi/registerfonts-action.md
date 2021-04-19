---
description: L’action RegisterFonts inscrit les polices installées auprès du système. Cette action mappe le nom de police dans la colonne FontTitle de la table de polices au chemin d’accès du fichier de polices installé.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Action RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518239"
---
# <a name="registerfonts-action"></a><span data-ttu-id="75826-104">Action RegisterFonts</span><span class="sxs-lookup"><span data-stu-id="75826-104">RegisterFonts Action</span></span>

<span data-ttu-id="75826-105">L’action RegisterFonts inscrit les polices installées auprès du système.</span><span class="sxs-lookup"><span data-stu-id="75826-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="75826-106">Cette action mappe le nom de police dans la colonne FontTitle de la [table de polices](font-table.md) au chemin d’accès du fichier de polices installé.</span><span class="sxs-lookup"><span data-stu-id="75826-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="75826-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="75826-107">Sequence Restrictions</span></span>

<span data-ttu-id="75826-108">L’action [InstallFiles](installfiles-action.md) doit être appelée avant d’appeler l’action RegisterFonts.</span><span class="sxs-lookup"><span data-stu-id="75826-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="75826-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="75826-109">ActionData Messages</span></span>



| <span data-ttu-id="75826-110">Champ</span><span class="sxs-lookup"><span data-stu-id="75826-110">Field</span></span> | <span data-ttu-id="75826-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="75826-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="75826-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="75826-112">\[1\]</span></span> | <span data-ttu-id="75826-113">Fichier de police.</span><span class="sxs-lookup"><span data-stu-id="75826-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="75826-114">Notes</span><span class="sxs-lookup"><span data-stu-id="75826-114">Remarks</span></span>

<span data-ttu-id="75826-115">L’action RegisterFonts est exécutée si le fichier spécifié dans la \_ colonne fichier de la [table de polices](font-table.md) appartient à un composant en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="75826-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



