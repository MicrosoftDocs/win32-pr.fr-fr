---
title: À propos des contrôles d’adresse IP
description: Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6859bd31250d30bcf26d0c5fde37afeca8cc81bd
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424229"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="e6195-103">À propos des contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e6195-103">About IP Address Controls</span></span>

<span data-ttu-id="e6195-104">Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible.</span><span class="sxs-lookup"><span data-stu-id="e6195-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="e6195-105">Ce contrôle permet également à l’application d’obtenir l’adresse sous forme numérique plutôt que sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="e6195-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="e6195-106">À propos des contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e6195-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="e6195-107">Création d’un contrôle d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e6195-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="e6195-108">Une adresse IP contrôle-t-elle un contrôle d’édition ?</span><span class="sxs-lookup"><span data-stu-id="e6195-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="e6195-109">À propos des contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e6195-109">About IP Address Controls</span></span>

<span data-ttu-id="e6195-110">Windows Internet Explorer version 4,0 introduit le contrôle d’adresse IP, un nouveau contrôle similaire à un contrôle d’édition qui permet à l’utilisateur d’entrer une adresse numérique au format IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="e6195-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="e6195-111">Ce format se compose de champs à 4 3 chiffres.</span><span class="sxs-lookup"><span data-stu-id="e6195-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="e6195-112">Chaque champ est traité individuellement. les numéros de champ sont de base zéro et se déroulent de gauche à droite, comme illustré dans cette figure.</span><span class="sxs-lookup"><span data-stu-id="e6195-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![Diagramme montrant des valeurs dans chacun des quatre champs d’un contrôle d’adresse IP](images/ipa-scrn.png)

<span data-ttu-id="e6195-114">Le contrôle permet d’entrer uniquement du texte numérique dans chacun des champs.</span><span class="sxs-lookup"><span data-stu-id="e6195-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="e6195-115">Une fois trois chiffres entrés dans un champ donné, le focus clavier est automatiquement déplacé vers le champ suivant.</span><span class="sxs-lookup"><span data-stu-id="e6195-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="e6195-116">Si le remplissage du champ entier n’est pas requis par l’application, l’utilisateur peut entrer moins de trois chiffres.</span><span class="sxs-lookup"><span data-stu-id="e6195-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="e6195-117">Par exemple, si le champ ne doit contenir que le nombre vingt-un, tapez « 21 » et appuyez sur la touche pour que l’utilisateur passe au champ suivant.</span><span class="sxs-lookup"><span data-stu-id="e6195-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="e6195-118">La plage par défaut de chaque champ est comprise entre 0 et 255, mais l’application peut définir la plage sur n’importe quelle valeur comprise entre ces limites et le message [**IPM \_ SetRange**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="e6195-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="e6195-119">Le contrôle d’adresse IP est implémenté dans la version 4,71 et les versions ultérieures de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="e6195-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="e6195-120">Création d’un contrôle d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e6195-120">Creating an IP Address Control</span></span>

<span data-ttu-id="e6195-121">Avant de créer un contrôle d’adresse IP, appelez [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avec l’indicateur des **\_ \_ classes Internet ICC** défini dans le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="e6195-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="e6195-122">Utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="e6195-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="e6195-123">Le nom de classe du contrôle est [**WC \_ IPAddress**](common-control-window-classes.md), qui est défini dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="e6195-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="e6195-124">Il n’existe pas de styles spécifiques à un contrôle d’adresse IP. Toutefois, étant donné qu’il s’agit d’un contrôle enfant, utilisez le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) au minimum.</span><span class="sxs-lookup"><span data-stu-id="e6195-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="e6195-125">Une adresse IP contrôle-t-elle un contrôle d’édition ?</span><span class="sxs-lookup"><span data-stu-id="e6195-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="e6195-126">Un contrôle d’adresse IP n’est pas un contrôle d’édition et ne répond pas aux \_ messages em.</span><span class="sxs-lookup"><span data-stu-id="e6195-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="e6195-127">Toutefois, il envoie à la fenêtre propriétaire les notifications de contrôle d’édition suivantes par le biais du message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e6195-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="e6195-128">Notez que le contrôle d’adresse IP enverra également \_ des notifications IPN privées par le biais du message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e6195-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|     <span data-ttu-id="e6195-129">Notification</span><span class="sxs-lookup"><span data-stu-id="e6195-129">Notification</span></span>                              |     <span data-ttu-id="e6195-130">Raison de la notification</span><span class="sxs-lookup"><span data-stu-id="e6195-130">Reason for notification</span></span>                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6195-131">en \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="e6195-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="e6195-132">Envoyé lorsque le contrôle d’adresse IP obtient le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="e6195-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="e6195-133">en \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="e6195-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="e6195-134">Envoyé lorsque le contrôle d’adresse IP perd le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="e6195-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="e6195-135">en \_ modification</span><span class="sxs-lookup"><span data-stu-id="e6195-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="e6195-136">Envoyé lorsqu’un champ du contrôle d’adresse IP change.</span><span class="sxs-lookup"><span data-stu-id="e6195-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="e6195-137">À l’instar de la notification en [ \_ modification](en-change.md) d’un contrôle d’édition standard, cette notification est reçue après la mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="e6195-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 