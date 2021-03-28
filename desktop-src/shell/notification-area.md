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
# <a name="notifications-and-the-notification-area"></a>Notifications et zone de notification

La zone de notification est une partie de la barre des tâches qui fournit une source temporaire pour les notifications et l’État. Elle peut également être utilisée pour afficher des icônes pour les fonctionnalités système et de programme qui n’ont pas de présence sur le bureau, telles que le niveau de la batterie, le contrôle du volume et l’état du réseau. La zone de notification est connue historiquement sous la forme d’une barre d’état système ou d’une zone d’État.

Cette rubrique contient les sections suivantes :

-   [Instructions relatives à la notification et à la zone de notification](#notification-and-notification-area-guidelines)
-   [Création et affichage d’une notification](#notifications-and-the-notification-area)
    -   [Icône Ajouter une notification](#add-a-notification-icon)
    -   [Définir la version de NOTIFYICONDATA](#define-the-notifyicondata-version)
    -   [Définir l’apparence et le contenu de la notification](#define-the-notification-look-and-contents)
    -   [Vérifier l’état de l’utilisateur](#check-the-user-status)
    -   [Afficher la notification](#display-the-notification)
    -   [Suppression d’une icône](#removing-an-icon)
-   [Exemple SDK](#sdk-sample)
-   [Rubriques connexes](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>Instructions relatives à la notification et à la zone de notification

Consultez les sections [notifications](../uxguide/mess-notif.md) et [zone de notification](../uxguide/winenv-notification.md) des instructions d’interaction avec l’expérience utilisateur Windows pour connaître les meilleures pratiques en matière d’utilisation des notifications et de la zone de notification. L’objectif est de fournir l’avantage de l’utilisateur via une utilisation appropriée des notifications, sans être ennuyeux ou gênant.

La zone de notification ne concerne pas les informations critiques qui doivent être traitées immédiatement. Il n’est pas non plus prévu pour un accès rapide aux programmes ou aux commandes. À compter de Windows 7, une grande partie de cette fonctionnalité est la meilleure possible via le bouton de la barre des tâches d’une application.

Windows 7 permet à un utilisateur de supprimer toutes les notifications d’une application, le cas échéant. une conception et une utilisation de notification réfléchies inclinent l’utilisateur pour permettre à votre application de continuer à les afficher. Les notifications sont une interruption ; Assurez-vous qu’elles en valent la chance.

Windows 7 introduit le concept de « temps silencieux ». L’heure de silence est définie comme la première heure après qu’un nouvel utilisateur s’est connecté à son compte pour la première fois, ou pour la première fois après une mise à niveau du système d’exploitation ou une nouvelle installation. Cette durée est réservée pour permettre à l’utilisateur d’explorer et de se familiariser avec le nouvel environnement sans la gêne des notifications. Pendant ce temps, la plupart des notifications ne doivent pas être envoyées ni affichées. Les exceptions incluent les commentaires que l’utilisateur s’attend à voir en réponse à une action de l’utilisateur, par exemple lorsqu’il se connecte à un périphérique USB ou imprime un document. Les caractéristiques de l’API relatives à l’heure de silence sont abordées plus loin dans cette rubrique.

## <a name="creating-and-displaying-a-notification"></a>Création et affichage d’une notification

Les sections restantes de cette rubrique décrivent la procédure de base à suivre pour afficher une notification de votre application à l’utilisateur.

1.  [Icône Ajouter une notification](#add-a-notification-icon)
2.  [Définir la version de NOTIFYICONDATA](#define-the-notifyicondata-version)
3.  [Définir l’apparence et le contenu de la notification](#define-the-notification-look-and-contents)
4.  [Vérifier l’état de l’utilisateur](#check-the-user-status)
5.  [Afficher la notification](#display-the-notification)
6.  [Suppression d’une icône](#removing-an-icon)

### <a name="add-a-notification-icon"></a>Icône Ajouter une notification

Pour afficher une notification, vous devez disposer d’une icône dans la zone de notification. Dans certains cas, tels que Microsoft Communicator ou le niveau de batterie, cette icône est déjà présente. Toutefois, dans de nombreux autres cas, vous allez ajouter une icône à la zone de notification uniquement si nécessaire pour afficher la notification. Dans les deux cas, cela s’effectue à l’aide de la fonction [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) . **Shell \_ NotifyIcon** vous permet d’ajouter, de modifier ou de supprimer une icône dans la zone de notification.

![zone de notification contenant trois icônes](images/taskbar/notificationareaicons.png)

Quand une icône est ajoutée à la zone de notification sur Windows 7, elle est ajoutée à la section de dépassement de capacité de la zone de notification par défaut. Cette zone contient les icônes de la zone de notification qui sont actives, mais qui ne sont pas visibles dans la zone de notification. Seul l’utilisateur peut promouvoir une icône du dépassement de capacité vers la zone de notification, même si, dans certaines circonstances, le système peut promouvoir temporairement une icône dans la zone de notification sous la forme d’un bref aperçu (sous une minute).

> [!Note]  
> L’utilisateur doit avoir l’affirmation finale sur les icônes qu’il souhaite voir dans sa zone de notification. Avant d’installer une icône non transitoire dans la zone de notification, l’utilisateur doit être invité à fournir l’autorisation. Ils doivent également recevoir l’option (normalement, par le biais de son menu contextuel) pour supprimer l’icône de la zone de notification.

 

La structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) envoyée dans l’appel à la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contient des informations qui spécifient à la fois l’icône de la zone de notification et la notification elle-même. Voici les éléments spécifiques à l’icône de zone de notification proprement dite qui peut être définie par l’intermédiaire de **NOTIFYICONDATA**.

-   Ressource à partir de laquelle l’icône est prise.
-   Identificateur unique de l’icône.
-   Style de l’info-bulle de l’icône.
-   État de l’icône (masqué, partagé ou les deux) dans la zone de notification.
-   Handle d’une fenêtre d’application associée à l’icône.
-   Identificateur du message de rappel qui permet à l’icône de communiquer les événements qui se produisent dans le rectangle englobant de l’icône et la notification du ballon avec la fenêtre d’application associée. Le rectangle englobant de l’icône peut être récupéré via l' [**interpréteur de commandes \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).

Chaque icône de la zone de notification peut être identifiée de deux manières :

-   GUID avec lequel l’icône est déclarée dans le registre. Il s’agit de la méthode recommandée sur Windows 7 et versions ultérieures.
-   Handle d’une fenêtre associée à l’icône de la zone de notification, plus un identificateur d’icône défini par l’application. Cette méthode est utilisée sur Windows Vista et les versions antérieures.

Les icônes de la zone de notification peuvent avoir une info-bulle. L’info-bulle peut être une info-bulle standard (par défaut) ou une interface utilisateur dessinée, indépendante de l’application. Une info-bulle n’est pas obligatoire, mais elle est recommandée.

Les icônes de la zone de notification doivent être compatibles haute résolution. Une application doit fournir une icône de pixel de 16x16 et une icône 32x32 dans son fichier de ressources, puis utiliser [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) pour garantir que l’icône correcte est chargée et mise à l’échelle de manière appropriée.

L’application responsable de l’icône de la zone de notification doit gérer un clic de souris pour cette icône. Quand un utilisateur clique avec le bouton droit sur l’icône, il doit afficher un menu contextuel normal. Toutefois, le résultat d’un clic avec le bouton gauche de la souris dépend de la fonction de l’icône. Elle doit afficher ce que l’utilisateur s’attend à voir dans le formulaire le mieux adapté à ce contenu : une fenêtre contextuelle, une boîte de dialogue ou la fenêtre de programme proprement dite. Par exemple, il peut afficher le texte d’état d’une icône d’État ou un curseur pour le contrôle du volume.

L’emplacement d’une fenêtre contextuelle ou d’une boîte de dialogue qui résulte du clic doit être placé près de la coordonnée du clic dans la zone de notification. Utilisez [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) pour déterminer son emplacement.

L’icône peut être ajoutée à la zone de notification sans afficher de notification en définissant uniquement les membres spécifiques aux icônes de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (voir ci-dessus) et en appelant [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) comme indiqué ici :


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



Vous pouvez également ajouter l’icône à la zone de notification et afficher une notification tous en un seul appel à l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes. Pour ce faire, suivez les instructions de cette rubrique.

### <a name="define-the-notifyicondata-version"></a>Définir la version de NOTIFYICONDATA

Lorsque Windows a progressé, la structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) a été développée pour inclure davantage de membres afin de définir davantage de fonctionnalités. Les constantes sont utilisées pour déclarer la version de **NOTIFYICONDATA** à utiliser avec votre icône de zone de notification, afin de permettre la compatibilité descendante. À moins qu’il y ait une raison impérieuse de faire autrement, il est fortement recommandé d’utiliser la \_ version \_ de NOTIFYICON version 4, introduite dans Windows Vista. Cette version fournit toutes les fonctionnalités disponibles, notamment la possibilité d’identifier l’icône de la zone de notification via un GUID inscrit, un mécanisme de rappel supérieur et une meilleure accessibilité.

Définissez la version à l’aide des appels suivants :


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



Notez que cet appel à l' [**interface \_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) n’affiche pas de notification.

### <a name="define-the-notification-look-and-contents"></a>Définir l’apparence et le contenu de la notification

Une notification est un type spécial de contrôle ToolTip info-bulle. Elle contient un titre, un corps de texte et une icône. Comme une fenêtre, elle a un bouton **Fermer** dans son coin supérieur droit. Elle contient également un bouton **options** qui ouvre l’élément icônes de la zone de notification dans le panneau de configuration, ce qui permet à l’utilisateur d’afficher ou de masquer l’icône ou d’afficher uniquement les notifications sans icône.

![capture d’écran de la bulle de notification indiquant que la puissance de la batterie est faible](images/taskbar/notificationballoon.png)

La structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) envoyée dans l’appel à la [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contient des informations qui spécifient à la fois l’icône de la zone de notification et la bulle de notification. Voici les éléments spécifiques à la notification qui peuvent être définis par le biais de **NOTIFYICONDATA**.

-   Icône à afficher dans la bulle de notification, spécifiée par le type de notification. La taille de l’icône peut être spécifiée, ainsi que des icônes personnalisées.
-   Titre de la notification. Ce titre doit contenir jusqu’à 48 caractères en anglais (pour prendre en charge la localisation). Le titre est la première ligne de la notification et est défini à l’aide de la taille de police, de la couleur et de la pondération.
-   Texte à utiliser dans le corps de la notification. Ce texte ne doit pas dépasser 200 caractères en anglais (pour prendre en charge la localisation).
-   Indique si la notification doit être ignorée si elle ne peut pas être affichée immédiatement.
-   Délai d’attente de la notification. Ce paramètre est ignoré dans les systèmes Windows Vista et versions ultérieures, en faveur d’un paramètre de délai d’accessibilité à l’ensemble du système.
-   Indique si la notification doit respecter le temps de silence, définie à l’aide du drapeau [**NIIF \_ respecter le \_ \_ temps de silence**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .

> [!Note]  
> Les interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) et [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) sont des wrappers de modèle COM (Component Object Model) pour [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Toutefois, à ce stade, ils ne fournissent pas \_ directement la fonctionnalité NotifyIcon version 4 complète \_ disponible par le biais de l' **interface \_ NotifyIcon Shell** , y compris l’utilisation d’un GUID pour identifier l’icône de la zone de notification.

 

### <a name="check-the-user-status"></a>Vérifier l’état de l’utilisateur

Le système utilise la fonction [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) pour vérifier si l’utilisateur est en mode silencieux, s’éloigner de l’ordinateur ou dans un État ininterrompu, tel que le mode de présentation. Le fait que le système affiche votre notification dépend de cet État.

> [!Note]  
> Si votre application utilise une méthode de notification personnalisée qui n’utilise pas [**l' \_ interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes shell, [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)ou [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), elle doit toujours appeler explicitement [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) pour déterminer si elle doit afficher l’interface utilisateur de notification à ce moment-là.

 

Les notifications envoyées lorsque l’utilisateur est absent sont mises en file d’attente pour l’affichage, mais comme vous ne pouvez pas savoir à quel moment l’utilisateur sera renvoyé ou si la notification sera toujours valide à ce moment-là, vous pouvez envisager de renvoyer la notification ultérieurement.

Les notifications envoyées pendant une période de silence sont ignorées. Les instructions de conception demandent que toutes les notifications soient ignorables. Ils ne doivent pas nécessiter une action immédiate de l’utilisateur. Par conséquent, aucune notification n’est si importante qu’elle doit remplacer le temps silencieux.

### <a name="display-the-notification"></a>Afficher la notification

Une fois que vous avez défini la version de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) et que vous avez défini la notification dans une structure **NOTIFYICONDATA** , appelez l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) pour afficher l’icône.

-   Si l’icône de la zone de notification n’est pas présente, appelez l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) pour ajouter l’icône. Procédez ainsi pour les icônes temporaires et non temporaires.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   Si l’icône de la zone de notification est déjà présente, appelez l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes pour modifier l’icône.
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

Le code suivant montre un exemple de définition de données [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) et de leur envoi via [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona). Notez que cet exemple identifie l’icône de notification via un GUID (par défaut dans Windows 7).


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



### <a name="removing-an-icon"></a>Suppression d’une icône

Pour supprimer une icône, par exemple, lorsque vous avez uniquement ajouté temporairement l’icône pour diffuser une notification, appelez la fonction [**\_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes comme indiqué ici. Seule une structure [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) minimale qui identifie l’icône est nécessaire dans cet appel.


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> Quand une application est désinstallée, son icône de zone de notification peut toujours apparaître à l’utilisateur en tant qu’option dans la page icônes de la zone de notification dans le panneau de configuration pendant sept jours. Toutefois, toutes les modifications apportées sont sans effet.

 

## <a name="sdk-sample"></a>Exemple SDK

Consultez l’exemple d’exemple [NotificationIcon](samples-notificationicon.md) dans le kit de développement logiciel (SDK) Windows pour obtenir un exemple complet de l’utilisation de l' [**interface \_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)de commandes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[La barre des tâches](taskbar.md)
</dt> <dt>

[Extensions de la barre des tâches](taskbar-extensions.md)
</dt> </dl>

 

 
