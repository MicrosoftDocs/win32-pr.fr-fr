---
description: Décrit la cohérence des lectures validées, l’isolation de lecture validée et les concepts de verrouillage transactionnel dans NTFS transactionnel.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Concepts de base de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320105"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="ec6df-103">Concepts de base de TxF</span><span class="sxs-lookup"><span data-stu-id="ec6df-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="ec6df-104">Isolation de lecture</span><span class="sxs-lookup"><span data-stu-id="ec6df-104">Read Isolation</span></span>

<span data-ttu-id="ec6df-105">NTFS transactionnel (TxF) fournit une cohérence en lecture validée.</span><span class="sxs-lookup"><span data-stu-id="ec6df-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="ec6df-106">Un [*rédacteur transactionnel*](glossary.md) fait référence à un descripteur de fichier transactionnel ouvert avec une autorisation qui ne fait pas partie d’un accès en lecture générique, mais qui fait partie d’un accès en écriture générique.</span><span class="sxs-lookup"><span data-stu-id="ec6df-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="ec6df-107">Un *rédacteur transactionnel* affiche la version la plus récente d’un fichier qui comprend toutes les modifications apportées par la même transaction.</span><span class="sxs-lookup"><span data-stu-id="ec6df-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="ec6df-108">Il ne peut y avoir qu’un seul Writer traité par fichier.</span><span class="sxs-lookup"><span data-stu-id="ec6df-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="ec6df-109">Les rédacteurs non transactionnels sont toujours bloqués par un rédacteur transactionnel, même si le fichier est ouvert avec des autorisations en écriture partagée.</span><span class="sxs-lookup"><span data-stu-id="ec6df-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="ec6df-110">Un [*lecteur transactionnel*](glossary.md) fait référence à un descripteur de fichier transactionnel ouvert avec une autorisation qui fait partie de l’accès en lecture générique, mais qui ne fait pas partie d’un accès en écriture générique.</span><span class="sxs-lookup"><span data-stu-id="ec6df-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="ec6df-111">Un *lecteur traité* affiche une version validée du fichier qui existait au moment où le descripteur de fichier a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="ec6df-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="ec6df-112">Le lecteur traité est isolé des effets des enregistreurs traités.</span><span class="sxs-lookup"><span data-stu-id="ec6df-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="ec6df-113">Cela fournit une vue cohérente du fichier uniquement pendant la durée de vie du descripteur de fichier et bloque les enregistreurs non transactionnels.</span><span class="sxs-lookup"><span data-stu-id="ec6df-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="ec6df-114">Lorsqu’un descripteur a été ouvert en vue d’une modification avec la fonction [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , toutes les ouvertures suivantes du fichier au sein de cette transaction, qu’il soit en lecture seule ou non, sont converties par le système en rédacteur transactionnel à des fins d’isolation et d’autres sémantiques transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="ec6df-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="ec6df-115">Cela signifie que, quand un handle est ouvert pour l’accès en lecture seule, le handle ne reçoit pas de vue du fichier avant le début de la transaction ; elle reçoit la vue de la transaction active du fichier.</span><span class="sxs-lookup"><span data-stu-id="ec6df-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="ec6df-116">Un descripteur de fichier non transactionnel ne voit pas les modifications apportées dans une transaction tant que la transaction n’est pas validée.</span><span class="sxs-lookup"><span data-stu-id="ec6df-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="ec6df-117">Le descripteur de fichier non transactionnel reçoit une vue isolée qui est similaire à un lecteur traité, mais contrairement à un lecteur traité, il reçoit la mise à jour du fichier lorsqu’un rédacteur transactionnel valide la transaction.</span><span class="sxs-lookup"><span data-stu-id="ec6df-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="ec6df-118">Niveaux d’isolation</span><span class="sxs-lookup"><span data-stu-id="ec6df-118">Isolation Levels</span></span>

<span data-ttu-id="ec6df-119">TxF offre une isolation en lecture validée.</span><span class="sxs-lookup"><span data-stu-id="ec6df-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="ec6df-120">Cela signifie que les mises à jour de fichiers ne sont pas visibles en dehors de la transaction.</span><span class="sxs-lookup"><span data-stu-id="ec6df-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="ec6df-121">En outre, si un fichier est ouvert plusieurs fois lors de la lecture de fichiers dans la transaction, vous pouvez voir des résultats différents avec chaque ouverture suivante.</span><span class="sxs-lookup"><span data-stu-id="ec6df-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="ec6df-122">Les fichiers qui étaient disponibles lors de leur première accès peuvent ne pas être disponibles (car ils ont été supprimés), ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="ec6df-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="ec6df-123">Verrouillage transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-123">Transactional Locking</span></span>

<span data-ttu-id="ec6df-124">La création d’un rédacteur transactionnel sur un fichier verrouille de façon *transactionnelle* le fichier.</span><span class="sxs-lookup"><span data-stu-id="ec6df-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="ec6df-125">Une fois qu’un fichier est verrouillé par une transaction, les autres opérations du système de fichiers externes à la transaction de verrouillage qui tentent de modifier le fichier verrouillé de manière transactionnelle échouent avec une **\_ \_ violation de partage des erreurs** ou un **\_ \_ conflit transactionnel d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="ec6df-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="ec6df-126">Le tableau suivant résume le verrouillage transactionnel.</span><span class="sxs-lookup"><span data-stu-id="ec6df-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="ec6df-127">Fichier actuellement ouvert par</span><span class="sxs-lookup"><span data-stu-id="ec6df-127">File currently opened by</span></span>

<span data-ttu-id="ec6df-128">Fichier ouvert tenté par</span><span class="sxs-lookup"><span data-stu-id="ec6df-128">File open attempted by</span></span>

<span data-ttu-id="ec6df-129">Transacted</span><span class="sxs-lookup"><span data-stu-id="ec6df-129">Transacted</span></span>

<span data-ttu-id="ec6df-130">Non transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-130">Non-Transacted</span></span>

<span data-ttu-id="ec6df-131">Lecteur</span><span class="sxs-lookup"><span data-stu-id="ec6df-131">Reader</span></span>

<span data-ttu-id="ec6df-132">Lecteur/enregistreur</span><span class="sxs-lookup"><span data-stu-id="ec6df-132">Reader/Writer</span></span>

<span data-ttu-id="ec6df-133">Lecteur</span><span class="sxs-lookup"><span data-stu-id="ec6df-133">Reader</span></span>

<span data-ttu-id="ec6df-134">Lecteur/enregistreur</span><span class="sxs-lookup"><span data-stu-id="ec6df-134">Reader/Writer</span></span>

<span data-ttu-id="ec6df-135">Lecteur transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-135">Transacted Reader</span></span>

<span data-ttu-id="ec6df-136">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-136">Yes</span></span>

<span data-ttu-id="ec6df-137">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-137">Yes</span></span>

<span data-ttu-id="ec6df-138">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-138">Yes</span></span>

<span data-ttu-id="ec6df-139">Non 2</span><span class="sxs-lookup"><span data-stu-id="ec6df-139">No2</span></span>

<span data-ttu-id="ec6df-140">Lecteur/enregistreur transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="ec6df-141">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-141">Yes</span></span>

<span data-ttu-id="ec6df-142">Non 2</span><span class="sxs-lookup"><span data-stu-id="ec6df-142">No2</span></span>

<span data-ttu-id="ec6df-143">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-143">Yes</span></span>

<span data-ttu-id="ec6df-144">Non 2</span><span class="sxs-lookup"><span data-stu-id="ec6df-144">No2</span></span>

<span data-ttu-id="ec6df-145">Lecteur non transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-145">Non-Transacted Reader</span></span>

<span data-ttu-id="ec6df-146">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-146">Yes</span></span>

<span data-ttu-id="ec6df-147">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-147">Yes</span></span>

<span data-ttu-id="ec6df-148">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-148">Yes</span></span>

<span data-ttu-id="ec6df-149">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-149">Yes</span></span>

<span data-ttu-id="ec6df-150">Lecteur/enregistreur non transactionnel</span><span class="sxs-lookup"><span data-stu-id="ec6df-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="ec6df-151">Non1</span><span class="sxs-lookup"><span data-stu-id="ec6df-151">No1</span></span>

<span data-ttu-id="ec6df-152">Non1</span><span class="sxs-lookup"><span data-stu-id="ec6df-152">No1</span></span>

<span data-ttu-id="ec6df-153">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-153">Yes</span></span>

<span data-ttu-id="ec6df-154">Oui</span><span class="sxs-lookup"><span data-stu-id="ec6df-154">Yes</span></span>

1. <span data-ttu-id="ec6df-155">Échec avec **\_ \_ conflit transactionnel d’erreur**</span><span class="sxs-lookup"><span data-stu-id="ec6df-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="ec6df-156">2. échec avec **\_ \_ violation de partage d’erreurs**</span><span class="sxs-lookup"><span data-stu-id="ec6df-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="ec6df-157">Si vous ouvrez un flux nommé pour une modification qui utilise une transaction, la totalité du fichier doit être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="ec6df-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="ec6df-158">En plus du verrouillage transactionnel, les règles de partage de fichiers NTFS standard s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="ec6df-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="ec6df-159">Vous devez prendre en compte les deux modes de partage de fichiers suivants en parallèle :</span><span class="sxs-lookup"><span data-stu-id="ec6df-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="ec6df-160">Mode de verrouillage transactionnel.</span><span class="sxs-lookup"><span data-stu-id="ec6df-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="ec6df-161">Modes de partage de fichiers normaux.</span><span class="sxs-lookup"><span data-stu-id="ec6df-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="ec6df-162">Quel que soit le mode le plus restrictif, c’est celui qui s’applique.</span><span class="sxs-lookup"><span data-stu-id="ec6df-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




