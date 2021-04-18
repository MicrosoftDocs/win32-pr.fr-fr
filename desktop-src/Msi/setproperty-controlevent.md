---
description: 'La syntaxe de l’événement SetProperty est différente de celle d’autres ControlEvents à la place du nom de l’événement 1 place la propriété entre crochets : \[ nom de la propriété \_ \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: ControlEvent, SetProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536176"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="0c01c-103">ControlEvent, SetProperty</span><span class="sxs-lookup"><span data-stu-id="0c01c-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="0c01c-104">La syntaxe de l’événement SetProperty est différente de celle d’autres ControlEvents à la place du nom de l’événement 1 place la propriété entre crochets : \[ nom de la propriété \_ \] .</span><span class="sxs-lookup"><span data-stu-id="0c01c-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="0c01c-105">L’argument est la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0c01c-105">The argument is the new value of the property.</span></span> <span data-ttu-id="0c01c-106">Pour annuler la propriété, l’argument doit avoir la valeur {} .</span><span class="sxs-lookup"><span data-stu-id="0c01c-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="0c01c-107">Cela est nécessaire, car l’argument est une clé primaire dans la table et ne peut pas être null.</span><span class="sxs-lookup"><span data-stu-id="0c01c-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="0c01c-108">L’argument sera mis en forme à l’aide de la méthode FormatText. par conséquent, l’argument peut contenir toute expression que la méthode FormatText peut gérer.</span><span class="sxs-lookup"><span data-stu-id="0c01c-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="0c01c-109">Les valeurs de propriété sont évaluées au moment de l’ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="0c01c-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="0c01c-110">Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="0c01c-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="0c01c-111">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="0c01c-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="0c01c-112">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0c01c-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="0c01c-113">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c01c-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="0c01c-114">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0c01c-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="0c01c-115">Publié par</span><span class="sxs-lookup"><span data-stu-id="0c01c-115">Published By</span></span>

<span data-ttu-id="0c01c-116">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="0c01c-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="0c01c-117">Argument</span><span class="sxs-lookup"><span data-stu-id="0c01c-117">Argument</span></span>

<span data-ttu-id="0c01c-118">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0c01c-118">The new value of the property.</span></span> <span data-ttu-id="0c01c-119">{} pour null.</span><span class="sxs-lookup"><span data-stu-id="0c01c-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0c01c-120">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="0c01c-120">Action on Subscribers</span></span>

<span data-ttu-id="0c01c-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="0c01c-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0c01c-122">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="0c01c-122">Typical Use</span></span>

<span data-ttu-id="0c01c-123">Contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue liée à cet événement pour qu’il modifie une propriété lorsque le bouton fait l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="0c01c-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



