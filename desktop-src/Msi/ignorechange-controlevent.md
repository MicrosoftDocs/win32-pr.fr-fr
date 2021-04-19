---
description: Le ControlEvent, IgnoreChange est publié par le contrôle DirectoryList lorsque le dossier sélectionné passe d’un répertoire à un autre dans le contrôle. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525019"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="4e7e6-104">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="4e7e6-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="4e7e6-105">Le ControlEvent, IgnoreChange est publié par le [contrôle DirectoryList](directorylist-control.md) lorsque le dossier sélectionné passe d’un répertoire à un autre dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e7e6-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="4e7e6-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="4e7e6-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="4e7e6-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4e7e6-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4e7e6-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4e7e6-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4e7e6-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4e7e6-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4e7e6-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="4e7e6-110">Published By</span></span>

[<span data-ttu-id="4e7e6-111">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="4e7e6-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="4e7e6-112">Argument</span><span class="sxs-lookup"><span data-stu-id="4e7e6-112">Argument</span></span>

<span data-ttu-id="4e7e6-113">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="4e7e6-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4e7e6-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="4e7e6-114">Action on Subscribers</span></span>

<span data-ttu-id="4e7e6-115">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="4e7e6-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4e7e6-116">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="4e7e6-116">Typical Use</span></span>

<span data-ttu-id="4e7e6-117">Le [contrôle DirectoryCombo](directorycombo-control.md) utilise généralement le ControlEvent, IgnoreChange.</span><span class="sxs-lookup"><span data-stu-id="4e7e6-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



