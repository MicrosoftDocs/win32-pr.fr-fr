---
description: Les administrateurs peuvent contrôler la quantité de données que chaque utilisateur peut stocker sur un volume de système de fichiers NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gestion des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534101"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="1b53f-103">Gestion des quotas de disque</span><span class="sxs-lookup"><span data-stu-id="1b53f-103">Managing Disk Quotas</span></span>

<span data-ttu-id="1b53f-104">Le système de fichiers NTFS prend en charge les *quotas de disque*, ce qui permet aux administrateurs de contrôler la quantité de données que chaque utilisateur peut stocker sur un volume de système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="1b53f-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="1b53f-105">Les administrateurs peuvent éventuellement configurer le système pour qu’il journalise un événement lorsque les utilisateurs sont proches de leur quota et pour refuser de l’espace disque aux utilisateurs qui dépassent leur quota.</span><span class="sxs-lookup"><span data-stu-id="1b53f-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="1b53f-106">Les administrateurs peuvent également générer des rapports et utiliser l’observateur d’événements pour suivre les problèmes de quota.</span><span class="sxs-lookup"><span data-stu-id="1b53f-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="1b53f-107">Vous pouvez déterminer si un système de fichiers prend en charge les quotas de disque en appelant la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et en examinant l’indicateur de bit **quotas de \_ volume \_ de fichier** .</span><span class="sxs-lookup"><span data-stu-id="1b53f-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b53f-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1b53f-108">In this section</span></span>



| <span data-ttu-id="1b53f-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1b53f-109">Topic</span></span>                                                                                                   | <span data-ttu-id="1b53f-110">Description</span><span class="sxs-lookup"><span data-stu-id="1b53f-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b53f-111">Administration au niveau de l’utilisateur des quotas de disque</span><span class="sxs-lookup"><span data-stu-id="1b53f-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="1b53f-112">Comment obtenir davantage d’espace disque disponible après avoir dépassé le quota alloué.</span><span class="sxs-lookup"><span data-stu-id="1b53f-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="1b53f-113">Administration au niveau du système des quotas de disque</span><span class="sxs-lookup"><span data-stu-id="1b53f-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="1b53f-114">L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume.</span><span class="sxs-lookup"><span data-stu-id="1b53f-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="1b53f-115">L’administrateur peut également définir des quotas par défaut pour le volume.</span><span class="sxs-lookup"><span data-stu-id="1b53f-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="1b53f-116">Limites de quota de disque</span><span class="sxs-lookup"><span data-stu-id="1b53f-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="1b53f-117">Décrit deux types de limites de quota de disque et la mesure des limites de quota de disque.</span><span class="sxs-lookup"><span data-stu-id="1b53f-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="1b53f-118">Interfaces de quota de disque</span><span class="sxs-lookup"><span data-stu-id="1b53f-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="1b53f-119">Interfaces utilisées avec les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="1b53f-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




