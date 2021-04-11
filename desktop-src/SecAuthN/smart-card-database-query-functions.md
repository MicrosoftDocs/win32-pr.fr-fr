---
description: Interrogez la base de données de la carte à puce. Ils peuvent fournir une liste des cartes à puce fournies par un utilisateur spécifique, les interfaces et le fournisseur de services principal d’une carte spécifique, les groupes de lecteurs définis pour le système et les lecteurs au sein d’un ensemble de groupes de lecteurs.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Fonctions de requête de base de données de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209706"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="23039-104">Fonctions de requête de base de données de carte à puce</span><span class="sxs-lookup"><span data-stu-id="23039-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="23039-105">Les fonctions suivantes interrogent la [*base de données des cartes à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="23039-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="23039-106">Ils peuvent fournir une liste des cartes à puce fournies par un utilisateur spécifique, les interfaces et le [*fournisseur de services principal*](../secgloss/p-gly.md) d’une carte spécifique, les [*groupes de lecteurs*](../secgloss/r-gly.md) définis pour le système et les [*lecteurs*](../secgloss/r-gly.md) au sein d’un ensemble de groupes de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="23039-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="23039-107">Lorsque vous utilisez ces fonctions, vous pouvez interroger la base de données de carte à puce complète, ou vous pouvez affiner la recherche en définissant le [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="23039-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="23039-108">Le contexte du gestionnaire de ressources est défini en appelant [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) avant d’appeler une fonction de requête.</span><span class="sxs-lookup"><span data-stu-id="23039-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="23039-109">Sans un contexte spécifié, certaines informations peuvent toujours être inaccessibles en raison de restrictions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="23039-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="23039-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="23039-110">Topic</span></span>                                                  | <span data-ttu-id="23039-111">Description</span><span class="sxs-lookup"><span data-stu-id="23039-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23039-112">**SCardGetProviderId**</span><span class="sxs-lookup"><span data-stu-id="23039-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="23039-113">Récupérez l’identificateur (GUID) du [*fournisseur de services principal*](../secgloss/p-gly.md) pour la carte donnée.</span><span class="sxs-lookup"><span data-stu-id="23039-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="23039-114">**SCardListCards**</span><span class="sxs-lookup"><span data-stu-id="23039-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="23039-115">Récupérer une liste de cartes précédemment introduites dans le système par un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="23039-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="23039-116">**SCardListInterfaces**</span><span class="sxs-lookup"><span data-stu-id="23039-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="23039-117">Récupérez les identificateurs (GUID) des interfaces fournies par une carte donnée.</span><span class="sxs-lookup"><span data-stu-id="23039-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="23039-118">**SCardListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="23039-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="23039-119">Récupérez la liste des groupes de lecteurs qui ont été introduits précédemment dans le système.</span><span class="sxs-lookup"><span data-stu-id="23039-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="23039-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="23039-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="23039-121">Récupérez la liste des lecteurs dans un ensemble de groupes de lecteurs nommés.</span><span class="sxs-lookup"><span data-stu-id="23039-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
