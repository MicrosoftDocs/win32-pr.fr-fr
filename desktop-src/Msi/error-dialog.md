---
description: Une boîte de dialogue d’erreur est une boîte de dialogue modale qui affiche un message d’erreur. Il peut y avoir plusieurs boîtes de dialogue d’erreur dans chaque installation.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Boîte de dialogue d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527250"
---
# <a name="error-dialog"></a><span data-ttu-id="137cb-104">Boîte de dialogue d’erreur</span><span class="sxs-lookup"><span data-stu-id="137cb-104">Error Dialog</span></span>

<span data-ttu-id="137cb-105">Une boîte de dialogue d’erreur est une boîte de dialogue modale qui affiche un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="137cb-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="137cb-106">Il peut y avoir plusieurs boîtes de dialogue d’erreur dans chaque installation.</span><span class="sxs-lookup"><span data-stu-id="137cb-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="137cb-107">Une propriété ErrorDialog doit être définie pour spécifier la boîte de dialogue à utiliser.</span><span class="sxs-lookup"><span data-stu-id="137cb-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="137cb-108">Si cette propriété n’est pas définie ou ne pointe pas vers une boîte de dialogue d’erreur valide, les messages d’erreur ne s’affichent pas.</span><span class="sxs-lookup"><span data-stu-id="137cb-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="137cb-109">Dans ce cas, l’erreur est enregistrée uniquement avec un avertissement concernant la boîte de dialogue manquante.</span><span class="sxs-lookup"><span data-stu-id="137cb-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="137cb-110">Le bit de style de boîte de [dialogue d’erreur](error-dialog-style-bit.md) doit être défini pour une boîte de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="137cb-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="137cb-111">La boîte de dialogue doit avoir un [contrôle de texte](text-control.md) nommé ErrorText.</span><span class="sxs-lookup"><span data-stu-id="137cb-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="137cb-112">L’enregistrement de la boîte de dialogue d’erreur dans la [table de boîte de dialogue](dialog-table.md) doit avoir le contrôle ErrorText entré dans le \_ premier champ Control.</span><span class="sxs-lookup"><span data-stu-id="137cb-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="137cb-113">La boîte de dialogue doit contenir sept [PUSHBUTTON](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="137cb-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="137cb-114">Tous ces boutons spécifient le ControlEvent, [EndDialog](enddialog-controlevent.md) dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="137cb-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="137cb-115">Chaque bouton spécifie l’un des attributs suivants : **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span><span class="sxs-lookup"><span data-stu-id="137cb-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="137cb-116">Le focus de ces contrôles ne doit pas être lié par le biais de l’utilisation de la \_ colonne Control Next dans la [table Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="137cb-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="137cb-117">Ces boutons doivent être placés à peu près à la même position dans la boîte de dialogue, car lorsqu’ils sont créés, seul un sous-ensemble de ces sept boutons est créé, en fonction du message.</span><span class="sxs-lookup"><span data-stu-id="137cb-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="137cb-118">La coordonnée X des boutons est modifiée afin que les boutons affichés soient espacés uniformément.</span><span class="sxs-lookup"><span data-stu-id="137cb-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="137cb-119">La coordonnée Y, la hauteur et la largeur des boutons sont inchangées.</span><span class="sxs-lookup"><span data-stu-id="137cb-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="137cb-120">Étant donné que les boutons sont disposés horizontalement, aucun autre contrôle ne peut être placé dans la même zone horizontale de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="137cb-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="137cb-121">Pour une boîte de dialogue d’erreur, les \_ champs Control default et Control \_ Cancel de la [table Dialog](dialog-table.md) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="137cb-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="137cb-122">Le \_ premier champ contrôle d’une boîte de dialogue d’erreur doit spécifier le contrôle ErrorText.</span><span class="sxs-lookup"><span data-stu-id="137cb-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="137cb-123">Si un [contrôle Icon](icon-control.md) nommé ErrorIcon est inclus dans cette boîte de dialogue, les icônes Windows standard suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="137cb-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="137cb-124">\_Erreur IDI en réponse aux messages imtFatalExit.</span><span class="sxs-lookup"><span data-stu-id="137cb-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="137cb-125">IDI \_ avertissement en réponse aux messages imtWarning et.</span><span class="sxs-lookup"><span data-stu-id="137cb-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="137cb-126">IDI \_ les informations en réponse aux messages imtOutOfDiskSpace.</span><span class="sxs-lookup"><span data-stu-id="137cb-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="137cb-127">Le contrôle ErrorIcon doit être créé avec l' [attribut de contrôle FixedSize](fixedsize-control-attribute.md) défini pour éviter le dimensionnement incorrect des icônes Windows standard.</span><span class="sxs-lookup"><span data-stu-id="137cb-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 



