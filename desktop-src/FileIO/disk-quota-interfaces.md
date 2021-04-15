---
description: Interfaces utilisées avec les quotas de disque.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de quota de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485624"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="59df0-103">Interfaces de quota de disque</span><span class="sxs-lookup"><span data-stu-id="59df0-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="59df0-104">Les interfaces suivantes sont utilisées avec les quotas de disque.</span><span class="sxs-lookup"><span data-stu-id="59df0-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="59df0-105">Interface</span><span class="sxs-lookup"><span data-stu-id="59df0-105">Interface</span></span>                                          | <span data-ttu-id="59df0-106">Description</span><span class="sxs-lookup"><span data-stu-id="59df0-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59df0-107">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="59df0-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="59df0-108">Contrôle les fonctionnalités de quota de disque d’un volume de système de fichiers NTFS unique.</span><span class="sxs-lookup"><span data-stu-id="59df0-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="59df0-109">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="59df0-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="59df0-110">Reçoit des notifications d’événements liés au quota.</span><span class="sxs-lookup"><span data-stu-id="59df0-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="59df0-111">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="59df0-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="59df0-112">Représente une entrée de quota d’utilisateur unique dans le fichier d’informations de quota de volume.</span><span class="sxs-lookup"><span data-stu-id="59df0-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="59df0-113">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="59df0-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="59df0-114">Ajoute plusieurs objets utilisateur de quota à un conteneur qui est ensuite envoyé pour la mise à jour en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="59df0-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="59df0-115">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="59df0-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="59df0-116">Énumère les entrées de quota utilisateur sur le volume.</span><span class="sxs-lookup"><span data-stu-id="59df0-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

