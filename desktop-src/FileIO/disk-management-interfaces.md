---
description: Interfaces utilisées dans la gestion des disques.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gestion des disques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209904"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="bed06-103">Interfaces de gestion des disques</span><span class="sxs-lookup"><span data-stu-id="bed06-103">Disk Management Interfaces</span></span>

<span data-ttu-id="bed06-104">Les interfaces suivantes sont utilisées dans gestion des disques.</span><span class="sxs-lookup"><span data-stu-id="bed06-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bed06-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bed06-105">In this section</span></span>



| <span data-ttu-id="bed06-106">Interface</span><span class="sxs-lookup"><span data-stu-id="bed06-106">Interface</span></span>                                                     | <span data-ttu-id="bed06-107">Description</span><span class="sxs-lookup"><span data-stu-id="bed06-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bed06-108">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="bed06-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="bed06-109">Contrôle les fonctionnalités de quota de disque d’un volume de système de fichiers NTFS unique.</span><span class="sxs-lookup"><span data-stu-id="bed06-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="bed06-110">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="bed06-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="bed06-111">Reçoit des notifications d’événements liés au quota.</span><span class="sxs-lookup"><span data-stu-id="bed06-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="bed06-112">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="bed06-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="bed06-113">Représente une entrée de quota d’utilisateur unique dans le fichier d’informations de quota de volume.</span><span class="sxs-lookup"><span data-stu-id="bed06-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="bed06-114">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="bed06-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="bed06-115">Ajoute plusieurs objets utilisateur de quota à un conteneur qui est ensuite envoyé pour la mise à jour en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="bed06-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="bed06-116">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="bed06-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="bed06-117">Énumère les entrées de quota utilisateur sur le volume.</span><span class="sxs-lookup"><span data-stu-id="bed06-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

