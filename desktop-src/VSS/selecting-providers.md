---
description: Un demandeur doit sélectionner un fournisseur spécifique uniquement s’il contient des informations sur les fournisseurs disponibles.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Sélection des fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115139"
---
# <a name="selecting-providers"></a><span data-ttu-id="1b543-103">Sélection des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="1b543-103">Selecting Providers</span></span>

<span data-ttu-id="1b543-104">Un demandeur doit sélectionner un fournisseur spécifique uniquement s’il contient des informations sur les fournisseurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="1b543-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="1b543-105">Dans la mesure où cela n’est généralement pas le cas, il est recommandé qu’un demandeur fournisse \_ la valeur NULL comme ID de fournisseur à [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), ce qui permet au système de choisir un fournisseur selon l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="1b543-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="1b543-106">Si un fournisseur de matériel qui prend en charge le volume donné est disponible, il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b543-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="1b543-107">Si aucun fournisseur de matériel n’est disponible, si un fournisseur de logiciels spécifique au volume donné est disponible, il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b543-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="1b543-108">Si aucun fournisseur de matériel et aucun fournisseur de logiciels spécifique aux volumes n’est disponible, le fournisseur système est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b543-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="1b543-109">Toutefois, un demandeur peut obtenir des informations sur les fournisseurs disponibles à l’aide de [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="1b543-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="1b543-110">Avec ces informations, et seulement si l’application de sauvegarde a une bonne compréhension des différents fournisseurs, un demandeur peut fournir un ID de fournisseur valide à [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span><span class="sxs-lookup"><span data-stu-id="1b543-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="1b543-111">Notez que tous les volumes n’ont pas besoin d’avoir le même fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1b543-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



