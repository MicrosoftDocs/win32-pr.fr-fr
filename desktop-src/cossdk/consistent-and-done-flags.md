---
description: Indicateurs cohérents et terminés
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Indicateurs cohérents et terminés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524372"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="8d8b2-103">Indicateurs cohérents et terminés</span><span class="sxs-lookup"><span data-stu-id="8d8b2-103">Consistent and Done Flags</span></span>

<span data-ttu-id="8d8b2-104">COM+ crée toujours un objet de contexte avant d’activer un objet transactionnel.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="8d8b2-105">L’objet Context contient des informations relatives aux objets, telles que son créateur et son identificateur de transaction.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="8d8b2-106">Chaque objet de contexte contient également un *indicateur de cohérence* et un *indicateur Done*.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="8d8b2-107">Ensemble, ces indicateurs déterminent l’état de l’objet transactionnel.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="8d8b2-108">L’indicateur de cohérence indique que l’objet transactionnel est cohérent ou incohérent.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="8d8b2-109">Les détails spécifiques de la cohérence de l’état d’un objet sont définis par le programmeur.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="8d8b2-110">Quand un appel de méthode affecte à cet indicateur la valeur true, l’objet est cohérent.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="8d8b2-111">False indique que l’objet est incohérent.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="8d8b2-112">COM+ affecte la valeur true à l’indicateur lorsqu’il crée une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="8d8b2-113">Un objet cohérent est prêt à poursuivre la transaction.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="8d8b2-114">Lorsqu’un objet reste actif, les appels de méthode suivants peuvent basculer à plusieurs reprises l’indicateur de cohérence de true à false et vice versa.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="8d8b2-115">L’indicateur Done détermine la durée d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="8d8b2-116">Lorsqu’un appel de méthode est retourné, COM+ inspecte l’indicateur Done.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="8d8b2-117">Si la méthode affecte à cet indicateur la valeur true, COM+ désactive l’objet et note l’indicateur de cohérence.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="8d8b2-118">Lorsque l’indicateur Done a la valeur false, COM+ ne désactive pas l’objet et ne note pas l’indicateur consistent.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="8d8b2-119">COM+ affecte la valeur false à l’indicateur Done lorsqu’il crée une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="8d8b2-120">L’indicateur consistent convertit un vote pour valider ou abandonner la transaction dans laquelle il s’exécute, et l’indicateur Done finalise le vote.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="8d8b2-121">COM+ inspecte l’indicateur de cohérence lorsque l’indicateur Done a la valeur true lors du retour d’un appel de méthode ou lorsque l’objet est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="8d8b2-122">Bien que l’indicateur de cohérence d’un objet puisse changer à plusieurs reprises au sein de chaque appel de méthode, seule la dernière modification compte.</span><span class="sxs-lookup"><span data-stu-id="8d8b2-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d8b2-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d8b2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d8b2-124">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="8d8b2-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="8d8b2-125">Définition des indicateurs cohérents et terminés</span><span class="sxs-lookup"><span data-stu-id="8d8b2-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



