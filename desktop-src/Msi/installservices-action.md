---
description: L’action InstallServices inscrit un service pour le système. Cette action interroge la table ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Action InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530906"
---
# <a name="installservices-action"></a><span data-ttu-id="81a4a-104">Action InstallServices</span><span class="sxs-lookup"><span data-stu-id="81a4a-104">InstallServices Action</span></span>

<span data-ttu-id="81a4a-105">L’action InstallServices inscrit un service pour le système.</span><span class="sxs-lookup"><span data-stu-id="81a4a-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="81a4a-106">Cette action interroge la [table ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="81a4a-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="81a4a-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="81a4a-107">Sequence Restrictions</span></span>

<span data-ttu-id="81a4a-108">L’action services doit être utilisée dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="81a4a-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="81a4a-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="81a4a-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="81a4a-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="81a4a-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="81a4a-111">L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="81a4a-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="81a4a-112">InstallServices</span><span class="sxs-lookup"><span data-stu-id="81a4a-112">InstallServices</span></span>

[<span data-ttu-id="81a4a-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="81a4a-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="81a4a-114">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="81a4a-114">ActionData Messages</span></span>

<span data-ttu-id="81a4a-115">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="81a4a-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a4a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="81a4a-116">Remarks</span></span>

<span data-ttu-id="81a4a-117">Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation d’installer des services ou que l’application fasse partie d’une installation gérée.</span><span class="sxs-lookup"><span data-stu-id="81a4a-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



