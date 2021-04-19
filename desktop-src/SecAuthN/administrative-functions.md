---
description: Les fonctions administratives suivantes permettent à un fournisseur de réseau de prendre des mesures spécifiques au réseau pour afficher et manipuler des répertoires spécifiques au réseau, en d’autres termes, des répertoires mappés à des protocoles autres que Windows.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Fonctions d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545025"
---
# <a name="administrative-functions"></a><span data-ttu-id="bd6ae-103">Fonctions d’administration</span><span class="sxs-lookup"><span data-stu-id="bd6ae-103">Administrative Functions</span></span>

<span data-ttu-id="bd6ae-104">Les fonctions administratives suivantes permettent à un fournisseur de réseau de prendre des mesures spécifiques au réseau pour afficher et manipuler des répertoires spécifiques au réseau, en d’autres termes, des répertoires mappés à des protocoles autres que Windows.</span><span class="sxs-lookup"><span data-stu-id="bd6ae-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="bd6ae-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="bd6ae-105">Function</span></span>                                         | <span data-ttu-id="bd6ae-106">Description</span><span class="sxs-lookup"><span data-stu-id="bd6ae-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd6ae-107">**NPGetDirectoryType**</span><span class="sxs-lookup"><span data-stu-id="bd6ae-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="bd6ae-108">Appelé par le gestionnaire de fichiers pour déterminer le type d’un répertoire réseau.</span><span class="sxs-lookup"><span data-stu-id="bd6ae-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="bd6ae-109">**NPDirectoryNotify**</span><span class="sxs-lookup"><span data-stu-id="bd6ae-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="bd6ae-110">Appelé par le gestionnaire de fichiers pour informer le fournisseur réseau des opérations d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="bd6ae-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="bd6ae-111">Cette fonction peut être utilisée pour effectuer un comportement spécial pour certains répertoires.</span><span class="sxs-lookup"><span data-stu-id="bd6ae-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



