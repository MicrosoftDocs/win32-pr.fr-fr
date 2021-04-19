---
description: L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes. En outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Action RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540857"
---
# <a name="registerproduct-action"></a><span data-ttu-id="fe6c6-104">Action RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="fe6c6-104">RegisterProduct Action</span></span>

<span data-ttu-id="fe6c6-105">L’action RegisterProduct enregistre les informations sur le produit avec le programme d’installation et avec ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="fe6c6-106">En outre, cette action stocke le package de base de données Windows Installer sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="fe6c6-107">L’action RegisterProduct configure les contrôles affichés par l’ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="fe6c6-108">Pour plus d’informations, consultez Configuration de l' [Ajout/suppression de programmes avec Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="fe6c6-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fe6c6-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="fe6c6-109">Sequence Restrictions</span></span>

<span data-ttu-id="fe6c6-110">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fe6c6-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="fe6c6-111">ActionData Messages</span></span>



| <span data-ttu-id="fe6c6-112">Champ</span><span class="sxs-lookup"><span data-stu-id="fe6c6-112">Field</span></span> | <span data-ttu-id="fe6c6-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="fe6c6-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="fe6c6-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fe6c6-114">\[1\]</span></span> | <span data-ttu-id="fe6c6-115">Informations sur le produit inscrit.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fe6c6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fe6c6-116">Remarks</span></span>

<span data-ttu-id="fe6c6-117">L’action RegisterProduct n’est pas exécutée lors de l’installation sur un point d’installation d’administration.</span><span class="sxs-lookup"><span data-stu-id="fe6c6-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 



