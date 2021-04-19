---
description: L’action MsiConfigureServices configure un service pour le système. Cette action interroge les tables MsiServiceConfig et MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Action MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545181"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="5b69d-104">Action MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="5b69d-105">L’action MsiConfigureServices configure un service pour le système.</span><span class="sxs-lookup"><span data-stu-id="5b69d-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="5b69d-106">Cette action interroge les tables [MsiServiceConfig](msiserviceconfig-table.md) et [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5b69d-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="5b69d-107">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5b69d-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="5b69d-108">Cette action est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="5b69d-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5b69d-109">Les services Windows permettent d’effectuer automatiquement des actions prédéfinies en réponse à une défaillance dans un service.</span><span class="sxs-lookup"><span data-stu-id="5b69d-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="5b69d-110">Pour prendre en charge la configuration par programmation de ces **actions de récupération** en cas d’échec d’un service, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) a été ajouté à MSI dans la version MSI 5,0.</span><span class="sxs-lookup"><span data-stu-id="5b69d-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="5b69d-111">Toutefois, cette fonctionnalité ne fonctionne pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="5b69d-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="5b69d-112">Pour contourner ce problème, un développeur d’applications doit utiliser la fonctionnalité d' **action personnalisée** dans MSI pour exécuter **sc.exe** et définir les **options de récupération** de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="5b69d-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="5b69d-113">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="5b69d-113">Sequence Restrictions</span></span>

<span data-ttu-id="5b69d-114">Cette action standard doit être utilisée dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="5b69d-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="5b69d-115">StopServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="5b69d-116">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="5b69d-117">L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="5b69d-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="5b69d-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="5b69d-119">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-119">MsiConfigureServices</span></span>

[<span data-ttu-id="5b69d-120">StartServices</span><span class="sxs-lookup"><span data-stu-id="5b69d-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="5b69d-121">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="5b69d-121">ActionData Messages</span></span>

<span data-ttu-id="5b69d-122">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="5b69d-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b69d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5b69d-123">Remarks</span></span>

<span data-ttu-id="5b69d-124">Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation d’installer des services ou que l’application fasse partie d’une installation gérée.</span><span class="sxs-lookup"><span data-stu-id="5b69d-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



