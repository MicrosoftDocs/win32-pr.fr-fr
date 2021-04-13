---
description: Le NTFS transactionnel (TxF) intègre des transactions dans le système de fichiers NTFS, ce qui permet aux développeurs d’applications et aux administrateurs de gérer plus facilement les erreurs et de préserver l’intégrité des données.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: À propos du NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318433"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="5e37d-103">À propos du NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-103">About Transactional NTFS</span></span>

<span data-ttu-id="5e37d-104">\[Microsoft recommande vivement aux développeurs d’utiliser d’autres moyens pour répondre aux besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="5e37d-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="5e37d-105">De nombreux scénarios pour lesquels TxF a été développé peuvent être obtenus à l’aide de techniques plus simples et plus facilement disponibles.</span><span class="sxs-lookup"><span data-stu-id="5e37d-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="5e37d-106">En outre, TxF peut ne pas être disponible dans les versions futures de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5e37d-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="5e37d-107">Pour plus d’informations et pour obtenir des alternatives à TxF, consultez [alternatives à l’utilisation de NTFS transactionnel](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="5e37d-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="5e37d-108">Le NTFS transactionnel (TxF) intègre des transactions dans le système de fichiers NTFS, ce qui permet aux développeurs d’applications et aux administrateurs de gérer plus facilement les erreurs et de préserver l’intégrité des données.</span><span class="sxs-lookup"><span data-stu-id="5e37d-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="5e37d-109">TxF peut participer aux transactions distribuées que les coordonnées [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , ce qui vous permet d’utiliser TxF pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5e37d-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="5e37d-110">Transactions qui s’étendent sur plusieurs magasins de données, par exemple une transaction unique pour les opérations de fichier et SQL</span><span class="sxs-lookup"><span data-stu-id="5e37d-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="5e37d-111">Transactions qui s’étendent sur plusieurs ordinateurs, par exemple, une seule transaction pour les mises à jour de fichiers sur plusieurs ordinateurs</span><span class="sxs-lookup"><span data-stu-id="5e37d-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e37d-112">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5e37d-112">In this section</span></span>



| <span data-ttu-id="5e37d-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5e37d-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="5e37d-114">Description</span><span class="sxs-lookup"><span data-stu-id="5e37d-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e37d-115">Quand utiliser le NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="5e37d-116">Utilisez le NTFS transactionnel pour maintenir l’intégrité des données.</span><span class="sxs-lookup"><span data-stu-id="5e37d-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="5e37d-117">Déploiement de NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="5e37d-118">Contrôle de la mise en cache dans le NTFS transactionnel.</span><span class="sxs-lookup"><span data-stu-id="5e37d-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="5e37d-119">Utilisation de NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="5e37d-120">Gestion des descripteurs de fichiers transactionnels dans NTFS transactionnel.</span><span class="sxs-lookup"><span data-stu-id="5e37d-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="5e37d-121">Concepts de base de TxF</span><span class="sxs-lookup"><span data-stu-id="5e37d-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="5e37d-122">Décrit la cohérence des lectures validées, l’isolation de lecture validée et les concepts de verrouillage transactionnel dans NTFS transactionnel.</span><span class="sxs-lookup"><span data-stu-id="5e37d-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="5e37d-123">Considérations relatives à la programmation pour NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="5e37d-124">Décrit les différentes considérations en matière de programmation pour le NTFS transactionnel.</span><span class="sxs-lookup"><span data-stu-id="5e37d-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="5e37d-125">Considérations relatives aux performances pour le NTFS transactionnel</span><span class="sxs-lookup"><span data-stu-id="5e37d-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="5e37d-126">Recommandations pour les transactions de système de fichiers optimales.</span><span class="sxs-lookup"><span data-stu-id="5e37d-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

