---
description: Héritage de transactions manuelles
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Héritage de transactions manuelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514923"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="b3a4a-103">Héritage de transactions manuelles</span><span class="sxs-lookup"><span data-stu-id="b3a4a-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="b3a4a-104">Si un objet avec une transaction BYOT dans son contexte crée un deuxième objet, l’objet en aval peut hériter de la transaction BYOT (si elle est configurée pour hériter des transactions).</span><span class="sxs-lookup"><span data-stu-id="b3a4a-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="b3a4a-105">Le premier objet créé à l’aide de la passerelle BYOT doit être configuré pour « exiger » ou « prendre en charge » les transactions.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="b3a4a-106">Les objets suivants dans l’activité peuvent être configurés en fonction des spécifications de l’application.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="b3a4a-107">Pour les transactions automatiques, le runtime COM+ ne tente pas de valider la transaction jusqu’à ce que l’objet racine indique qu’elle est prête (en appelant [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) avant de retourner un appel).</span><span class="sxs-lookup"><span data-stu-id="b3a4a-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="b3a4a-108">Les utilisateurs doivent savoir qu’une transaction BYOT peut être validée prématurément (dans le sens où le travail des objets enfants n’a pas été effectué), parce que la « racine » n’est pas exécutée dans l’environnement d’exécution COM+ et que la sémantique de validation n’est pas liée à la durée de vie de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="b3a4a-109">En général, l’utilisateur doit veiller à ne pas violer la limite de synchronisation de la transaction.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="b3a4a-110">Dans le cas contraire, les sémantiques de validation COM+ s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="b3a4a-111">COM+ ne tente pas de valider une transaction alors qu’un objet dans une limite de synchronisation est en cours d’appel.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="b3a4a-112">En outre, les objets peuvent indiquer leur cohérence à l’aide de [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span><span class="sxs-lookup"><span data-stu-id="b3a4a-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="b3a4a-113">Si une tentative est effectuée pour valider une transaction qui inclut le travail d’un objet appelé **DisableCommit**, la transaction est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



