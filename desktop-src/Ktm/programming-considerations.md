---
description: 'En savoir plus sur : considérations relatives à la programmation pour l’écriture de gestionnaires de ressources'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Considérations relatives à la programmation pour l’écriture de gestionnaires de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529177"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="8553e-103">Considérations relatives à la programmation pour l’écriture de gestionnaires de ressources</span><span class="sxs-lookup"><span data-stu-id="8553e-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="8553e-104">Lorsque vous utilisez l’API du gestionnaire de transactions du noyau pour ajouter la prise en charge des transactions à vos applications, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8553e-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="8553e-105">Lorsque vous écrivez votre propre gestionnaire de ressources, vous devez disposer d’une bonne connaissance pratique des techniques et des protocoles de gestion des transactions.</span><span class="sxs-lookup"><span data-stu-id="8553e-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="8553e-106">Si vous n’écrivez pas correctement les gestionnaires de ressources, vous pouvez corrompre vos propres données avec des opérations de récupération correctement gérées.</span><span class="sxs-lookup"><span data-stu-id="8553e-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="8553e-107">Vous pouvez également épingler la fin du journal des transactions et remplir votre système de fichiers à l’aide des journaux de transactions.</span><span class="sxs-lookup"><span data-stu-id="8553e-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="8553e-108">Si votre stratégie de taille de journal n’est pas définie pour empêcher la taille du journal, votre gestionnaire de ressources n’arrête pas les transactions.</span><span class="sxs-lookup"><span data-stu-id="8553e-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="8553e-109">Votre gestionnaire de ressources doit arrêter la mise à jour du système afin qu’il ne sature pas les ressources du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8553e-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="8553e-110">Les gestionnaires de ressources doivent utiliser des listes de contrôle d’accès (ACL) pour contrôler l’accès aux fichiers journaux. dans le cas contraire, les attaques par déni de service sont possibles.</span><span class="sxs-lookup"><span data-stu-id="8553e-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="8553e-111">Tout gestionnaire de ressources ou participant de transaction qui met en cache des données doit s’inscrire pour les notifications de prépréparation.</span><span class="sxs-lookup"><span data-stu-id="8553e-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="8553e-112">Lors de la réception d’une notification de prépréparation, vous devez vider toutes vos données, de sorte que tous les gestionnaires de ressources en aval puissent s’inscrire avant la phase de préparation.</span><span class="sxs-lookup"><span data-stu-id="8553e-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="8553e-113">Tout travail supplémentaire dans cette transaction ne doit pas être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8553e-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="8553e-114">Ne fermez pas un handle d’inscription tant que la transaction est toujours active ; Cela entraîne la restauration de la transaction.</span><span class="sxs-lookup"><span data-stu-id="8553e-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



