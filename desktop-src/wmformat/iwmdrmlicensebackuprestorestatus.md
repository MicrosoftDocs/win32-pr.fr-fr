---
title: Interface IWMDRMLicenseBackupRestoreStatus
description: L’interface IWMDRMLicenseBackupRestoreStatus fournit une méthode permettant de récupérer des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence. Cette interface est fournie avec les événements de progression générés pendant les opérations de sauvegarde et de restauration de la licence.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Format Windows Media de l’interface IWMDRMLicenseBackupRestoreStatus
- Interface IWMDRMLicenseBackupRestoreStatus format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315995"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="7fa9e-105">Interface IWMDRMLicenseBackupRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="7fa9e-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="7fa9e-106">L’interface **IWMDRMLicenseBackupRestoreStatus** fournit une méthode permettant de récupérer des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="7fa9e-107">Cette interface est fournie avec les événements de progression générés pendant les opérations de sauvegarde et de restauration de la licence.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="7fa9e-108">Plusieurs événements **MEWMDRMLicenseBackupProgress** sont générés au cours d’une sauvegarde de licence, chacun d’entre eux disposant d’une instance de cette interface.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="7fa9e-109">Il en va de même pour les événements **MEWMDRMLicenseRestoreProgress** , générés lors de la restauration de la licence.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="7fa9e-110">Pour récupérer un pointeur vers une instance de l’interface **IWMDRMLicenseBackupRestoreStatus** , vous devez d’abord appeler la méthode **IMFMediaEvent :: GetValue** de l’événement Progress.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="7fa9e-111">La valeur récupérée à partir de l’événement est un pointeur vers l’interface **IUnknown** de l’objet qui implémente l’interface **IWMDRMLicenseBackupRestoreStatus** .</span><span class="sxs-lookup"><span data-stu-id="7fa9e-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="7fa9e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="7fa9e-112">Members</span></span>

<span data-ttu-id="7fa9e-113">L’interface **IWMDRMLicenseBackupRestoreStatus** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7fa9e-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7fa9e-114">**IWMDRMLicenseBackupRestoreStatus** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fa9e-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="7fa9e-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fa9e-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7fa9e-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7fa9e-116">Methods</span></span>

<span data-ttu-id="7fa9e-117">L’interface **IWMDRMLicenseBackupRestoreStatus** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="7fa9e-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="7fa9e-118">Method</span></span>                                                          | <span data-ttu-id="7fa9e-119">Description</span><span class="sxs-lookup"><span data-stu-id="7fa9e-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fa9e-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa9e-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="7fa9e-121">Récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.</span><span class="sxs-lookup"><span data-stu-id="7fa9e-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7fa9e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fa9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa9e-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="7fa9e-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

