---
title: Développement d’une application WPF DPI par moniteur
description: Remarque Cette page couvre le développement WPF hérité pour Windows 8.1. Si vous développez des applications WPF pour Windows 10, consultez la documentation la plus récente sur GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interface utilisateur Windows, applications compatibles DPI
- Interface utilisateur Windows, haute résolution
- Applications prenant en charge DPI
- haute résolution
- écriture d’applications Win32 compatibles DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101640"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Développement d’une application WPF DPI par moniteur

**API importantes**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Cette page traite du développement WPF hérité pour Windows 8.1.** Si vous développez des applications WPF pour Windows 10, consultez la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentation la plus récente sur GitHub.</a>

 

Windows 8.1 offre aux développeurs de nouvelles fonctionnalités pour créer des applications de bureau qui prennent en charge la résolution par moniteur. Pour tirer parti de cette fonctionnalité, une application par analyse prenant en charge DPI doit effectuer les opérations suivantes :

-   Modifiez les dimensions des fenêtres pour conserver une taille physique qui semble cohérente sur n’importe quel affichage
-   Restructurer et restituer à nouveau les graphiques pour la nouvelle taille de fenêtre
-   Sélectionner les polices mises à l’échelle correctement pour le niveau PPP
-   Sélectionner et charger des ressources bitmap adaptées au niveau PPP

Pour faciliter la création d’une application prenant en charge la résolution par moniteur, Windows 8.1 fournit les Win32APIs Microsoft suivants :

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (ou entrée de manifeste PPP) définit le processus sur un niveau de sensibilisation PPP spécifié, qui détermine ensuite la façon dont Windows met à l’échelle l’interface utilisateur. Cela remplace [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) retourne le niveau de sensibilisation PPP. Cela remplace [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) retourne la valeur PPP d’une analyse.
-   La notification de fenêtre [**WM \_ DPICHANGED**](wm-dpichanged.md) est envoyée aux applications prenant en charge la résolution par moniteur lorsque la position d’une fenêtre change de telle sorte que la plus grande partie de sa zone croise une analyse avec une valeur PPP différente de la résolution avant modification de la position ou lorsque l’utilisateur déplace le curseur d’affichage. Pour créer une application qui se redimensionne et s’affiche à nouveau lorsqu’un utilisateur la déplace vers un autre affichage, utilisez cette notification.

Pour plus d’informations sur les différents niveaux de reconnaissance PPP pris en charge pour les applications de bureau dans Windows 8.1 consultez la rubrique sur l' [écriture d’applications DPI-Aware Desktop et Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>Mise à l’échelle DPI et WPF

Les applications Windows Presentation Foundation (WPF) utilisent par défaut la prise en charge DPI système. Pour obtenir les définitions des différents niveaux de reconnaissance PPP, consultez la rubrique [écriture de DPI-Aware bureau et des applications Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). Le système graphique WPF utilise des unités indépendantes du périphérique pour permettre la résolution et l’indépendance des appareils. WPF met automatiquement à l’échelle chaque pixel indépendant de l’appareil en fonction de la résolution système actuelle. Cela permet aux applications WPF de se mettre à l’échelle automatiquement quand la valeur PPP du moniteur sur lequel se trouve la fenêtre correspond à la même résolution système. Toutefois, étant donné que les applications WPF prennent en charge le système dpi, l’application est mise à l’échelle par le système d’exploitation lorsque l’application est déplacée vers un moniteur avec une résolution différente ou lorsque le curseur du panneau de configuration est utilisé pour modifier la résolution. La mise à l’échelle dans le système d’exploitation peut entraîner un flou des applications WPF, en particulier lorsque la mise à l’échelle est non intégrale. Afin d’éviter la mise à l’échelle des applications WPF, vous devez les mettre à jour pour qu’elles prennent en charge la résolution par moniteur.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Exemple de procédure pas à pas pour chaque moniteur WPF

L' [exemple WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) avec prise en charge de l’analyse est un exemple d’application WPF mis à jour pour prendre en charge la résolution par moniteur. Cet exemple est composé de deux projets :

-   NativeHelpers. vcxproj : il s’agit d’un projet d’assistance natif qui implémente la fonctionnalité de base permettant à une application WPF de prendre en charge la résolution par moniteur en utilisant les Win32APIs ci-dessus. Le projet contient deux classes :
    -   PerMonDPIHelpers : classe qui fournit des fonctions d’assistance pour les opérations liées à DPI, telles que la récupération de la valeur PPP actuelle de l’analyseur actif, la définition d’un processus pour la prise en charge DPI par moniteur, etc.
    -   PerMonitorDPIWindow : classe de base dérivée de **System. Windows. Window** qui implémente les fonctionnalités permettant à une fenêtre d’application WPF d’être compatible avec la résolution par le moniteur. Ajuste la taille de la fenêtre, la taille de rendu graphique et la taille de police en fonction des PPP du moniteur plutôt que de la résolution du système.
-   WPFApplication. csproj : exemple d’application WPF qui utilise PerMonitorDPIWindow (PerMonitorDPIWindow) et montre comment la fenêtre d’application et le rendu se redimensionne quand la fenêtre est déplacée vers un moniteur avec une résolution différente ou lorsque le curseur dans le panneau de configuration d’affichage est utilisé pour modifier la résolution.

Pour exécuter l’exemple, suivez les étapes ci-dessous :

1.  Télécharger et décompresser l' [exemple WPF avec prise en charge par moniteur](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  Démarrez Microsoft Visual Studio et sélectionnez **fichier > ouvrir > projet/solution**
3.  Accédez au répertoire qui contient l’exemple décompressé. Accédez au répertoire nommé pour l’exemple, puis double-cliquez sur le fichier de solution Visual Studio (. sln).
4.  Appuyez sur F7 ou utilisez **générer > générer la solution** pour générer l’exemple
5.  Appuyez sur CTRL + F5 ou utilisez l' **> de débogage exécuter sans débogage** pour exécuter l’exemple

Pour voir l’impact de la modification du DPI sur une application WPF mise à jour pour être compatible avec la résolution PPP par moniteur à l’aide de la classe de base de l’exemple, déplacez la fenêtre d’application vers et depuis les affichages ayant des DPI différents. Lorsque la fenêtre est déplacée entre les analyses, la taille de la fenêtre et l’échelle de l’interface utilisateur sont mises à jour en fonction de la résolution de l’affichage à l’aide du système graphique Scalable de WPF, plutôt que d’être mises à l’échelle par le système d’exploitation. L’interface utilisateur de l’application est rendue en mode natif et n’apparaît pas floue. Si vous n’avez pas deux affichages avec des PPP différents, modifiez la résolution en modifiant le curseur dans le panneau de configuration d’affichage. La modification du curseur et le fait de cliquer sur **appliquer** redimensionnent la fenêtre de l’application et mettent automatiquement à jour la mise à l’échelle de l’interface utilisateur.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Mise à jour d’une application WPF existante pour qu’elle prenne en charge les DPI par moniteur à l’aide d’un projet d’assistance dans l’exemple WPF

Si vous disposez d’une application WPF existante et que vous souhaitez utiliser le projet d’assistance PPP de l’exemple pour la prise en charge de l’informatique en DPI, procédez comme suit.

1.  Télécharger et décompresser l’exemple WPF avec prise en charge par moniteur
2.  Démarrez Visual Studio et sélectionnez **fichier > ouvrir > projet/solution**
3.  Accédez au répertoire qui contient une application WPF existante et double-cliquez sur le fichier de solution Visual Studio (. sln).
4.  Cliquez avec le bouton droit sur **Solution > ajouter > projet existant** ![ une capture d’écran qui illustre la sélection de menu Ajouter : projet existant](images/scrvs-image1.png)
5.  Dans la boîte de dialogue de sélection de fichier, accédez au répertoire qui contient l’exemple décompressé. Ouvrez le répertoire nommé pour l’exemple, accédez au dossier « NativeHelpers », sélectionnez le fichier projet Visual C++ « NativeHelpers. vcxproj », puis cliquez sur **OK** .
6.  Cliquez avec le bouton droit sur le projet NativeHelpers et sélectionnez **générer**. Cela génère NativeHelpers.dll qui sera ajouté en tant que référence à l’application WPF à l’étape suivante ![ une capture d’écran illustrant la sélection du menu Générer](images/scrvs-image2.png)
7.  Ajoutez une référence à NativeHelpers.dll à partir de votre application WPF. Développez votre projet d’application WPF, cliquez avec le bouton droit sur **références** , puis cliquez sur **Ajouter une référence...**
8.  Dans la boîte de dialogue qui s’affiche, développez la section **solution** . Sous **projets**, sélectionnez NativeHelpers, puis cliquez sur **OK** pour ![ obtenir une capture d’écran illustrant la boîte de dialogue Resource Manager.](images/scrvs-image3.png)
9.  Développez votre projet d’application WPF, développez **Propriétés**, puis ouvrez **AssemblyInfo. cs**. Apporter les ajouts suivants à AssemblyInfo. cs
    -   Ajoutez une référence à System. Windows. Media dans la section de référence (à l’aide de System. Windows. Media ;)
    -   Ajout de l’attribut DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![capture d’écran illustrant les propriétés supplémentaires](images/scrvs-image4.png)
10. Hériter de la classe de fenêtre WPF principale de la classe de base PerMonitorDPIWindow
    -   Mettez à jour le fichier. cs de la fenêtre WPF principale afin d’hériter de la classe de base PerMonitorDPIWindow
        -   Ajoutez une référence à NativeHelpers dans la section de référence en ajoutant la ligne `using NativeHelpers;`
        -   Hériter de la classe de fenêtre principale de la classe PerMonitorDPIWindow

        ![une capture d’écran illustrant la référence c++](images/scrvs-image5.png)
    -   Mettez à jour le fichier. XAML de la fenêtre WPF principale afin d’hériter de la classe de base PerMonitorDPIWindow
        -   Ajoutez une référence à NativeHelpers dans la section de référence en ajoutant la ligne `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Hériter de la classe de fenêtre principale de la classe PerMonitorDPIWindow

        ![capture d’écran illustrant l’ajout de la référence. Xaml](images/scrvs-image6.png)
11. Appuyez sur F7 ou utilisez **générer > générer la solution** pour générer l’exemple
12. Appuyez sur CTRL + F5 ou utilisez l' **> de débogage exécuter sans débogage** pour exécuter l’exemple

L' [exemple](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) d’application WPF avec prise en charge de l’analyse illustre la manière dont une application WPF peut être mise à jour pour être compatible avec la résolution PPP par moniteur en répondant à la notification de fenêtre [**WM \_ DPICHANGED**](wm-dpichanged.md) . En réponse à la notification de fenêtre, l’exemple met à jour la transformation de mise à l’échelle utilisée par WPF en fonction de la valeur PPP actuelle du moniteur sur lequel la fenêtre est activée. Le *wParam* de la notification de fenêtre contient la nouvelle PPP dans *wParam*. Le *lParam* contient un rectangle qui a la taille et la position de la nouvelle fenêtre suggérée, mise à l’échelle pour la nouvelle résolution PPP.

Remarque :

> [!Note]  
> Dans la mesure où cet exemple remplace la taille de la fenêtre et la transformation d’échelle du nœud racine de la fenêtre WPF, un travail supplémentaire peut être requis par le développeur d’applications dans les cas suivants :
>
> -   La taille de la fenêtre a un impact sur les autres parties de l’application, telles que la fenêtre WPF qui est hébergée dans une autre application.
> -   L’application WPF qui étend cette classe définit d’autres transformations sur le visuel racine. l’exemple peut remplacer une autre transformation appliquée par l’application WPF elle-même.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Vue d’ensemble du projet d’assistance dans l’exemple WPF

Pour rendre une application WPF existante prenant en charge DPI par moniteur, la bibliothèque NativeHelpers fournit les fonctionnalités suivantes :

-   **Marque l’application WPF en fonction de la prise en charge DPI par ponitor :** L’application WPF est marquée comme prise en charge DPI par moniteur en appelant [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) pour le processus actuel. Le marquage de l’application en fonction de la prise en charge DPI par moniteur permet de garantir que

    -   Le système d’exploitation n’effectue pas la mise à l’échelle de l’application lorsque la résolution du système ne correspond pas à la résolution actuelle de l’analyse de la fenêtre de l’application.
    -   Le message [**WM \_ DPICHANGED**](wm-dpichanged.md) est envoyé à chaque modification de la résolution de la fenêtre

-   **Ajuste la dimension de la fenêtre, redisposition et restitue à nouveau le contenu graphique et sélectionne les polices en fonction de la résolution initiale du moniteur sur lequel la fenêtre est activée :** Une fois que l’application est marquée avec la prise en charge DPI par moniteur, WPF met toujours à l’échelle la taille de la fenêtre, les graphiques et la taille de police en fonction de la résolution du système. Dans la mesure où, au lancement de l’application, il n’est pas garanti que la résolution des PPP du système soit identique à celle du moniteur sur lequel la fenêtre est lancée, la bibliothèque ajuste ces valeurs une fois la fenêtre chargée. La classe de base **PerMonitorDPIWindow** les met à jour dans le gestionnaire **OnLoaded ()** .

    La taille de la fenêtre est mise à jour en modifiant les propriétés de **largeur** et de **hauteur** de la fenêtre. La disposition et la taille sont mises à jour en appliquant une transformation d’échelle appropriée au nœud racine de la fenêtre WPF.

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   **Répond à WM \_ Notification de fenêtre DPICHANGED :** mettez à jour la taille de la fenêtre, les graphiques et la taille de police en fonction des PPP passés dans la notification de fenêtre. La classe de base **PerMonitorDPIWindow** gère la notification de fenêtre dans la méthode **HandleMessages ()** .

    La taille de la fenêtre est mise à jour en appelant **SetWindowPos** à l’aide des informations passées dans le *lParam* du message de fenêtre. La disposition et la taille des graphiques sont mises à jour en appliquant une transformation d’échelle appropriée au nœud racine de la fenêtre WPF. Le facteur d’échelle est calculé à l’aide du PPP passé dans le *wParam* du message de fenêtre.

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Gestion de la modification DPI pour les ressources telles que les images

Pour mettre à jour le contenu graphique, l’exemple d’application WPF applique une transformation d’échelle au nœud racine de l’application WPF. Bien que cela fonctionne bien pour le contenu qui est rendu en mode natif par WPF (Rectangle, texte, etc.), cela implique que les ressources bitmap comme les images sont mises à l’échelle par WPF.

Afin d’éviter les bitmaps floues provoqués par la mise à l’échelle, le développeur d’applications WPF peut écrire un contrôle d’image DPI personnalisé qui sélectionne une autre ressource en fonction de la valeur PPP actuelle du moniteur sur lequel se trouve la fenêtre. Le contrôle image peut reposer sur l’événement **DPIChanged ()** déclenché pour la fenêtre WPF qui consomme à partir du **PerMonitorDPIWindow**, lorsque les PPP changent.

> [!Note]  
> Le contrôle image doit également sélectionner le contrôle approprié pendant le lancement de l’application dans le gestionnaire d’événements de fenêtre WPF **chargé ()** .

 

 

 