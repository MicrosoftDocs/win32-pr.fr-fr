---
description: L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions InstallExecute ou InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Action InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753517"
---
# <a name="installfinalize-action"></a><span data-ttu-id="eae04-103">Action InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="eae04-103">InstallFinalize Action</span></span>

<span data-ttu-id="eae04-104">L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions [InstallExecute](installexecute-action.md) ou [InstallExecuteAgain](installexecuteagain-action.md) .</span><span class="sxs-lookup"><span data-stu-id="eae04-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="eae04-105">Cette action marque la fin d’une transaction qui commence par l’action [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="eae04-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="eae04-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="eae04-106">Sequence Restrictions</span></span>

<span data-ttu-id="eae04-107">L’action [InstallInitialize](installinitialize-action.md) doit précéder l’action InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="eae04-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="eae04-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="eae04-108">ActionData Messages</span></span>

<span data-ttu-id="eae04-109">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="eae04-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae04-110">Notes</span><span class="sxs-lookup"><span data-stu-id="eae04-110">Remarks</span></span>

<span data-ttu-id="eae04-111">S’il est détecté que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer l' **Ajout/suppression de programmes** dans les informations du **panneau de configuration** du produit, pour annuler l’inscription et annuler la publication du produit, et pour supprimer la base de données locale mise en cache de% Windows%, si elle existe.</span><span class="sxs-lookup"><span data-stu-id="eae04-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="eae04-112">Les modifications système effectuées avant l’action ne peuvent pas être restaurées après l’exécution de l’action InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="eae04-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="eae04-113">L’action InstallFinalize met à jour le système avec toutes les opérations déterminées à ce point, puis met fin à la transaction.</span><span class="sxs-lookup"><span data-stu-id="eae04-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



