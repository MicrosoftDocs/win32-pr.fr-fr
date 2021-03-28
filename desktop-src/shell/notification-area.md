---
description: La zone de notification est une partie de la barre des tâches qui fournit une source temporaire pour les notifications et l’État.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notifications et zone de notification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318633"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="eb182-103">Notifications et zone de notification</span><span class="sxs-lookup"><span data-stu-id="eb182-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="eb182-104">La zone de notification est une partie de la barre des tâches qui fournit une source temporaire pour les notifications et l’État.</span><span class="sxs-lookup"><span data-stu-id="eb182-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="eb182-105">Elle peut également être utilisée pour afficher des icônes pour les fonctionnalités système et de programme qui n’ont pas de présence sur le bureau, telles que le niveau de la batterie, le contrôle du volume et l’état du réseau.</span><span class="sxs-lookup"><span data-stu-id="eb182-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="eb182-106">La zone de notification est connue historiquement sous la forme d’une barre d’état système ou d’une zone d’État.</span><span class="sxs-lookup"><span data-stu-id="eb182-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="eb182-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb182-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="eb182-108">Instructions relatives à la notification et à la zone de notification</span><span class="sxs-lookup"><span data-stu-id="eb182-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="eb182-109">Création et affichage d’une notification</span><span class="sxs-lookup"><span data-stu-id="eb182-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="eb182-110">Icône Ajouter une notification</span><span class="sxs-lookup"><span data-stu-id="eb182-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="eb182-111">Définir la version de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="eb182-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="eb182-112">Définir l’apparence et le contenu de la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="eb182-113">Vérifier l’état de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb182-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="eb182-114">Afficher la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="eb182-115">Suppression d’une icône</span><span class="sxs-lookup"><span data-stu-id="eb182-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="eb182-116">Exemple SDK</span><span class="sxs-lookup"><span data-stu-id="eb182-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="eb182-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb182-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="eb182-118">Instructions relatives à la notification et à la zone de notification</span><span class="sxs-lookup"><span data-stu-id="eb182-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="eb182-119">Consultez les sections [notifications](../uxguide/mess-notif.md) et [zone de notification](../uxguide/winenv-notification.md) des instructions d’interaction avec l’expérience utilisateur Windows pour connaître les meilleures pratiques en matière d’utilisation des notifications et de la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="eb182-120">L’objectif est de fournir l’avantage de l’utilisateur via une utilisation appropriée des notifications, sans être ennuyeux ou gênant.</span><span class="sxs-lookup"><span data-stu-id="eb182-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="eb182-121">La zone de notification ne concerne pas les informations critiques qui doivent être traitées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="eb182-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="eb182-122">Il n’est pas non plus prévu pour un accès rapide aux programmes ou aux commandes.</span><span class="sxs-lookup"><span data-stu-id="eb182-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="eb182-123">À compter de Windows 7, une grande partie de cette fonctionnalité est la meilleure possible via le bouton de la barre des tâches d’une application.</span><span class="sxs-lookup"><span data-stu-id="eb182-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="eb182-124">Windows 7 permet à un utilisateur de supprimer toutes les notifications d’une application, le cas échéant. une conception et une utilisation de notification réfléchies inclinent l’utilisateur pour permettre à votre application de continuer à les afficher.</span><span class="sxs-lookup"><span data-stu-id="eb182-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="eb182-125">Les notifications sont une interruption ; Assurez-vous qu’elles en valent la chance.</span><span class="sxs-lookup"><span data-stu-id="eb182-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="eb182-126">Windows 7 introduit le concept de « temps silencieux ».</span><span class="sxs-lookup"><span data-stu-id="eb182-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="eb182-127">L’heure de silence est définie comme la première heure après qu’un nouvel utilisateur s’est connecté à son compte pour la première fois, ou pour la première fois après une mise à niveau du système d’exploitation ou une nouvelle installation.</span><span class="sxs-lookup"><span data-stu-id="eb182-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="eb182-128">Cette durée est réservée pour permettre à l’utilisateur d’explorer et de se familiariser avec le nouvel environnement sans la gêne des notifications.</span><span class="sxs-lookup"><span data-stu-id="eb182-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="eb182-129">Pendant ce temps, la plupart des notifications ne doivent pas être envoyées ni affichées.</span><span class="sxs-lookup"><span data-stu-id="eb182-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="eb182-130">Les exceptions incluent les commentaires que l’utilisateur s’attend à voir en réponse à une action de l’utilisateur, par exemple lorsqu’il se connecte à un périphérique USB ou imprime un document.</span><span class="sxs-lookup"><span data-stu-id="eb182-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="eb182-131">Les caractéristiques de l’API relatives à l’heure de silence sont abordées plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="eb182-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="eb182-132">Création et affichage d’une notification</span><span class="sxs-lookup"><span data-stu-id="eb182-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="eb182-133">Les sections restantes de cette rubrique décrivent la procédure de base à suivre pour afficher une notification de votre application à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb182-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="eb182-134">Icône Ajouter une notification</span><span class="sxs-lookup"><span data-stu-id="eb182-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="eb182-135">Définir la version de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="eb182-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="eb182-136">Définir l’apparence et le contenu de la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="eb182-137">Vérifier l’état de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb182-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="eb182-138">Afficher la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="eb182-139">Suppression d’une icône</span><span class="sxs-lookup"><span data-stu-id="eb182-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="eb182-140">Icône Ajouter une notification</span><span class="sxs-lookup"><span data-stu-id="eb182-140">Add a Notification Icon</span></span>

<span data-ttu-id="eb182-141">Pour afficher une notification, vous devez disposer d’une icône dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="eb182-142">Dans certains cas, tels que Microsoft Communicator ou le niveau de batterie, cette icône est déjà présente.</span><span class="sxs-lookup"><span data-stu-id="eb182-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="eb182-143">Toutefois, dans de nombreux autres cas, vous allez ajouter une icône à la zone de notification uniquement si nécessaire pour afficher la notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="eb182-144">Dans les deux cas, cela s’effectue à l’aide de la fonction [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="eb182-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="eb182-145">**Shell \_ NotifyIcon** vous permet d’ajouter, de modifier ou de supprimer une icône dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![zone de notification contenant trois icônes](images/taskbar/notificationareaicons.png)

<span data-ttu-id="eb182-147">Quand une icône est ajoutée à la zone de notification sur Windows 7, elle est ajoutée à la section de dépassement de capacité de la zone de notification par défaut.</span><span class="sxs-lookup"><span data-stu-id="eb182-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="eb182-148">Cette zone contient les icônes de la zone de notification qui sont actives, mais qui ne sont pas visibles dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="eb182-149">Seul l’utilisateur peut promouvoir une icône du dépassement de capacité vers la zone de notification, même si, dans certaines circonstances, le système peut promouvoir temporairement une icône dans la zone de notification sous la forme d’un bref aperçu (sous une minute).</span><span class="sxs-lookup"><span data-stu-id="eb182-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="eb182-150">L’utilisateur doit avoir l’affirmation finale sur les icônes qu’il souhaite voir dans sa zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="eb182-151">Avant d’installer une icône non transitoire dans la zone de notification, l’utilisateur doit être invité à fournir l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="eb182-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="eb182-152">Ils doivent également recevoir l’option (normalement, par le biais de son menu contextuel) pour supprimer l’icône de la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="eb182-153">La structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) envoyée dans l’appel à la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contient des informations qui spécifient à la fois l’icône de la zone de notification et la notification elle-même.</span><span class="sxs-lookup"><span data-stu-id="eb182-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="eb182-154">Voici les éléments spécifiques à l’icône de zone de notification proprement dite qui peut être définie par l’intermédiaire de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="eb182-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="eb182-155">Ressource à partir de laquelle l’icône est prise.</span><span class="sxs-lookup"><span data-stu-id="eb182-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="eb182-156">Identificateur unique de l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="eb182-157">Style de l’info-bulle de l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="eb182-158">État de l’icône (masqué, partagé ou les deux) dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="eb182-159">Handle d’une fenêtre d’application associée à l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="eb182-160">Identificateur du message de rappel qui permet à l’icône de communiquer les événements qui se produisent dans le rectangle englobant de l’icône et la notification du ballon avec la fenêtre d’application associée.</span><span class="sxs-lookup"><span data-stu-id="eb182-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="eb182-161">Le rectangle englobant de l’icône peut être récupéré via l' [**interpréteur de commandes \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span><span class="sxs-lookup"><span data-stu-id="eb182-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="eb182-162">Chaque icône de la zone de notification peut être identifiée de deux manières :</span><span class="sxs-lookup"><span data-stu-id="eb182-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="eb182-163">GUID avec lequel l’icône est déclarée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="eb182-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="eb182-164">Il s’agit de la méthode recommandée sur Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb182-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="eb182-165">Handle d’une fenêtre associée à l’icône de la zone de notification, plus un identificateur d’icône défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="eb182-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="eb182-166">Cette méthode est utilisée sur Windows Vista et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="eb182-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="eb182-167">Les icônes de la zone de notification peuvent avoir une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="eb182-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="eb182-168">L’info-bulle peut être une info-bulle standard (par défaut) ou une interface utilisateur dessinée, indépendante de l’application.</span><span class="sxs-lookup"><span data-stu-id="eb182-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="eb182-169">Une info-bulle n’est pas obligatoire, mais elle est recommandée.</span><span class="sxs-lookup"><span data-stu-id="eb182-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="eb182-170">Les icônes de la zone de notification doivent être compatibles haute résolution.</span><span class="sxs-lookup"><span data-stu-id="eb182-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="eb182-171">Une application doit fournir une icône de pixel de 16x16 et une icône 32x32 dans son fichier de ressources, puis utiliser [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) pour garantir que l’icône correcte est chargée et mise à l’échelle de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="eb182-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="eb182-172">L’application responsable de l’icône de la zone de notification doit gérer un clic de souris pour cette icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="eb182-173">Quand un utilisateur clique avec le bouton droit sur l’icône, il doit afficher un menu contextuel normal.</span><span class="sxs-lookup"><span data-stu-id="eb182-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="eb182-174">Toutefois, le résultat d’un clic avec le bouton gauche de la souris dépend de la fonction de l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="eb182-175">Elle doit afficher ce que l’utilisateur s’attend à voir dans le formulaire le mieux adapté à ce contenu : une fenêtre contextuelle, une boîte de dialogue ou la fenêtre de programme proprement dite.</span><span class="sxs-lookup"><span data-stu-id="eb182-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="eb182-176">Par exemple, il peut afficher le texte d’état d’une icône d’État ou un curseur pour le contrôle du volume.</span><span class="sxs-lookup"><span data-stu-id="eb182-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="eb182-177">L’emplacement d’une fenêtre contextuelle ou d’une boîte de dialogue qui résulte du clic doit être placé près de la coordonnée du clic dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="eb182-178">Utilisez [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) pour déterminer son emplacement.</span><span class="sxs-lookup"><span data-stu-id="eb182-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="eb182-179">L’icône peut être ajoutée à la zone de notification sans afficher de notification en définissant uniquement les membres spécifiques aux icônes de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (voir ci-dessus) et en appelant [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="eb182-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="eb182-180">Vous pouvez également ajouter l’icône à la zone de notification et afficher une notification tous en un seul appel à l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes.</span><span class="sxs-lookup"><span data-stu-id="eb182-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="eb182-181">Pour ce faire, suivez les instructions de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="eb182-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="eb182-182">Définir la version de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="eb182-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="eb182-183">Lorsque Windows a progressé, la structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) a été développée pour inclure davantage de membres afin de définir davantage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="eb182-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="eb182-184">Les constantes sont utilisées pour déclarer la version de **NOTIFYICONDATA** à utiliser avec votre icône de zone de notification, afin de permettre la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="eb182-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="eb182-185">À moins qu’il y ait une raison impérieuse de faire autrement, il est fortement recommandé d’utiliser la \_ version \_ de NOTIFYICON version 4, introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb182-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="eb182-186">Cette version fournit toutes les fonctionnalités disponibles, notamment la possibilité d’identifier l’icône de la zone de notification via un GUID inscrit, un mécanisme de rappel supérieur et une meilleure accessibilité.</span><span class="sxs-lookup"><span data-stu-id="eb182-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="eb182-187">Définissez la version à l’aide des appels suivants :</span><span class="sxs-lookup"><span data-stu-id="eb182-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="eb182-188">Notez que cet appel à l' [**interface \_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) n’affiche pas de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="eb182-189">Définir l’apparence et le contenu de la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="eb182-190">Une notification est un type spécial de contrôle ToolTip info-bulle.</span><span class="sxs-lookup"><span data-stu-id="eb182-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="eb182-191">Elle contient un titre, un corps de texte et une icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="eb182-192">Comme une fenêtre, elle a un bouton **Fermer** dans son coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="eb182-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="eb182-193">Elle contient également un bouton **options** qui ouvre l’élément icônes de la zone de notification dans le panneau de configuration, ce qui permet à l’utilisateur d’afficher ou de masquer l’icône ou d’afficher uniquement les notifications sans icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![capture d’écran de la bulle de notification indiquant que la puissance de la batterie est faible](images/taskbar/notificationballoon.png)

<span data-ttu-id="eb182-195">La structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) envoyée dans l’appel à la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contient des informations qui spécifient à la fois l’icône de la zone de notification et la bulle de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="eb182-196">Voici les éléments spécifiques à la notification qui peuvent être définis par le biais de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="eb182-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="eb182-197">Icône à afficher dans la bulle de notification, spécifiée par le type de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="eb182-198">La taille de l’icône peut être spécifiée, ainsi que des icônes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="eb182-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="eb182-199">Titre de la notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-199">A notification title.</span></span> <span data-ttu-id="eb182-200">Ce titre doit contenir jusqu’à 48 caractères en anglais (pour prendre en charge la localisation).</span><span class="sxs-lookup"><span data-stu-id="eb182-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="eb182-201">Le titre est la première ligne de la notification et est défini à l’aide de la taille de police, de la couleur et de la pondération.</span><span class="sxs-lookup"><span data-stu-id="eb182-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="eb182-202">Texte à utiliser dans le corps de la notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="eb182-203">Ce texte ne doit pas dépasser 200 caractères en anglais (pour prendre en charge la localisation).</span><span class="sxs-lookup"><span data-stu-id="eb182-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="eb182-204">Indique si la notification doit être ignorée si elle ne peut pas être affichée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="eb182-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="eb182-205">Délai d’attente de la notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-205">A timeout for the notification.</span></span> <span data-ttu-id="eb182-206">Ce paramètre est ignoré dans les systèmes Windows Vista et versions ultérieures, en faveur d’un paramètre de délai d’accessibilité à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="eb182-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="eb182-207">Indique si la notification doit respecter le temps de silence, définie à l’aide du drapeau [**NIIF \_ respecter le \_ \_ temps de silence**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .</span><span class="sxs-lookup"><span data-stu-id="eb182-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="eb182-208">Les interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) et [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) sont des wrappers de modèle COM (Component Object Model) pour [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="eb182-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="eb182-209">Toutefois, à ce stade, ils ne fournissent pas \_ directement la fonctionnalité NotifyIcon version 4 complète \_ disponible par le biais de l' **interface \_ NotifyIcon Shell** , y compris l’utilisation d’un GUID pour identifier l’icône de la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="eb182-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="eb182-210">Vérifier l’état de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb182-210">Check the User Status</span></span>

<span data-ttu-id="eb182-211">Le système utilise la fonction [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) pour vérifier si l’utilisateur est en mode silencieux, s’éloigner de l’ordinateur ou dans un État ininterrompu, tel que le mode de présentation.</span><span class="sxs-lookup"><span data-stu-id="eb182-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="eb182-212">Le fait que le système affiche votre notification dépend de cet État.</span><span class="sxs-lookup"><span data-stu-id="eb182-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="eb182-213">Si votre application utilise une méthode de notification personnalisée qui n’utilise pas [**l' \_ interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes shell, [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)ou [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), elle doit toujours appeler explicitement [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) pour déterminer si elle doit afficher l’interface utilisateur de notification à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="eb182-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="eb182-214">Les notifications envoyées lorsque l’utilisateur est absent sont mises en file d’attente pour l’affichage, mais comme vous ne pouvez pas savoir à quel moment l’utilisateur sera renvoyé ou si la notification sera toujours valide à ce moment-là, vous pouvez envisager de renvoyer la notification ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="eb182-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="eb182-215">Les notifications envoyées pendant une période de silence sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="eb182-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="eb182-216">Les instructions de conception demandent que toutes les notifications soient ignorables.</span><span class="sxs-lookup"><span data-stu-id="eb182-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="eb182-217">Ils ne doivent pas nécessiter une action immédiate de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb182-217">They should not require immediate user action.</span></span> <span data-ttu-id="eb182-218">Par conséquent, aucune notification n’est si importante qu’elle doit remplacer le temps silencieux.</span><span class="sxs-lookup"><span data-stu-id="eb182-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="eb182-219">Afficher la notification</span><span class="sxs-lookup"><span data-stu-id="eb182-219">Display the Notification</span></span>

<span data-ttu-id="eb182-220">Une fois que vous avez défini la version de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) et que vous avez défini la notification dans une structure **NOTIFYICONDATA** , appelez l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) pour afficher l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="eb182-221">Si l’icône de la zone de notification n’est pas présente, appelez l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) pour ajouter l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="eb182-222">Procédez ainsi pour les icônes temporaires et non temporaires.</span><span class="sxs-lookup"><span data-stu-id="eb182-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="eb182-223">Si l’icône de la zone de notification est déjà présente, appelez l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes pour modifier l’icône.</span><span class="sxs-lookup"><span data-stu-id="eb182-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="eb182-224">Le code suivant montre un exemple de définition de données [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) et de leur envoi via [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="eb182-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="eb182-225">Notez que cet exemple identifie l’icône de notification via un GUID (par défaut dans Windows 7).</span><span class="sxs-lookup"><span data-stu-id="eb182-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="eb182-226">Suppression d’une icône</span><span class="sxs-lookup"><span data-stu-id="eb182-226">Removing an Icon</span></span>

<span data-ttu-id="eb182-227">Pour supprimer une icône, par exemple, lorsque vous avez uniquement ajouté temporairement l’icône pour diffuser une notification, appelez la fonction [**\_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="eb182-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="eb182-228">Seule une structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) minimale qui identifie l’icône est nécessaire dans cet appel.</span><span class="sxs-lookup"><span data-stu-id="eb182-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="eb182-229">Quand une application est désinstallée, son icône de zone de notification peut toujours apparaître à l’utilisateur en tant qu’option dans la page icônes de la zone de notification dans le panneau de configuration pendant sept jours.</span><span class="sxs-lookup"><span data-stu-id="eb182-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="eb182-230">Toutefois, toutes les modifications apportées sont sans effet.</span><span class="sxs-lookup"><span data-stu-id="eb182-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="eb182-231">Exemple SDK</span><span class="sxs-lookup"><span data-stu-id="eb182-231">SDK Sample</span></span>

<span data-ttu-id="eb182-232">Consultez l’exemple d’exemple [NotificationIcon](samples-notificationicon.md) dans le kit de développement logiciel (SDK) Windows pour obtenir un exemple complet de l’utilisation de l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes.</span><span class="sxs-lookup"><span data-stu-id="eb182-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb182-233">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb182-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb182-234">**\_NotifyIcon Shell**</span><span class="sxs-lookup"><span data-stu-id="eb182-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="eb182-235">**Shell \_ NotifyIconGetRect**</span><span class="sxs-lookup"><span data-stu-id="eb182-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="eb182-236">**NOTIFYICONDATA**</span><span class="sxs-lookup"><span data-stu-id="eb182-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="eb182-237">**SHQueryUserNotificationState**</span><span class="sxs-lookup"><span data-stu-id="eb182-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="eb182-238">**IUserNotification**</span><span class="sxs-lookup"><span data-stu-id="eb182-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="eb182-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="eb182-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="eb182-240">La barre des tâches</span><span class="sxs-lookup"><span data-stu-id="eb182-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="eb182-241">Extensions de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="eb182-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
