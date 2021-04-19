---
description: Le .NET Framework a un modèle de sécurité qui traite différemment les applications en fonction de leur origine.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Sécurité et confiance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e3039f8aa93c2ae563a918177462cd09a217af
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106524762"
---
# <a name="security-and-trust"></a>Sécurité et confiance

Le .NET Framework a un modèle de sécurité qui traite différemment les applications en fonction de leur origine. Les fichiers exécutables et les assemblys qui proviennent de l’ordinateur d’un utilisateur s’exécutent généralement avec une confiance totale ; les mêmes exécutables et assemblys exécutés sur Internet s’exécutent généralement avec une confiance partielle. Cela permet d’empêcher du code malveillant de lire ou de modifier les informations auxquelles il ne doit pas avoir accès, telles que les fichiers locaux, les éléments dans le presse-papiers et d’autres ressources. Si un exécutable appelle un assembly, qui à son tour appelle un autre assembly qui requiert un certain niveau de confiance, le niveau de confiance le plus bas de tous les composants de la chaîne est appliqué. Toutefois, un administrateur sur un ordinateur peut définir des autorisations spécifiques qui remplacent les autorisations par défaut.

Une vue d’ensemble du modèle de sécurité est fournie dans les [contrôles Light-Weight Client-Side sécurisés](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer), et vous pouvez obtenir plus de détails sur le modèle de sécurité dans la [sécurité d’accès du code dans la pratique](/previous-versions/msp-n-p/ff648663(v=pandp.10)). Une bonne vue d’ensemble de la sécurité des bibliothèques (qui est particulièrement importante pour les objets [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) sur une page Web) est disponible dans [utilisation de bibliothèques à partir de code d’un niveau de confiance partiel](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp), et d’autres informations de sécurité sur les contrôles managés sont disponibles dans [écriture de contrôles managés sécurisés](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Autorisations

La plupart des objets et membres gérés dans l’API des technologies Tablet PC ont deux conditions requises :

-   L’exécution est toujours obligatoire.
-   FullTrust est requis lorsque l’action de sécurité [InheritanceDemand](/previous-versions/windows/) a lieu. Cela signifie qu’une confiance totale est requise lorsqu’une classe dérivée hérite d’une classe ou remplace une méthode du kit de développement logiciel (SDK) Tablet PC.

Le tableau suivant répertorie les classes et les membres qui requièrent des autorisations supplémentaires. Les autorisations pour une classe donnée s’appliquent également à tous ses membres non listés dans ce tableau.



| Classe ou méthode                                                                       | Autorisations                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard. OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Collecte**](inkcollector-class.md)                                            | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Descripteur InkCollector.                                                                   | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (voir la remarque ci-dessous)<br/> |
| InkEdit                                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (voir la remarque ci-dessous)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [PenInputPanel](/previous-versions/aa514041(v=msdn.10))                             | Voir la remarque ci-dessous.<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Dessin**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderr. InkSpaceToPixel (IntPtr, point), Renderr. InkSpaceToPixel (IntPtr \[ , point) \]    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderr. PixelToInkSpace (IntPtr, point), Renderr. PixelToInkSpace (IntPtr \[ , point) \]    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**Participent**](realtimestylus-class.md)                                        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, Boolean), RealTimeStylus (IntPtr, tablette) | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) et [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Il est généralement préférable d’utiliser un contrôle plutôt qu’un handle (IntPtr) pour les constructeurs, car les contrôles requièrent moins d’autorisations. De même, il est préférable d’utiliser un objet Graphics au lieu d’un handle pour [renderr. Draw](/previous-versions/ms828488(v=msdn.10)), [renderr. InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) et [renderr. PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)).

 

> [!Note]  
> Les propriétés [InkCollector. handle](/previous-versions/ms836504(v=msdn.10)) et [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10)) n’ont pas besoin de l’autorisation [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) si le handle est destiné à un contrôle Windows Forms, mais pour d’autres fenêtres.

 

> [!Note]  
> Pour la [classe PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , les méthodes et propriétés suivantes requièrent [SecurityPermissionFlag. AllFlags](/previous-versions/windows/): PenInputPanel (IntPtr), [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)), [occupé](/previous-versions/ms571975(v=vs.100)), [CommitPendingInput](/previous-versions/ms569650(v=vs.100)), [CurrentPanel](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), [EnableTsf](/previous-versions/ms569656(v=vs.100)), [Factoid](/previous-versions/ms571978(v=vs.100)), [Height](/previous-versions/ms571979(v=vs.100)), [HorizontalOffset](/previous-versions/ms571980(v=vs.100)), [InputFailed](/previous-versions/ms567738(v=vs.100)), [gauche](/previous-versions/ms571981(v=vs.100)), [MoveTo](/previous-versions/ms569667(v=vs.100)), [PanelChanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Refresh](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))et [Width](/previous-versions/ms571985(v=vs.100)).

 

## <a name="other-considerations"></a>Autres considérations

D’autres considérations de sécurité connues sont les suivantes :

-   Microsoft Internet Explorer 6 ou version ultérieure est requis pour que les contrôles Web fonctionnent correctement. Avec Internet Explorer 5,5, seuls les contrôles managés initiaux sont chargés. vous ne pouvez pas charger dynamiquement des contrôles supplémentaires au moment de l’exécution.
-   Si vous utilisez Windows XP Service Pack 2 (SP2) et CLR 1.0, les contrôles Web dans Internet Explorer nécessitent l’ajout du site en tant que site de confiance, même s’ils se trouvent dans la zone intranet. Toutefois, dans ce cas, ils ne s’exécuteront plus dans la zone de sites de confiance, bien qu’ils soient exécutés dans la zone intranet. Ce problème est résolu avec CLR 1.1.

 

 