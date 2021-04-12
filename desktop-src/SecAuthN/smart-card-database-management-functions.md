---
description: Gérez la base de données de la carte à puce, en mettant à jour la base de données à l’aide d’un contexte Resource Manager spécifié.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Fonctions de gestion de base de données de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319898"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="ae64b-103">Fonctions de gestion de base de données de carte à puce</span><span class="sxs-lookup"><span data-stu-id="ae64b-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="ae64b-104">Les fonctions suivantes gèrent la [*base de données des cartes à puce*](../secgloss/s-gly.md), en mettant à jour la base de données à l’aide d’un [*contexte Resource Manager*](../secgloss/r-gly.md)spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae64b-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="ae64b-105">La sécurité de la base de données est conservée en plaçant des restrictions d’accès sur la base de données, plutôt que d’ajouter des mécanismes de sécurité au [*sous-système de carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ae64b-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="ae64b-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ae64b-106">Topic</span></span>                                                            | <span data-ttu-id="ae64b-107">Description</span><span class="sxs-lookup"><span data-stu-id="ae64b-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae64b-108">**SCardAddReaderToGroup**</span><span class="sxs-lookup"><span data-stu-id="ae64b-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="ae64b-109">Ajoutez un [*lecteur*](../secgloss/r-gly.md) à un [*groupe de lecteurs*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ae64b-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="ae64b-110">**SCardForgetCardType**</span><span class="sxs-lookup"><span data-stu-id="ae64b-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="ae64b-111">Retirez une carte à puce du système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="ae64b-112">**SCardForgetReader**</span><span class="sxs-lookup"><span data-stu-id="ae64b-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="ae64b-113">Suppression d’un lecteur du système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="ae64b-114">**SCardForgetReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="ae64b-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="ae64b-115">Suppression d’un groupe de lecteurs du système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="ae64b-116">**SCardIntroduceCardType**</span><span class="sxs-lookup"><span data-stu-id="ae64b-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="ae64b-117">Introduisez une nouvelle carte pour le système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="ae64b-118">**SCardIntroduceReader**</span><span class="sxs-lookup"><span data-stu-id="ae64b-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="ae64b-119">Introduisez un nouveau lecteur sur le système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="ae64b-120">**SCardIntroduceReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="ae64b-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="ae64b-121">Introduisez un nouveau groupe de lecteurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="ae64b-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="ae64b-122">**SCardRemoveReaderFromGroup**</span><span class="sxs-lookup"><span data-stu-id="ae64b-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="ae64b-123">Suppression d’un lecteur d’un groupe de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="ae64b-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
