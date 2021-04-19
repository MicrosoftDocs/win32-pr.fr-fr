---
description: L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Action UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535060"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="927e2-103">Action UnregisterFonts</span><span class="sxs-lookup"><span data-stu-id="927e2-103">UnregisterFonts Action</span></span>

<span data-ttu-id="927e2-104">L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.</span><span class="sxs-lookup"><span data-stu-id="927e2-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="927e2-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="927e2-105">Sequence Restrictions</span></span>

<span data-ttu-id="927e2-106">L’action [RemoveFiles](removefiles-action.md) doit être appelée après UnregisterFonts.</span><span class="sxs-lookup"><span data-stu-id="927e2-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="927e2-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="927e2-107">ActionData Messages</span></span>



| <span data-ttu-id="927e2-108">Champ</span><span class="sxs-lookup"><span data-stu-id="927e2-108">Field</span></span> | <span data-ttu-id="927e2-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="927e2-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="927e2-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="927e2-110">\[1\]</span></span> | <span data-ttu-id="927e2-111">Fichier de police.</span><span class="sxs-lookup"><span data-stu-id="927e2-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="927e2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="927e2-112">Remarks</span></span>

<span data-ttu-id="927e2-113">L’action UnregisterFonts est exécutée si le fichier spécifié dans la \_ colonne file de la [table font](font-table.md) appartient à un composant en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="927e2-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



