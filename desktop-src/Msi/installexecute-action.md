---
description: L’action InstallExecute exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecute ou de l’action InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Action InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112263"
---
# <a name="installexecute-action"></a><span data-ttu-id="4be1c-103">Action InstallExecute</span><span class="sxs-lookup"><span data-stu-id="4be1c-103">InstallExecute Action</span></span>

<span data-ttu-id="4be1c-104">L’action InstallExecute exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecute ou de l’action [InstallExecuteAgain](installexecuteagain-action.md).</span><span class="sxs-lookup"><span data-stu-id="4be1c-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="4be1c-105">L’action InstallExecute met à jour le système sans mettre fin à la transaction.</span><span class="sxs-lookup"><span data-stu-id="4be1c-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4be1c-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="4be1c-106">Sequence Restrictions</span></span>

<span data-ttu-id="4be1c-107">L’action InstallExecute intervient entre l' [action InstallInitialize](installinitialize-action.md) et l’action [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="4be1c-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4be1c-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="4be1c-108">ActionData Messages</span></span>

<span data-ttu-id="4be1c-109">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="4be1c-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be1c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4be1c-110">Remarks</span></span>

<span data-ttu-id="4be1c-111">L' [action InstallExecuteAgain](installexecuteagain-action.md) effectue la même opération que l’action InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="4be1c-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="4be1c-112">Étant donné que les tables de séquence n’ont qu’une seule clé primaire, la colonne d’action, la même action ne peut pas être répétée dans une table de séquences particulière.</span><span class="sxs-lookup"><span data-stu-id="4be1c-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="4be1c-113">Il existe deux actions qui font la même chose, InstallExecute et InstallExecuteAgain, dans les cas où la fonctionnalité de InstallExecute est nécessaire deux fois dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4be1c-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="4be1c-114">Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4be1c-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



