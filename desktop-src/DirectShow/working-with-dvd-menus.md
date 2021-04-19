---
description: Utilisation des menus de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Utilisation des menus de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537144"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="e86ff-103">Utilisation des menus de DVD</span><span class="sxs-lookup"><span data-stu-id="e86ff-103">Working With DVD Menus</span></span>

<span data-ttu-id="e86ff-104">Le navigateur DVD peut afficher un menu lorsque l’utilisateur active un bouton ou lorsque le navigateur accède au premier domaine de lecture.</span><span class="sxs-lookup"><span data-stu-id="e86ff-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="e86ff-105">Pour afficher un menu par programme, appelez la méthode [**IDvdControl2 :: ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .</span><span class="sxs-lookup"><span data-stu-id="e86ff-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="e86ff-106">Il existe plusieurs façons de sélectionner des boutons de menu par programme :</span><span class="sxs-lookup"><span data-stu-id="e86ff-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="e86ff-107">Pour sélectionner un bouton par numéro, appelez [**IDvdControl2 :: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="e86ff-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="e86ff-108">Les boutons sont numérotés de 1 à 36.</span><span class="sxs-lookup"><span data-stu-id="e86ff-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="e86ff-109">La méthode [**IDvdInfo2 :: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) retourne le nombre de boutons disponibles.</span><span class="sxs-lookup"><span data-stu-id="e86ff-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="e86ff-110">Pour sélectionner un bouton par rapport à la position du bouton actuellement sélectionné, appelez [**IDvdControl2 :: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="e86ff-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="e86ff-111">Vous pouvez sélectionner un bouton dans la direction vers le haut, vers le bas, à gauche ou à droite.</span><span class="sxs-lookup"><span data-stu-id="e86ff-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="e86ff-112">Pour sélectionner un bouton par ses coordonnées dans la fenêtre, appelez [**IDvdControl2 :: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="e86ff-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="e86ff-113">Cette méthode prend les coordonnées (x, y) relatives à la zone cliente de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="e86ff-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="e86ff-114">(Pour le mode sans fenêtre, il s’agit de la fenêtre d’application.) S’il n’existe aucun bouton à cet emplacement, la méthode retourne \_ le \_ bouton VFW E DVD \_ no \_ .</span><span class="sxs-lookup"><span data-stu-id="e86ff-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="e86ff-115">De plus, il existe plusieurs façons d’activer un bouton :</span><span class="sxs-lookup"><span data-stu-id="e86ff-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="e86ff-116">Pour activer un bouton par nombre, appelez [**IDvdControl2 :: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span><span class="sxs-lookup"><span data-stu-id="e86ff-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="e86ff-117">Pour activer un bouton par ses coordonnées, appelez [**IDvdControl2 :: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span><span class="sxs-lookup"><span data-stu-id="e86ff-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="e86ff-118">Pour activer le bouton qui est actuellement sélectionné, appelez [**IDvdControl2 :: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="e86ff-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="e86ff-119">Si aucun bouton n’est sélectionné, la méthode retourne \_ le \_ bouton VFW E DVD \_ no \_ .</span><span class="sxs-lookup"><span data-stu-id="e86ff-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="e86ff-120">N’oubliez pas que la sélection d’un bouton met simplement en évidence ses bordures.</span><span class="sxs-lookup"><span data-stu-id="e86ff-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="e86ff-121">Pour déclencher l’activation de la commande associée, le bouton doit être activé.</span><span class="sxs-lookup"><span data-stu-id="e86ff-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="e86ff-122">L’activation d’un bouton par programmation peut être effectuée de différentes manières, mais le bouton doit toujours être sélectionné avant de pouvoir être activé.</span><span class="sxs-lookup"><span data-stu-id="e86ff-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e86ff-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e86ff-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86ff-124">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="e86ff-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



