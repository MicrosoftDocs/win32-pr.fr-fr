---
description: Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d’enregistrement d’HOMOLOGUe \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestion des enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544973"
---
# <a name="record-management"></a><span data-ttu-id="9de05-103">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="9de05-103">Record Management</span></span>

<span data-ttu-id="9de05-104">Pour gérer les enregistrements, vous pouvez utiliser des informations stockées dans des structures d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="9de05-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="9de05-105">Lorsque des enregistrements sont créés, mis à jour ou supprimés, les modifications apportées à un graphique sont répliquées sur tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="9de05-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="9de05-106">Le tableau suivant répertorie les règles de mise à jour et d’actualisation automatique des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="9de05-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="9de05-107">Tâche de gestion</span><span class="sxs-lookup"><span data-stu-id="9de05-107">Management Task</span></span>     | <span data-ttu-id="9de05-108">Règle</span><span class="sxs-lookup"><span data-stu-id="9de05-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de05-109">Mise à jour d'un enregistrement</span><span class="sxs-lookup"><span data-stu-id="9de05-109">Updating a record</span></span>   | <span data-ttu-id="9de05-110">Conservez la même heure d’expiration ou augmentez-la.</span><span class="sxs-lookup"><span data-stu-id="9de05-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="9de05-111">Vous ne pouvez pas réduire le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="9de05-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="9de05-112">Actualisation d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="9de05-112">Refreshing a record</span></span> | <span data-ttu-id="9de05-113">Utilisez l’indicateur d’actualisation automatique de l' [**\_ indicateur d’enregistrement \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) pour actualiser automatiquement un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9de05-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="9de05-114">Utilisez cet indicateur uniquement lorsque le nœud qui publie un enregistrement est en ligne.</span><span class="sxs-lookup"><span data-stu-id="9de05-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="9de05-115">Dans le cas contraire, n’utilisez pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="9de05-115">Otherwise, do not use this flag.</span></span> |



 

 

 



