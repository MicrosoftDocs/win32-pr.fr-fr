---
title: Propriétés ITsSbTaskInfo
description: L’interface ITsSbTaskInfo expose les propriétés suivantes.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678389"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="6b871-103">Propriétés ITsSbTaskInfo</span><span class="sxs-lookup"><span data-stu-id="6b871-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="6b871-104">L’interface [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b871-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b871-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6b871-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6b871-106">**Propriété de contexte**</span><span class="sxs-lookup"><span data-stu-id="6b871-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="6b871-107">Récupère les octets de contexte associés à la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-108">**Propriété échéance**</span><span class="sxs-lookup"><span data-stu-id="6b871-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="6b871-109">Récupère l’heure à laquelle la tâche doit être lancée.</span><span class="sxs-lookup"><span data-stu-id="6b871-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="6b871-110">Cela permet de hiérarchiser les correctifs.</span><span class="sxs-lookup"><span data-stu-id="6b871-110">This is used to prioritize patches.</span></span> <span data-ttu-id="6b871-111">Le correctif avec l’échéance la plus proche sera initié en premier.</span><span class="sxs-lookup"><span data-stu-id="6b871-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-112">**EndTime, propriété**</span><span class="sxs-lookup"><span data-stu-id="6b871-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="6b871-113">Récupère la dernière heure à laquelle l’agent de tâche peut démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-114">**Propriété Identificateur**</span><span class="sxs-lookup"><span data-stu-id="6b871-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="6b871-115">Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-116">**propriété Label**</span><span class="sxs-lookup"><span data-stu-id="6b871-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="6b871-117">Récupère l’étiquette qui décrit l’objectif de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-118">**Propriété de plug-in**</span><span class="sxs-lookup"><span data-stu-id="6b871-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="6b871-119">Récupère le nom complet de l’agent de tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-120">**StartTime, propriété**</span><span class="sxs-lookup"><span data-stu-id="6b871-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="6b871-121">Récupère le moment où l’agent de tâche peut démarrer la tâche au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="6b871-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-122">**Status (propriété)**</span><span class="sxs-lookup"><span data-stu-id="6b871-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="6b871-123">Récupère une valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b871-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="6b871-124">**Propriété TargetId**</span><span class="sxs-lookup"><span data-stu-id="6b871-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="6b871-125">Récupère l’identificateur cible.</span><span class="sxs-lookup"><span data-stu-id="6b871-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




