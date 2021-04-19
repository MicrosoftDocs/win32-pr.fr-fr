---
description: Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle&\# 8212 ; Incremental, Differential et full&\# 8212 ; que VSS reconnaît, ainsi qu’une configuration de sauvegarde propre à VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurations de sauvegarde VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514618"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="cdcfb-103">Configurations de sauvegarde VSS</span><span class="sxs-lookup"><span data-stu-id="cdcfb-103">VSS Backup Configurations</span></span>

<span data-ttu-id="cdcfb-104">Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle (incrémentielle, différentielle et complète) dont VSS est conscient, ainsi qu’une configuration de sauvegarde propre à VSS.</span><span class="sxs-lookup"><span data-stu-id="cdcfb-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="cdcfb-105">Lors de la définition d’une configuration de sauvegarde, un demandeur et les rédacteurs sur un système indiquent comment les données seront écrites sur un dispositif de stockage, comment le mécanisme de cliché instantané sera déployé et quelles informations doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="cdcfb-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="cdcfb-106">L’interaction entre les enregistreurs et les demandeurs est déterminée par le type de sauvegarde qu’un demandeur souhaite exécuter et les genres (ou schémas) que chaque Writer peut prendre en charge :</span><span class="sxs-lookup"><span data-stu-id="cdcfb-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="cdcfb-107">État de sauvegarde VSS</span><span class="sxs-lookup"><span data-stu-id="cdcfb-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="cdcfb-108">Prise en charge du schéma de sauvegarde de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="cdcfb-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="cdcfb-109">Prise en charge des schémas au niveau du fichier</span><span class="sxs-lookup"><span data-stu-id="cdcfb-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



