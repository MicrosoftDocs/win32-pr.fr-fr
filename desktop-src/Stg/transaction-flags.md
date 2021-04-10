---
title: Indicateurs de transaction
description: Un objet peut être ouvert en mode direct ou traité.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196943"
---
# <a name="transaction-flags"></a><span data-ttu-id="9af90-103">Indicateurs de transaction</span><span class="sxs-lookup"><span data-stu-id="9af90-103">Transaction Flags</span></span>

<span data-ttu-id="9af90-104">Un objet peut être ouvert en mode direct ou traité.</span><span class="sxs-lookup"><span data-stu-id="9af90-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="9af90-105">Lorsqu’un objet est ouvert en mode direct, les modifications sont apportées immédiatement et de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="9af90-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="9af90-106">Lorsqu’un objet est ouvert en mode traité, les modifications sont mises en mémoire tampon afin qu’elles puissent être explicitement validées ou rétablies une fois la modification terminée.</span><span class="sxs-lookup"><span data-stu-id="9af90-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="9af90-107">Les modifications validées sont enregistrées dans l’objet pendant que les modifications annulées sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="9af90-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="9af90-108">Le mode direct est le mode d’accès par défaut.</span><span class="sxs-lookup"><span data-stu-id="9af90-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="9af90-109">Le mode transactionnel n’est pas requis sur un objet de stockage parent pour pouvoir être utilisé sur un élément imbriqué.</span><span class="sxs-lookup"><span data-stu-id="9af90-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="9af90-110">Toutefois, une transaction pour un élément imbriqué est imbriquée dans la transaction pour son objet de stockage parent.</span><span class="sxs-lookup"><span data-stu-id="9af90-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="9af90-111">Par conséquent, les modifications apportées à un objet enfant ne peuvent pas être validées tant que celles-ci n’ont pas été validées, et elles restent non validées jusqu’à ce que l’objet de stockage racine (le parent de niveau supérieur) soit effectivement écrit sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9af90-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="9af90-112">En d’autres termes, les modifications se déplacent vers l’extérieur : les objets internes publient les modifications apportées aux transactions de leurs conteneurs immédiats.</span><span class="sxs-lookup"><span data-stu-id="9af90-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




