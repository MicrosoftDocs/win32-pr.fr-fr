---
description: Une barre d’outils de bureau d’application (également appelée appbar) est une fenêtre similaire à la barre des tâches Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Utilisation des barres d’outils de l’application Desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112354"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="a2994-103">Utilisation des barres d’outils de l’application Desktop</span><span class="sxs-lookup"><span data-stu-id="a2994-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="a2994-104">Une *barre d’outils de bureau d’application* (également appelée appbar) est une fenêtre similaire à la barre des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="a2994-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="a2994-105">Elle est ancrée à un bord de l’écran et contient généralement des boutons qui permettent à l’utilisateur d’accéder rapidement à d’autres applications et fenêtres.</span><span class="sxs-lookup"><span data-stu-id="a2994-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="a2994-106">Le système empêche d’autres applications d’utiliser la zone de bureau utilisée par un appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="a2994-107">Un nombre quelconque de barres peut exister sur le Bureau à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="a2994-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="a2994-108">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2994-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a2994-109">À propos des barres d’outils application Desktop</span><span class="sxs-lookup"><span data-stu-id="a2994-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="a2994-110">Envoi de messages</span><span class="sxs-lookup"><span data-stu-id="a2994-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="a2994-111">Inscription</span><span class="sxs-lookup"><span data-stu-id="a2994-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="a2994-112">Taille et position de appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="a2994-113">Masquer automatiquement les barres d’outils du Bureau d’application</span><span class="sxs-lookup"><span data-stu-id="a2994-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="a2994-114">Messages de notification appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="a2994-115">Inscription d’une barre d’outils de bureau d’application</span><span class="sxs-lookup"><span data-stu-id="a2994-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="a2994-116">Définition de la taille et de la position appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="a2994-117">Traitement des messages de notification appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="a2994-118">À propos des barres d’outils application Desktop</span><span class="sxs-lookup"><span data-stu-id="a2994-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="a2994-119">Windows fournit une API qui vous permet de tirer parti des services appbar fournis par le système.</span><span class="sxs-lookup"><span data-stu-id="a2994-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="a2994-120">Les services permettent de s’assurer que les barres définis par l’application fonctionnent correctement les uns avec les autres et avec la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2994-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="a2994-121">Le système gère les informations sur chaque appbar et envoie les messages barres pour les informer des événements qui peuvent affecter leur taille, leur position et leur apparence.</span><span class="sxs-lookup"><span data-stu-id="a2994-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="a2994-122">sending messages</span><span class="sxs-lookup"><span data-stu-id="a2994-122">Sending Messages</span></span>

<span data-ttu-id="a2994-123">Une application utilise un ensemble spécial de messages, appelés messages appbar, pour ajouter ou supprimer un appbar, définir la taille et la position d’un appbar et récupérer des informations sur la taille, la position et l’état de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2994-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="a2994-124">Pour envoyer un message appbar, une application doit utiliser la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) .</span><span class="sxs-lookup"><span data-stu-id="a2994-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="a2994-125">Les paramètres de la fonction incluent un identificateur de message, tel que [**ABM \_ New**](abm-new.md), et l’adresse d’une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a2994-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="a2994-126">Les membres de structure contiennent les informations dont le système a besoin pour traiter le message donné.</span><span class="sxs-lookup"><span data-stu-id="a2994-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="a2994-127">Pour tout message appbar donné, le système utilise certains membres de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) et ignore les autres.</span><span class="sxs-lookup"><span data-stu-id="a2994-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="a2994-128">Toutefois, le système utilise toujours les membres **cbSize** et **HWND** , de sorte qu’une application doit remplir ces membres pour chaque message appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="a2994-129">Le membre **cbSize** spécifie la taille de la structure, et le membre **HWND** est le handle de la fenêtre du appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="a2994-130">Certains messages appbar demandent des informations du système.</span><span class="sxs-lookup"><span data-stu-id="a2994-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="a2994-131">Lors du traitement de ces messages, le système copie les informations demandées dans la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a2994-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="a2994-132">Inscription</span><span class="sxs-lookup"><span data-stu-id="a2994-132">Registration</span></span>

<span data-ttu-id="a2994-133">Le système conserve une liste interne de barres et conserve des informations sur chaque barre de la liste.</span><span class="sxs-lookup"><span data-stu-id="a2994-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="a2994-134">Le système utilise les informations pour gérer les barres, y effectuer des services et leur envoyer des messages de notification.</span><span class="sxs-lookup"><span data-stu-id="a2994-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="a2994-135">Une application doit inscrire un appbar (c’est-à-dire l’ajouter à la liste interne) avant de pouvoir recevoir des services appbar à partir du système.</span><span class="sxs-lookup"><span data-stu-id="a2994-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="a2994-136">Pour inscrire un appbar, une application envoie le [**\_ nouveau message ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a2994-137">La structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) associée comprend le descripteur de la fenêtre du appbar et un identificateur de message défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="a2994-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="a2994-138">Le système utilise l’identificateur de message pour envoyer des messages de notification à la procédure de fenêtre de la fenêtre appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="a2994-139">Pour plus d’informations, consultez messages de notification appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="a2994-140">Une application annule l’inscription d’un appbar en envoyant le message [**ABM \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="a2994-141">L’annulation de l’inscription d’un appbar le supprime de la liste interne des barres du système.</span><span class="sxs-lookup"><span data-stu-id="a2994-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="a2994-142">Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="a2994-143">Une application doit toujours envoyer **ABM \_ supprimer** avant de détruire un appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="a2994-144">Taille et position de appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-144">Appbar Size and Position</span></span>

<span data-ttu-id="a2994-145">Une application doit définir la taille et la position d’un appbar afin qu’il n’interfère pas avec d’autres barres ou la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2994-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="a2994-146">Chaque appbar doit être ancré à un bord particulier de l’écran, et plusieurs barres peuvent être ancrés à une arête.</span><span class="sxs-lookup"><span data-stu-id="a2994-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="a2994-147">Toutefois, si un appbar est ancré sur le même bord que la barre des tâches, le système garantit que la barre des tâches est toujours sur le bord le plus à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="a2994-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="a2994-148">Pour définir la taille et la position d’un appbar, une application propose tout d’abord un bord d’écran et un rectangle englobant pour appbar en envoyant le message [**ABM \_ QUERYPOS**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="a2994-149">Le système détermine si une partie de la zone d’écran dans le rectangle proposé est utilisée par la barre des tâches ou un autre appbar, ajuste le rectangle (si nécessaire) et retourne le rectangle ajusté à l’application.</span><span class="sxs-lookup"><span data-stu-id="a2994-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="a2994-150">Ensuite, l’application envoie le message [**ABM \_ SetPos**](abm-setpos.md) pour définir le nouveau rectangle englobant pour le appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="a2994-151">Là encore, le système peut ajuster le rectangle avant de le renvoyer à l’application.</span><span class="sxs-lookup"><span data-stu-id="a2994-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="a2994-152">Pour cette raison, l’application doit utiliser le rectangle ajusté retourné par **ABM \_ SetPos** pour définir la taille et la position finales.</span><span class="sxs-lookup"><span data-stu-id="a2994-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="a2994-153">L’application peut utiliser la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour déplacer le appbar dans la position.</span><span class="sxs-lookup"><span data-stu-id="a2994-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="a2994-154">En utilisant un processus en deux étapes pour définir la taille et la position, le système permet à l’application de fournir des commentaires intermédiaires à l’utilisateur pendant l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a2994-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="a2994-155">Par exemple, si l’utilisateur fait glisser un appbar, l’application peut afficher un rectangle ombré indiquant la nouvelle position avant le déplacement réel du appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="a2994-156">Une application doit définir la taille et la position de son appbar après l’avoir inscrit et chaque fois que le appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="a2994-157">Un appbar reçoit ce message de notification chaque fois qu’une modification se produit dans la taille, la position ou l’état de visibilité de la barre des tâches et lorsqu’un autre appbar du même côté de l’écran est redimensionné, ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="a2994-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="a2994-158">Chaque fois qu’un appbar reçoit le \_ message WM Activate, il doit envoyer le message d' [**\_ activation ABM**](abm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="a2994-159">De même, lorsqu’un appbar reçoit un \_ message WM WINDOWPOSCHANGED, il doit appeler [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md).</span><span class="sxs-lookup"><span data-stu-id="a2994-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="a2994-160">L’envoi de ces messages permet de s’assurer que le système définit correctement l’ordre de plan des barres de masquage automatique sur le même bord.</span><span class="sxs-lookup"><span data-stu-id="a2994-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="a2994-161">Masquer automatiquement les barres d’outils du Bureau d’application</span><span class="sxs-lookup"><span data-stu-id="a2994-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="a2994-162">Un appbar de masquage automatique est normalement masqué mais devient visible lorsque l’utilisateur déplace le curseur de la souris sur le bord de l’écran auquel le appbar est associé.</span><span class="sxs-lookup"><span data-stu-id="a2994-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="a2994-163">Le appbar se masque à nouveau lorsque l’utilisateur déplace le curseur de la souris hors du rectangle englobant de la barre.</span><span class="sxs-lookup"><span data-stu-id="a2994-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="a2994-164">Bien que le système autorise un certain nombre de barres différents à un moment donné, il n’autorise qu’un seul appbar de masquage automatique à la fois pour chaque bord d’écran, sur la base d’un premier arrivé, premier servi.</span><span class="sxs-lookup"><span data-stu-id="a2994-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="a2994-165">Le système conserve automatiquement l’ordre de plan d’un appbar de masquage automatique (dans son groupe de l’ordre de plan uniquement).</span><span class="sxs-lookup"><span data-stu-id="a2994-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="a2994-166">Une application utilise le message [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) pour inscrire ou annuler l’inscription d’un appbar de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="a2994-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="a2994-167">Le message spécifie le bord du appbar et un indicateur qui spécifie si le appbar doit être inscrit ou désinscrit.</span><span class="sxs-lookup"><span data-stu-id="a2994-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="a2994-168">Le message échoue si un appbar de masquage automatique est en cours d’enregistrement mais qu’un est déjà associé à la périphérie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a2994-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="a2994-169">Une application peut récupérer le descripteur du appbar de masquage automatique associé à une arête en envoyant le message [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="a2994-170">Un appbar à masquage automatique n’a pas besoin de s’inscrire en tant que appbar normal ; autrement dit, il n’a pas besoin d’être inscrit en envoyant [**le \_ nouveau message ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a2994-171">Un appbar qui n’est pas inscrit par **ABM \_ New** recouvre tout barres ancré sur le même bord de l’écran.</span><span class="sxs-lookup"><span data-stu-id="a2994-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="a2994-172">Messages de notification appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-172">Appbar Notification Messages</span></span>

<span data-ttu-id="a2994-173">Le système envoie des messages pour notifier un appbar sur les événements qui peuvent affecter sa position et son apparence.</span><span class="sxs-lookup"><span data-stu-id="a2994-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="a2994-174">Les messages sont envoyés dans le contexte d’un message défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="a2994-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="a2994-175">L’application spécifie l’identificateur du message lorsqu’il envoie le [**\_ nouveau message ABM**](abm-new.md) pour inscrire le appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="a2994-176">Le code de notification se trouve dans le paramètre *wParam* du message défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="a2994-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="a2994-177">Un appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) lorsque la taille, la position ou l’état de visibilité de la barre des tâches change, lorsqu’un autre appbar est ajouté au même bord de l’écran ou lorsqu’un autre appbar sur le même bord de l’écran est redimensionné ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="a2994-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="a2994-178">Un appbar doit répondre à ce message de notification en envoyant des messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="a2994-179">Si la position d’un appbar a changé, elle doit appeler la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour se déplacer vers la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="a2994-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="a2994-180">Le système envoie le message de notification [**ABN \_ STATECHANGE**](abn-statechange.md) chaque fois que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé, c’est-à-dire lorsque l’utilisateur active ou désactive la case à cocher **toujours visible** ou **Masquer automatiquement** dans la feuille de propriétés de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2994-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="a2994-181">Un appbar peut utiliser ce message de notification pour définir son état sur conforme à celui de la barre des tâches, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="a2994-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="a2994-182">Lors du démarrage d’une application en plein écran ou de la fermeture de la dernière application en plein écran, un appbar reçoit le message de notification [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="a2994-183">Le paramètre *lParam* indique si l’application en plein écran est en mode d’ouverture ou de fermeture.</span><span class="sxs-lookup"><span data-stu-id="a2994-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="a2994-184">S’il s’ouvre, le appbar doit se placer au bas de l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="a2994-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="a2994-185">Le appbar doit restaurer sa position d’ordre de plan lorsque la dernière application en plein écran a été fermée.</span><span class="sxs-lookup"><span data-stu-id="a2994-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="a2994-186">Un appbar reçoit le message de notification [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) lorsque l’utilisateur sélectionne la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2994-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="a2994-187">Le système envoie le message deux fois, avant de réorganiser les fenêtres (*lParam* a la **valeur true**) et après avoir organisé les fenêtres (*lParam* a la **valeur false**).</span><span class="sxs-lookup"><span data-stu-id="a2994-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="a2994-188">Un appbar peut utiliser des messages [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) pour s’exclure de l’opération en cascade ou en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="a2994-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="a2994-189">Pour exclure lui-même, appbar doit se masquer quand *lParam* a la **valeur true** et s’afficher lui-même lorsque *lParam* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="a2994-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="a2994-190">Si un appbar se masque lui-même en réponse à ce message, il n’a pas besoin d’envoyer les messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) en réponse à l’opération en cascade ou en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="a2994-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="a2994-191">Inscription d’une barre d’outils de bureau d’application</span><span class="sxs-lookup"><span data-stu-id="a2994-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="a2994-192">Une application doit inscrire un appbar en envoyant le [**\_ nouveau message ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a2994-193">L’inscription d’un appbar l’ajoute à la liste interne du système et fournit au système un identificateur de message à utiliser pour envoyer des messages de notification à appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="a2994-194">Avant de quitter, une application doit annuler l’inscription de la appbar en envoyant le message [**ABM \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="a2994-195">L’annulation de l’inscription supprime le appbar de la liste interne du système et empêche la barre de recevoir des messages de notification appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="a2994-196">La fonction dans l’exemple suivant enregistre ou annule l’enregistrement d’un appbar, en fonction de la valeur d’un paramètre d’indicateur booléen.</span><span class="sxs-lookup"><span data-stu-id="a2994-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="a2994-197">Définition de la taille et de la position appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="a2994-198">Une application doit définir la taille et la position d’un appbar après avoir inscrit le appbar, une fois que l’utilisateur utilisateur a déplacé ou dimensionné le appbar, et chaque fois que le appbar reçoit le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="a2994-199">Avant de définir la taille et la position du appbar, l’application interroge le système pour obtenir un rectangle englobant approuvé en envoyant le message [**ABM \_ QUERYPOS**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="a2994-200">Le système retourne un rectangle englobant qui n’interfère pas avec la barre des tâches ou tout autre appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="a2994-201">Le système ajuste le rectangle simplement par soustraction de rectangle ; il ne fait aucun effort pour conserver la taille initiale du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a2994-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="a2994-202">Pour cette raison, le appbar doit réajuster le rectangle, si nécessaire, après l’envoi de **ABM \_ QUERYPOS**.</span><span class="sxs-lookup"><span data-stu-id="a2994-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="a2994-203">Ensuite, l’application transmet le rectangle englobant au système à l’aide du message [**ABM \_ SetPos**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="a2994-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="a2994-204">Ensuite, il appelle la fonction [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) pour déplacer le appbar dans la position.</span><span class="sxs-lookup"><span data-stu-id="a2994-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="a2994-205">L’exemple suivant montre comment définir la taille et la position d’un appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="a2994-206">Traitement des messages de notification appbar</span><span class="sxs-lookup"><span data-stu-id="a2994-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="a2994-207">Un appbar reçoit un message de notification lorsque l’état de la barre des tâches change, lorsqu’une application en plein écran démarre (ou lorsque la dernière se ferme), ou lorsqu’un événement peut affecter la taille et la position du appbar.</span><span class="sxs-lookup"><span data-stu-id="a2994-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="a2994-208">L’exemple suivant montre comment traiter les différents messages de notification.</span><span class="sxs-lookup"><span data-stu-id="a2994-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="a2994-209">La fonction suivante ajuste le rectangle englobant d’un appbar, puis appelle la fonction AppBarQuerySetPos définie par l’application (incluse dans la section précédente) pour définir la taille et la position de la barre en conséquence.</span><span class="sxs-lookup"><span data-stu-id="a2994-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
