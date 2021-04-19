---
description: ICE44 vérifie que NewDialog, SpawnDialog et SpawnWaitDialog ControlEvents font référence à des boîtes de dialogue valides dans la table Dialog.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520593"
---
# <a name="ice44"></a><span data-ttu-id="eb42c-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="eb42c-103">ICE44</span></span>

<span data-ttu-id="eb42c-104">ICE44 vérifie que [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)et [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents font référence à des boîtes de dialogue valides dans la [table Dialog](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb42c-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="eb42c-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="eb42c-105">Result</span></span>

<span data-ttu-id="eb42c-106">ICE44 publie un message d’erreur s’il existe un événement de contrôle de boîte de dialogue qui ne fait pas référence à une boîte de dialogue figurant dans la table de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="eb42c-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="eb42c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb42c-107">Example</span></span>

<span data-ttu-id="eb42c-108">ICE44 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="eb42c-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="eb42c-109">Erreur ICE44</span><span class="sxs-lookup"><span data-stu-id="eb42c-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="eb42c-110">Description</span><span class="sxs-lookup"><span data-stu-id="eb42c-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb42c-111">Événement de contrôle pour le contrôle’dialog1 '. ' Control1 'est de type SpawnDialog, mais son argument Dialog2 n’est pas une entrée valide dans la table Dialog.</span><span class="sxs-lookup"><span data-stu-id="eb42c-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="eb42c-112">Il existe une action SpawnDialog, SpawnWaitDialog ou NewDialog avec un argument qui ne fait pas référence à une boîte de dialogue dans la table Dialog.</span><span class="sxs-lookup"><span data-stu-id="eb42c-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="eb42c-113">Pour corriger cette erreur, ajoutez un argument qui est une clé dans la table de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="eb42c-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="eb42c-114">[Table de boîtes de dialogue](dialog-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="eb42c-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="eb42c-115">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="eb42c-115">Dialog</span></span>  | <span data-ttu-id="eb42c-116">Intitulé</span><span class="sxs-lookup"><span data-stu-id="eb42c-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="eb42c-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="eb42c-117">Dialog1</span></span> |       |



 

<span data-ttu-id="eb42c-118">[Table ControlEvent,](controlevent-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="eb42c-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="eb42c-119">Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="eb42c-119">Dialog\_</span></span> | <span data-ttu-id="eb42c-120">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="eb42c-120">Control\_</span></span> | <span data-ttu-id="eb42c-121">Type</span><span class="sxs-lookup"><span data-stu-id="eb42c-121">Type</span></span>        | <span data-ttu-id="eb42c-122">Argument</span><span class="sxs-lookup"><span data-stu-id="eb42c-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="eb42c-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="eb42c-123">Dialog1</span></span>  | <span data-ttu-id="eb42c-124">Control1</span><span class="sxs-lookup"><span data-stu-id="eb42c-124">Control1</span></span>  | <span data-ttu-id="eb42c-125">SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="eb42c-125">SpawnDialog</span></span> | <span data-ttu-id="eb42c-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="eb42c-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="eb42c-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb42c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb42c-128">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="eb42c-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




