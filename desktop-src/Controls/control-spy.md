---
title: Contrôler Spy v 2.0
description: Control Spy est un outil qui aide les développeurs à comprendre les contrôles communs sur la manière d’appliquer des styles à eux et comment ils répondent aux messages et aux notifications.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032024"
---
# <a name="control-spy-v20"></a><span data-ttu-id="64c16-103">Contrôler Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="64c16-103">Control Spy v2.0</span></span>

<span data-ttu-id="64c16-104">Control Spy est un outil qui aide les développeurs à comprendre les contrôles courants : comment leur appliquer des styles et comment ils répondent aux messages et aux notifications.</span><span class="sxs-lookup"><span data-stu-id="64c16-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="64c16-105">À l’aide de Control Spy, vous pouvez voir immédiatement comment différents styles affectent le comportement et l’apparence de chaque contrôle, ainsi que la façon dont vous pouvez modifier l’état de chaque contrôle en envoyant des messages.</span><span class="sxs-lookup"><span data-stu-id="64c16-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="64c16-106">Deux versions de Control Spy sont disponibles, une pour [Comctl32.dll version 5. x](common-control-versions.md) et une pour Comctl32.dll version 6,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="64c16-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="64c16-107">ControlSpyV6.exe a un manifeste d’application intégré, afin qu’il utilise les contrôles les plus récents.</span><span class="sxs-lookup"><span data-stu-id="64c16-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="64c16-108">ControlSpyV5.exe n’a pas ce manifeste. par conséquent, il s’agit par défaut de l’ancienne version.</span><span class="sxs-lookup"><span data-stu-id="64c16-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="64c16-109">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="64c16-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="64c16-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="64c16-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="64c16-111">Styles</span><span class="sxs-lookup"><span data-stu-id="64c16-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="64c16-112">Messages</span><span class="sxs-lookup"><span data-stu-id="64c16-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="64c16-113">Taille/couleur</span><span class="sxs-lookup"><span data-stu-id="64c16-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="64c16-114">Où se procurer l’espionnage de contrôle</span><span class="sxs-lookup"><span data-stu-id="64c16-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="64c16-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64c16-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="64c16-116">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="64c16-116">Overview</span></span>

<span data-ttu-id="64c16-117">Le contrôle Spy héberge un contrôle commun sélectionné au centre de sa fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="64c16-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="64c16-118">Vous pouvez modifier le contrôle affiché en sélectionnant différents contrôles dans la zone de liste située à gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="64c16-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="64c16-119">Les messages ou notifications reçus par le contrôle sont affichés dans la partie droite de la fenêtre à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="64c16-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="64c16-120">Vous pouvez activer ou désactiver cette fonctionnalité à l’aide des cases à cocher **messages reçus** et **notifications reçues** .</span><span class="sxs-lookup"><span data-stu-id="64c16-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="64c16-121">L’illustration suivante montre l’application Control Spy.</span><span class="sxs-lookup"><span data-stu-id="64c16-121">The following image shows the Control Spy application.</span></span>

![fenêtre Espion de contrôle](images/controlspy-main.png)

<span data-ttu-id="64c16-123">En bas de la fenêtre, plusieurs onglets présentent davantage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="64c16-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="64c16-124">Styles</span><span class="sxs-lookup"><span data-stu-id="64c16-124">Styles</span></span>

<span data-ttu-id="64c16-125">L’onglet **styles** vous permet de modifier le style de fenêtre actuel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="64c16-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="64c16-126">Sélectionnez ou désélectionnez les styles répertoriés, puis cliquez sur le bouton **appliquer** pour modifier le style du contrôle affiché.</span><span class="sxs-lookup"><span data-stu-id="64c16-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="64c16-127">Vous pouvez également utiliser le bouton **recréer** pour créer un nouveau contrôle avec les styles sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="64c16-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="64c16-128">Le bouton **Réinitialiser** retournera le contrôle aux styles par défaut.</span><span class="sxs-lookup"><span data-stu-id="64c16-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="64c16-129">Les boutons **copier le style** et **copier** le style sous l’onglet copient les constantes de style sélectionnées dans le presse-papiers sous la forme d’une liste délimitée par des bits ou ( \| ).</span><span class="sxs-lookup"><span data-stu-id="64c16-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="64c16-130">Vous pouvez coller cette liste directement dans votre appel à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour fournir un contrôle dans votre application avec le même style.</span><span class="sxs-lookup"><span data-stu-id="64c16-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="64c16-131">L’illustration suivante montre l’onglet **styles** pour un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="64c16-131">The following image shows the **Styles** tab for a button control.</span></span>

![onglet de contrôle des styles Spy](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="64c16-133">Messages</span><span class="sxs-lookup"><span data-stu-id="64c16-133">Messages</span></span>

<span data-ttu-id="64c16-134">L’onglet **messages** vous permet d’envoyer presque n’importe quel message à un contrôle.</span><span class="sxs-lookup"><span data-stu-id="64c16-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="64c16-135">Après avoir sélectionné un message dans la zone de liste, vous pouvez entrer des données qui sont envoyées en tant que paramètres *wParam* et *lParam* de l’appel à [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="64c16-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="64c16-136">Une fois que vous avez cliqué sur **Envoyer**, le message est envoyé au contrôle et tous les résultats s’affichent dans la zone de texte en bas de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="64c16-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="64c16-137">L’illustration suivante montre l’onglet messages lorsqu’un message particulier est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64c16-137">The following image shows the messages tab when a particular message is selected.</span></span>

![onglet de contrôle des messages Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="64c16-139">Taille/couleur</span><span class="sxs-lookup"><span data-stu-id="64c16-139">Size/Color</span></span>

<span data-ttu-id="64c16-140">L’onglet **taille/couleur** peut être utilisé pour modifier la taille du contrôle ainsi que la couleur de son arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="64c16-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="64c16-141">Où se procurer l’espionnage de contrôle</span><span class="sxs-lookup"><span data-stu-id="64c16-141">Where to Get Control Spy</span></span>

<span data-ttu-id="64c16-142">Vous pouvez télécharger [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) à partir de MSDN.</span><span class="sxs-lookup"><span data-stu-id="64c16-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="64c16-143">Les deux versions sont contenues dans le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="64c16-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64c16-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64c16-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64c16-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="64c16-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64c16-146">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="64c16-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="64c16-147">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="64c16-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 