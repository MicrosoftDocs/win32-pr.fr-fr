---
description: Terminologie utilisée pour décrire le NTFS transactionnel (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossaire TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210260"
---
# <a name="txf-glossary"></a><span data-ttu-id="87eb0-103">Glossaire TxF</span><span class="sxs-lookup"><span data-stu-id="87eb0-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="87eb0-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**sa**</span><span class="sxs-lookup"><span data-stu-id="87eb0-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="87eb0-105">La disponibilité signifie qu’un gestionnaire de ressources va abandonner les transactions même si cela rompt la cohérence afin que le système puisse continuer à effectuer de nouvelles tâches.</span><span class="sxs-lookup"><span data-stu-id="87eb0-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="87eb0-106">Le gestionnaire de ressources par défaut force la disponibilité sur le volume système.</span><span class="sxs-lookup"><span data-stu-id="87eb0-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="87eb0-107">Par exemple, si le journal des transactions est plein, l’espace du journal des transactions ne peut pas être ajouté, et une transaction plus ancienne qui serait abandonnée nécessite la remise d’un résultat à partir d’un gestionnaire de ressources supérieur pour qu’une transaction distribuée se termine, le gestionnaire de ressources n’attend pas le gestionnaire de transactions supérieur et abandonne cette transaction, même si cela peut entraîner une</span><span class="sxs-lookup"><span data-stu-id="87eb0-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="87eb0-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**cohérence**</span><span class="sxs-lookup"><span data-stu-id="87eb0-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="87eb0-109">La cohérence signifie qu’un gestionnaire de ressources va faire échouer de nouvelles transactions s’il ne peut pas avancer.</span><span class="sxs-lookup"><span data-stu-id="87eb0-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="87eb0-110">Par exemple, si le journal des transactions est plein, l’espace du journal des transactions ne peut pas être ajouté, et une transaction plus ancienne qui serait abandonnée nécessite la remise d’un résultat à partir d’un gestionnaire de ressources supérieur afin qu’une transaction distribuée se termine, le gestionnaire de ressources attendra ce résultat.</span><span class="sxs-lookup"><span data-stu-id="87eb0-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="87eb0-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span><span class="sxs-lookup"><span data-stu-id="87eb0-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="87eb0-112">Un miniversion est une version d’un fichier qu’un rédacteur transactionnel crée pendant une transaction.</span><span class="sxs-lookup"><span data-stu-id="87eb0-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="87eb0-113">Le miniversion peut être ouvert ultérieurement dans la transaction avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87eb0-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="87eb0-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lecteur transactionnel**</span><span class="sxs-lookup"><span data-stu-id="87eb0-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="87eb0-115">Un lecteur transactionnel est un descripteur de fichier transactionnel ouvert avec une autorisation qui fait partie de l’accès en lecture générique, mais qui ne fait pas partie d’un accès en écriture générique.</span><span class="sxs-lookup"><span data-stu-id="87eb0-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="87eb0-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**rédacteur transactionnel**</span><span class="sxs-lookup"><span data-stu-id="87eb0-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="87eb0-117">Un rédacteur transactionnel est un descripteur de fichier transactionnel ouvert avec une autorisation qui ne fait pas partie d’un accès en lecture générique, mais qui fait partie d’un accès en écriture générique.</span><span class="sxs-lookup"><span data-stu-id="87eb0-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



