---
title: Développement d’applications bureautiques haute résolution sur Windows
description: Ce contenu est destiné aux développeurs qui cherchent à mettre à jour les applications de bureau pour gérer le facteur d’échelle d’affichage dynamique (également appelé
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01958791dccd7c836babedbe726233797eddb646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531309"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Développement d’applications bureautiques haute résolution sur Windows

Ce contenu est destiné aux développeurs qui cherchent à mettre à jour les applications de bureau pour gérer les modifications du facteur d’échelle d’affichage (points par pouce ou PPP) de manière dynamique, ce qui permet à leurs applications d’être nettes sur n’importe quel affichage sur lequel elles sont affichées.

pour commencer, si vous créez une nouvelle Windows application à partir de zéro, il est fortement recommandé de créer une application [plateforme Windows universelle (UWP)](/windows/uwp/get-started/whats-a-uwp) . Les applications UWP sont &mdash; mises à l’échelle de manière automatique et dynamique &mdash; pour chaque affichage sur lequel elles s’exécutent.

les applications de bureau utilisant des technologies de programmation plus anciennes Windows (programmation Win32 brute, Windows Forms, Windows Presentation Framework (WPF), etc.) ne peuvent pas gérer automatiquement la mise à l’échelle DPI sans travail supplémentaire du développeur. Sans ce travail, les applications apparaissent floues ou de taille incorrecte dans de nombreux scénarios d’utilisation courants. Ce document fournit un contexte et des informations sur ce qui est impliqué dans la mise à jour d’une application de bureau pour un rendu correct.

## <a name="display-scale-factor--dpi"></a>Afficher le facteur d’échelle & PPP

À mesure que la technologie d’affichage progresse, les fabricants de panneaux d’affichage ont compressé un nombre grandissant de pixels dans chaque unité d’espace physique sur leurs panneaux. Cela a entraîné une augmentation des points par pouce (DPI) des panneaux d’affichage modernes plus hauts qu’ils n’ont été historiquement. Dans le passé, la plupart des affichages contenait 96 pixels par pouce linéaire de l’espace physique (96 ppp); dans 2017, les affichages de près de 300 ppp ou plus sont facilement disponibles.

La plupart des infrastructures d’interface utilisateur de bureau héritées ont des hypothèses intégrées que la résolution d’affichage ne changera pas pendant la durée de vie du processus.  Cette hypothèse n’est plus vraie, avec les DPI d’affichage fréquemment modifiés plusieurs fois pendant la durée de vie d’un processus d’application. Voici quelques scénarios courants dans lesquels le facteur d’échelle d’affichage/DPI change :

-   Configurations à plusieurs écrans où chaque affichage a un facteur d’échelle différent et l’application est déplacée d’un affichage à un autre (par exemple, 4 Ko et un affichage de 1080p)
-   Ancrage et déconnexion d’un ordinateur portable haute résolution avec un affichage externe à basse résolution (ou vice versa)
-   Connexion via Bureau à distance d’un ordinateur portable/tablette haute résolution à un appareil basse résolution (ou vice versa)
-   Modification des paramètres d’affichage-facteur d’échelle pendant l’exécution des applications

Dans ces scénarios, les applications UWP se redessinent automatiquement pour la nouvelle résolution. Par défaut, et sans travail supplémentaire des développeurs, les applications de bureau ne le font pas. Les applications de bureau qui n’effectuent pas ce travail supplémentaire pour répondre aux modifications PPP peuvent apparaître floues ou incorrectement dimensionnées pour l’utilisateur.

## <a name="dpi-awareness-mode"></a>Mode de reconnaissance DPI

les applications de bureau doivent indiquer Windows si elles prennent en charge la mise à l’échelle DPI. Par défaut, le système considère que les applications de bureau ne prennent pas en charge PPP et étire leurs fenêtres. en définissant l’un des modes de reconnaissance ppp disponibles suivants, les applications peuvent indiquer explicitement Windows comment elles souhaitent gérer la mise à l’échelle dpi :

### <a name="dpi-unaware"></a>Prise en charge de DPI

Les applications sans prise en charge DPI sont rendues à une valeur DPI fixe de 96 (100%). chaque fois que ces applications sont exécutées sur un écran avec une échelle d’affichage supérieure à 96 ppp, Windows étend la bitmap de l’application à la taille physique attendue. Cela entraîne l’affichage de l’application floue.

### <a name="system-dpi-awareness"></a>Reconnaissance du système DPI

Les applications de bureau qui prennent en charge le système DPI reçoivent généralement les PPP de l’analyse connectée principale au moment de la connexion de l’utilisateur. Pendant l’initialisation, ils présentent leur interface utilisateur de manière appropriée (dimensionnement des contrôles, choix de la taille des polices, chargement des ressources, etc.) à l’aide de cette valeur DPI système. par conséquent, les applications prenant en charge les dpi du système ne sont pas mises à l’échelle dpi (bitmap étirée) par Windows sur affiche le rendu à cette seule résolution. lorsque l’application est déplacée vers un affichage avec un facteur d’échelle différent, ou si le facteur d’échelle d’affichage change, Windows bitmap met à l’échelle les fenêtres de l’application, ce qui les rend floues. En fait, les applications de bureau prenant en charge le système DPI ne s’affichent qu’à un seul facteur d’échelle d’affichage, ce qui devient flou à chaque modification de la résolution.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Détection des PPP Per-Monitor et Per-Monitor (v2)

Il est recommandé que les applications de bureau soient mises à jour pour utiliser le mode de reconnaissance DPI par moniteur, ce qui leur permet d’effectuer un rendu correct immédiatement à chaque modification de la résolution. lorsqu’une application signale à Windows qu’elle souhaite s’exécuter dans ce mode, Windows n’étire pas la bitmap de l’application lorsque les ppp changent, en envoyant [WM \_ DPICHANGED](wm-dpichanged.md) à la fenêtre d’application. Il incombe ensuite à l’application de gérer le redimensionnement proprement dit pour la nouvelle résolution PPP. la plupart des infrastructures d’interface utilisateur utilisées par les applications de bureau (Windows les contrôles communs (comctl32), Windows Forms, Windows Framework de présentation, etc.) ne prennent pas en charge la mise à l’échelle ppp automatique, ce qui oblige les développeurs à redimensionner et à repositionner le contenu de leurs fenêtres elles-mêmes.

Il existe deux versions de Per-Monitor savoir qu’une application peut s’inscrire elle-même en tant que version 1 et version 2 (PMv2). L’inscription d’un processus comme s’exécutant en mode de sensibilisation PMv2 génère les résultats suivants :

1.  L’application qui est avertie lorsque la DPI change (à la fois les HWND de niveau supérieur et enfant)
2.  L’application visualisant les pixels bruts de chaque affichage
3.  L’application n’est jamais bitmap mise à l’échelle par Windows
4.  Zone non cliente automatique (titre de fenêtre, barres de défilement, etc.) Mise à l’échelle DPI par Windows
5.  Boîtes de dialogue Win32 (à partir de [createDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) résolution automatique en dpi mis à l’échelle par Windows
6.  Ressources bitmap dessinées par thème dans les contrôles communs (cases à cocher, arrière-plans de bouton, etc.) qui s’affichent automatiquement au facteur d’échelle PPP approprié

En cas d’exécution en mode de sensibilisation à Per-Monitor v2, les applications sont averties lorsque leur PPP a changé. Si une application ne se redimensionne pas pour la nouvelle résolution, l’interface utilisateur de l’application apparaîtra trop petite ou trop grande (en fonction de la différence dans les valeurs PPP précédentes et nouvelles).

> [!Note]  
> La sensibilisation à Per-Monitor v1 (PMv1) est très limitée. Il est recommandé que les applications utilisent PMv2.

Le tableau suivant montre comment les applications s’affichent sous différents scénarios :


| Mode de reconnaissance DPI | Windows Version introduite | Affichage de l’application en PPP | Comportement sur la modification PPP | 
|--------------------|----------------------------|---------------------------|------------------------|
| Ignore | N/A | Tous les affichages sont de 96 ppp | Étirement de bitmap (flou) | 
| Système | Vista | Tous les affichages ont le même PPP (la résolution PPP de l’affichage principal au moment du démarrage de la session de l’utilisateur actuel) | Étirement de bitmap (flou) | 
| Per-Monitor | 8.1 | PPP de l’affichage sur lequel la fenêtre d’application se trouve principalement | <ul><li>Le HWND de niveau supérieur est informé de la modification PPP</li><li>Aucune mise à l’échelle DPI de tout élément d’interface utilisateur.</li></ul><br /> | 
| Per-Monitor V2 | Windows 10 Creators Update (1703) | PPP de l’affichage sur lequel la fenêtre d’application se trouve principalement | <ul><li>Les HWND de niveau supérieur <span class="underline">et</span> enfant sont avertis de la modification PPP</li></ul><br /><span class="underline">Mise à l’échelle DPI automatique de :</span><ul><li>Zone non cliente</li><li>Bitmaps dessinées par thème dans les contrôles communs (ComCtl32 V6)</li><li>Boîtes de dialogue (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">createDialog</a>)</li></ul><br /> | 


### <a name="per-monitor-v1-dpi-awareness"></a>Reconnaissance par analyse (v1) ppp

Per-Monitor v1 (PMv1 v1 Awareness mode Awareness) a été introduit avec Windows 8.1. Ce mode de reconnaissance des PPP est très limité et offre uniquement les fonctionnalités listées ci-dessous. il est recommandé que les applications de bureau utilisent le mode de sensibilisation Per-Monitor v2, pris en charge sur Windows 10 1703 ou version ultérieure.

La prise en charge initiale de la reconnaissance par moniteur ne proposait que les applications suivantes :

1.  Les HWND de niveau supérieur sont avertis d’une modification PPP et ont fourni une nouvelle taille suggérée
2.  Windows n’étire pas la bitmap de l’interface utilisateur de l’application
3.  L’application voit tous les affichages en pixels physiques (voir virtualisation)

sur Windows 10 1607 ou version ultérieure, les applications PMv1 peuvent également appeler [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) pendant \_ le NCCREATE WM pour demander que Windows mettre correctement à l’échelle la zone non cliente de la fenêtre.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Prise en charge de la mise à l’échelle DPI par moniteur par infrastructure/infrastructure d’interface utilisateur

le tableau ci-dessous montre le niveau de prise en charge de la prise en charge DPI par moniteur offert par différentes Windows infrastructures d’interface utilisateur à partir de Windows 10 1703 :


| Infrastructure/technologie | Support | Version du SE | Mise à l’échelle DPI gérée par | En savoir plus | 
|------------------------|---------|------------|------------------------|-----------------|
| Plateforme Windows universelle (UWP) | Complète | 1607 | Infrastructure d’interface utilisateur | <a href="/windows/uwp/get-started/whats-a-uwp">Plateforme Windows universelle (UWP)</a> | 
| Commandes Win32/Common Controls (comctl32.dll) brutes | <ul><li>Messages de notification de changement DPI envoyés à tous les HWND</li><li>Les ressources dessinées par thème sont rendues correctement dans les contrôles communs</li><li>Mise à l’échelle DPI automatique pour les boîtes de dialogue</li></ul> | 1703 | Application | <a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Exemple</a> | 
| Windows Forms | Mise à l’échelle DPI automatique par moniteur limitée pour certains contrôles | 1703 | Infrastructure d’interface utilisateur | <a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">prise en charge des résolutions élevées en Windows Forms</a> | 
| Windows Presentation Framework (WPF) | Les applications WPF natives prennent en charge la résolution de WPF hébergée dans d’autres infrastructures et d’autres infrastructures hébergées dans WPF ne sont pas automatiquement mises à l’échelle | 1607 | Infrastructure d’interface utilisateur | <a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Exemple</a> | 
| GDI | None | N/A | Application | Voir <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">mise à l’échelle GDI haute résolution</a> | 
| GDI+ | None | N/A | Application | Voir <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">mise à l’échelle GDI haute résolution</a> | 
| MFC | None | N/A | Application | N/A | 




 

## <a name="updating-existing-applications"></a>Mise à jour des applications existantes

Pour mettre à jour une application de bureau existante afin de gérer correctement la mise à l’échelle DPI, elle doit être mise à jour de telle sorte qu’au minimum, les parties importantes de l’interface utilisateur soient mises à jour pour répondre aux modifications PPP.

La plupart des applications de bureau s’exécutent en mode de reconnaissance DPI système. les applications prenant en charge dpi système sont généralement mises à l’échelle en fonction de la résolution de l’affichage principal (l’affichage dans lequel se trouvait la barre d’état système au moment du démarrage de la session Windows). en cas de modification de la résolution des ppp, Windows la bitmap étire l’interface utilisateur de ces applications, ce qui entraîne souvent un flou. Lors de la mise à jour d’une application compatible DPI du système pour qu’elle prenne en charge la résolution par moniteur, le code qui gère la disposition de l’interface utilisateur doit être mis à jour de manière à ce qu’il soit exécuté non seulement pendant l’initialisation de l’application, mais aussi chaque fois qu’une notification de modification DPI ([WM \_ DPICHANGED](wm-dpichanged.md) dans le cas de Win32) est reçue. Cela implique généralement de revisiter les hypothèses du code dont l’interface utilisateur ne doit être mise à l’échelle qu’une seule fois.

En outre, dans le cas de la programmation Win32, de nombreuses API Win32 n’ont pas de résolution ou de contexte d’affichage, de sorte qu’elles ne retournent que des valeurs par rapport à la DPI système. Il peut être utile de parcourir votre code pour rechercher certaines de ces API et de les remplacer par des variantes compatibles PPP. Voici quelques-unes des API courantes qui ont des variantes prenant en charge la résolution :



| Version à PPP unique   | Version de Per-Monitor        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

Il est également judicieux de rechercher les tailles codées en dur dans votre code base qui supposent une résolution constante, en les remplaçant par du code qui compte correctement la mise à l’échelle PPP. Voici un exemple qui incorpore toutes ces suggestions :

### <a name="example"></a>Exemple :

L’exemple ci-dessous montre un cas simplifié en cas de création d’un HWND enfant. L’appel à CreateWindow suppose que l’application s’exécute à 96 ppp, et que la taille et la position du bouton ne sont pas correctes à un niveau dpi supérieur :


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



Le code mis à jour ci-dessous montre les éléments suivants :

1.  Code PPP de création de fenêtres mettant à l’échelle la position et la taille du HWND enfant pour la résolution de sa fenêtre parente
2.  Réponse aux modifications PPP par repositionnement et redimensionnement du HWND enfant
3.  Tailles codées en dur supprimées et remplacées par du code qui répond aux modifications PPP


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



Lors de la mise à jour d’une application compatible DPI du système, voici quelques étapes courantes à suivre :

1.  Marquez le processus comme prenant en charge la résolution par moniteur (v2) à l’aide d’un manifeste d’application (ou d’une autre méthode, selon la ou les infrastructures d’interface utilisateur utilisées).
2.  rendre la logique de disposition d’interface utilisateur réutilisable et la décaler du code d’initialisation de l’application de façon à ce qu’elle puisse être réutilisée en cas de changement de DPI (WM \_ DPICHANGED dans le cas de la programmation Windows (Win32)).
3.  Invalidez tout code qui suppose que les données sensibles DPI (DPI/polices/tailles, etc.) n’ont jamais besoin d’être mises à jour. Il est très courant de mettre en cache les tailles de police et les valeurs DPI lors de l’initialisation du processus. Lors de la mise à jour d’une application pour qu’elle prenne en charge la résolution par moniteur, les données sensibles DPI doivent être réévaluées chaque fois qu’une nouvelle valeur PPP est rencontrée.
4.  Lorsqu’un changement de PPP se produit, rechargez (ou re-pixellise) toutes les ressources bitmap pour la nouvelle résolution ou, éventuellement, la bitmap étirer les ressources actuellement chargées à la taille correcte.
5.  Grep pour les API qui ne sont pas Per-Monitor compatibles PPP et les remplace par les API compatibles Per-Monitor DPI (le cas échéant). Exemple : remplacez GetSystemMetrics par GetSystemMetricsForDpi.
6.  Testez votre application sur un système multi-PPP ou à affichage multiple.
7.  Pour les fenêtres de niveau supérieur de votre application que vous ne pouvez pas mettre à jour avec une mise à l’échelle DPI correcte, utilisez la mise à l’échelle DPI en mode mixte (décrite ci-dessous) pour permettre l’étirement de la bitmap de ces fenêtres de niveau supérieur par le système.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mise à l’échelle PPP Mixed-Mode (mise à l’échelle PPP de sous-processus)

Lors de la mise à jour d’une application pour prendre en charge la prise en charge DPI par moniteur, il peut parfois devenir difficile ou impossible de mettre à jour chaque fenêtre de l’application en une seule fois. Cela peut simplement être dû au temps et à l’effort requis pour mettre à jour et tester toute l’interface utilisateur, ou parce que vous n’êtes pas propriétaire de tout le code d’interface utilisateur que vous devez exécuter (si votre application charge éventuellement une interface utilisateur tierce). dans ces situations, Windows offre un moyen de faciliter le monde de la sensibilisation par moniteur en vous permettant d’exécuter certaines de vos fenêtres d’application (de niveau supérieur uniquement) dans leur mode de reconnaissance ppp d’origine, tout en mettant l’accent sur la mise à jour du temps et de l’énergie des parties les plus importantes de votre interface utilisateur.

Voici une illustration de ce à quoi cela peut ressembler : vous mettez à jour l’interface utilisateur principale de votre application (« fenêtre principale » dans l’illustration) pour qu’elle s’exécute avec une prise en forme DPI par moniteur lorsque vous exécutez d’autres fenêtres dans leur mode existant (« fenêtre secondaire »).

![différences de mise à l’échelle dpi entre les modes de sensibilisation](images/hub-page-illustrations.png)

avant la Windows 10 mise à jour anniversaire (1607), le mode de reconnaissance ppp d’un processus était une propriété à l’échelle du processus. à partir de la Windows 10 mise à jour anniversaire, cette propriété peut désormais être définie par fenêtre **de niveau supérieur** . (Les fenêtres **enfants** doivent continuer de correspondre à la taille de mise à l’échelle de leur parent.) Une fenêtre de niveau supérieur est définie en tant que fenêtre sans parent. Il s’agit généralement d’une fenêtre « normale » avec des boutons de réduction, d’agrandissement et de fermeture. le scénario dans lequel la prise en charge DPI de sous-processus est destinée est d’avoir une interface utilisateur secondaire mise à l’échelle par Windows (bitmap étirée) tout en conservant le temps et les ressources nécessaires à la mise à jour de votre interface utilisateur principale.

Pour activer la reconnaissance des PPP de sous-processus, appelez [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) avant et après les appels de création de fenêtre. La fenêtre créée sera associée à la reconnaissance PPP que vous définissez via SetThreadDpiAwarenessContext. Utilisez le deuxième appel pour restaurer la reconnaissance actuelle du thread s.

bien que l’utilisation de la mise à l’échelle dpi du sous-processus vous permette de vous reposer sur Windows pour effectuer une partie de la mise à l’échelle dpi de votre application, cela peut augmenter la complexité de votre application. Il est important de comprendre les inconvénients de cette approche et de la nature des complexités qu’elle introduite. Pour plus d’informations sur la prise en charge DPI de sous-processus, consultez [mise à l’échelle dpi en mode mixte et API prenant en charge dpi.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Test de vos modifications

Une fois que vous avez mis à jour votre application pour qu’elle prenne en charge la résolution par moniteur, il est important de vérifier que votre application répond correctement aux modifications PPP dans un environnement à plusieurs résolutions. Voici quelques précisions à tester :

1.  Déplacement de fenêtres d’application entre des affichages de valeurs PPP différentes
2.  Démarrage de votre application sur des affichages de valeurs PPP différentes
3.  Modification du facteur d’échelle de votre moniteur pendant l’exécution de l’application
4.  en modifiant l’affichage que vous utilisez comme affichage principal, en _déconnectant Windows_, puis en retestant votre application après vous être connecté. Cela est particulièrement utile pour rechercher du code qui utilise des tailles/Dimensions codées en dur.

## <a name="common-pitfalls-win32"></a>Pièges courants (Win32)

**N’utilise pas le rectangle suggéré fourni dans WM \_ DPICHANGED**

lorsque Windows envoie votre fenêtre d’application un message [**WM \_ DPICHANGED**](wm-dpichanged.md) , ce message comprend un rectangle suggéré que vous devez utiliser pour redimensionner votre fenêtre. Il est essentiel que votre application utilise ce rectangle pour se redimensionner, comme suit :

1.  S’assurer que le curseur de la souris reste dans la même position relative sur la fenêtre lors du déplacement entre les affichages
2.  Empêchez la fenêtre d’application d’accéder à un cycle récursif PPP-modification, où une modification PPP déclenche une modification PPP ultérieure, ce qui déclenche une autre modification PPP.

si vous avez des exigences spécifiques à l’application qui vous empêchent d’utiliser le rectangle suggéré fourni par Windows dans le \_ message wm DPICHANGED, consultez [**wm \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). ce message peut être utilisé pour fournir à Windows la taille souhaitée que vous souhaitez utiliser une fois que le changement de DPI s’est produit, tout en évitant les problèmes décrits ci-dessus.

**Absence de documentation sur la virtualisation**

Lorsqu’un HWND ou un processus s’exécute comme une prise en charge DPI ou une prise en charge DPI du système, il peut s’agir d’une image bitmap étirée par Windows. dans ce cas, Windows met à l’échelle et convertit les informations ppp de certaines api en l’espace de coordonnées du thread appelant. par exemple, si un thread qui ne prend pas en charge la résolution ppp interroge la taille de l’écran pendant qu’il s’exécute sur un affichage haute résolution, Windows virtualise la réponse fournie à l’application comme si l’écran était en unités de 96 ppp. en guise d’alternative, lorsqu’un thread prenant en charge dpi système interagit avec un affichage à une résolution différente de celle utilisée lors du démarrage de la session de l’utilisateur actuel, Windows met à l’échelle des appels d’API dans l’espace de coordonnées que le HWND utiliserait s’il s’exécutait à son facteur d’échelle ppp d’origine.

Lorsque vous mettez à jour votre application de bureau avec une mise à l’échelle PPP correctement, il peut être difficile de savoir quels appels d’API peuvent retourner des valeurs virtualisées en fonction du contexte du thread. ces informations ne sont pas suffisamment documentées par Microsoft. Sachez que si vous appelez une API système à partir d’un contexte de thread qui ne prend pas en charge DPI ou le système DPI, la valeur de retour peut être virtualisée. Par conséquent, assurez-vous que votre thread s’exécute dans le contexte PPP que vous attendez quand vous interagissez avec l’écran ou des fenêtres individuelles. Lorsque vous modifiez temporairement le contexte PPP d’un thread à l’aide de [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), veillez à restaurer l’ancien contexte lorsque vous avez terminé pour éviter de provoquer un comportement incorrect ailleurs dans votre application.

**de nombreuses api Windows n’ont pas de contexte ppp**

de nombreuses api Windows héritées n’incluent pas de contexte ppp ou HWND dans le cadre de leur interface. Par conséquent, les développeurs doivent souvent effectuer des tâches supplémentaires pour gérer la mise à l’échelle des informations sensibles DPI, telles que les tailles, les points ou les icônes. Par exemple, les développeurs qui utilisent [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) doivent être chargés d’étirer les icônes de bitmap ou d’utiliser d’autres API pour charger les icônes correctement dimensionnées pour les PPP appropriées, telles que [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Réinitialisation forcée de la reconnaissance DPI à l’échelle du processus**

En général, le mode de reconnaissance PPP de votre processus ne peut pas être modifié après l’initialisation du processus. toutefois, Windows pouvez modifier de force le mode de reconnaissance dpi de votre processus si vous tentez de rompre la condition selon laquelle tous les hwnd dans une arborescence de fenêtre ont le même mode de reconnaissance ppp. dans toutes les versions de Windows, à partir de Windows 10 1703, il n’est pas possible d’avoir des hwnd différents dans une arborescence HWND qui s’exécutent dans différents modes de reconnaissance ppp. Si vous tentez de créer une relation enfant-parent qui interrompt cette règle, la prise en DPI de l’ensemble du processus peut être réinitialisée. Cela peut être déclenché par :

1.  Appel CreateWindow où la fenêtre parente passée est d’un mode de reconnaissance PPP différent du thread appelant.
2.  Appel SetParent, où les deux fenêtres sont associées à différents modes de reconnaissance PPP.

Le tableau ci-dessous montre ce qui se passe si vous tentez de violer cette règle :



| Opération                 | Windows 8.1                                  | Windows 10 (1607 et versions antérieures)                | Windows 10 (1703 et versions ultérieures)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (in-proc)    | N/A                                          | **Héritages enfants** (mode mixte)              | **Héritages enfants** (mode mixte)              |
| CreateWindow (traitement croisé) | **Réinitialisation forcée** (du processus de l’appelant)       | **Héritages enfants** (mode mixte)              | **Réinitialisation forcée** (du processus de l’appelant)       |
| SetParent, (in-proc)       | N/A                                          | **Réinitialisation forcée** (du processus en cours)        | **Fail** (état d’erreur \_ non valide \_ )             |
| SetParent, (traitement croisé)    | **Réinitialisation forcée** (du processus de la fenêtre enfant) | **Réinitialisation forcée** (du processus de la fenêtre enfant) | **Réinitialisation forcée** (du processus de la fenêtre enfant) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les API haute résolution](high-dpi-reference.md)
</dt> <dt>

[La mise à l’échelle DPI en mode mixte et les API compatibles PPP.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

