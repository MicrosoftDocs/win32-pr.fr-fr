---
description: L’action InstallExecuteAgain exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecuteAgain ou de la dernière action InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Action InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951100"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="a2751-103">Action InstallExecuteAgain</span><span class="sxs-lookup"><span data-stu-id="a2751-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="a2751-104">L’action InstallExecuteAgain exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecuteAgain ou de la dernière [action InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="a2751-105">L’action InstallExecute met à jour le système sans mettre fin à la transaction.</span><span class="sxs-lookup"><span data-stu-id="a2751-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="a2751-106">InstallExecuteAgain effectue la même opération que l' [action InstallExecute](installexecute-action.md) , mais ne doit être utilisée qu’après InstallExecute.</span><span class="sxs-lookup"><span data-stu-id="a2751-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="a2751-107">InstallExecuteAgain doit toujours être défini de manière à ce qu’il ne s’exécute pas pendant la suppression.</span><span class="sxs-lookup"><span data-stu-id="a2751-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="a2751-108">Pour plus d’informations, consultez [utilisation des propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a2751-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="a2751-109">Sequence Restrictions</span></span>

<span data-ttu-id="a2751-110">L’action InstallExecute intervient entre l' [action InstallInitialize](installinitialize-action.md) et l’action [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a2751-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="a2751-111">ActionData Messages</span></span>

<span data-ttu-id="a2751-112">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="a2751-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2751-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a2751-113">Remarks</span></span>

<span data-ttu-id="a2751-114">L’action InstallExecuteAgain effectue la même opération que l' [action InstallExecute](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="a2751-115">Étant donné que les tables de séquence n’ont qu’une seule clé primaire, la colonne d’action, la même action ne peut pas être répétée dans une table de séquences particulière.</span><span class="sxs-lookup"><span data-stu-id="a2751-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="a2751-116">Il existe deux actions qui font la même chose, InstallExecute et InstallExecuteAgain, dans les cas où la fonctionnalité de InstallExecute est nécessaire deux fois dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="a2751-117">Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a2751-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



