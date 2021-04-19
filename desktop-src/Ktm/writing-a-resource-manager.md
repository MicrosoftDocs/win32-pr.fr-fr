---
description: Si vous écrivez un service ou un composant et que vous devez utiliser des services transactionnels ou si vous devez surveiller l’état d’une transaction de noyau, vous devez créer un gestionnaire de ressources (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Écriture d’un Gestionnaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517802"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="47696-103">Écriture d’un Gestionnaire des ressources</span><span class="sxs-lookup"><span data-stu-id="47696-103">Writing a Resource Manager</span></span>

<span data-ttu-id="47696-104">Si vous écrivez un service ou un composant et que vous devez utiliser des services transactionnels ou si vous devez surveiller l’état d’une transaction de noyau, vous devez créer un gestionnaire de ressources (RM).</span><span class="sxs-lookup"><span data-stu-id="47696-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="47696-105">Pour écrire un gestionnaire de ressources, vous devez créer plusieurs objets de noyau.</span><span class="sxs-lookup"><span data-stu-id="47696-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="47696-106">Les objets utilisés par un RM sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="47696-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="47696-107">Objets du gestionnaire de transactions (TM)</span><span class="sxs-lookup"><span data-stu-id="47696-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="47696-108">Objets Gestionnaire des ressources</span><span class="sxs-lookup"><span data-stu-id="47696-108">Resource Manager objects</span></span>
-   <span data-ttu-id="47696-109">Objets d’inscription</span><span class="sxs-lookup"><span data-stu-id="47696-109">Enlistment objects</span></span>

<span data-ttu-id="47696-110">Tout d’abord, créez un objet TM.</span><span class="sxs-lookup"><span data-stu-id="47696-110">First, create a TM object.</span></span> <span data-ttu-id="47696-111">Il existe deux types de TMs :</span><span class="sxs-lookup"><span data-stu-id="47696-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="47696-112">Volatile : ces TMs n’ont pas de journal et ne peuvent pas récupérer leur état</span><span class="sxs-lookup"><span data-stu-id="47696-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="47696-113">Durable : ces TMs ont un journal</span><span class="sxs-lookup"><span data-stu-id="47696-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="47696-114">Pour créer un TM durable, vous devez créer un journal CLFS et appeler [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ou faire en sorte que KTM le crée pour vous.</span><span class="sxs-lookup"><span data-stu-id="47696-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="47696-115">Après la création d’un TM fiable, vous devez d’abord récupérer le TM en appelant [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span><span class="sxs-lookup"><span data-stu-id="47696-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="47696-116">Une fois le TM récupéré, il peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="47696-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="47696-117">Si vous récupérez une TM existante, tous les services RMs associés à ce TM commencent à recevoir des messages de récupération.</span><span class="sxs-lookup"><span data-stu-id="47696-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="47696-118">Pour plus d’informations, consultez traitement de la [récupération](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="47696-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="47696-119">Ensuite, vous créez un gestionnaire de ressources en appelant [**CreateResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) avec le handle TM.</span><span class="sxs-lookup"><span data-stu-id="47696-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="47696-120">Le RM peut être volatile ou durable.</span><span class="sxs-lookup"><span data-stu-id="47696-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="47696-121">Seul TMs durable peut être utilisé avec le RMs durable.</span><span class="sxs-lookup"><span data-stu-id="47696-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="47696-122">Lorsque vous travaillez de façon transactionnelle, vous vous inscrivez à la transaction en appelant [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)et en spécifiant les notifications à recevoir.</span><span class="sxs-lookup"><span data-stu-id="47696-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="47696-123">**Remarque**  Vous pouvez commencer à recevoir des notifications avant la fin de l’appel à [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .</span><span class="sxs-lookup"><span data-stu-id="47696-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="47696-124">Quand vous recevez une notification, appelez la fonction « Complete \* » appropriée quand une tâche associée au traitement de la notification est terminée.</span><span class="sxs-lookup"><span data-stu-id="47696-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="47696-125">Les fonctions complètes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="47696-125">The complete functions are:</span></span>

-   [<span data-ttu-id="47696-126">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="47696-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="47696-127">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="47696-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="47696-128">**PreprepareComplete**</span><span class="sxs-lookup"><span data-stu-id="47696-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="47696-129">Si, à un moment donné, un gestionnaire de ressources n’est pas en mesure de terminer le travail de la transaction, ou si la poursuite du rendu de votre application ne peut pas annuler le travail effectué dans la transaction, vous devez restaurer la transaction en appelant [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span><span class="sxs-lookup"><span data-stu-id="47696-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 



