---
description: Cette rubrique décrit les interfaces et les méthodes spécifiques requises pour créer un gestionnaire d’aperçus.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Génération de gestionnaires d’aperçus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a810f15fed66d69bce32387249a2e0d678a1eb6c0dd918ec5df2e1ddbeb5be8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032917"
---
# <a name="building-preview-handlers"></a>Génération de gestionnaires d’aperçus

Cette rubrique décrit les interfaces et les méthodes spécifiques requises pour créer un gestionnaire d’aperçus.

Un gestionnaire d’aperçus doit implémenter les interfaces suivantes :

-   [IInitializeWithStream :: Initialize](#iinitializewithstreaminitialize) (fortement préféré), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)ou [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Si votre gestionnaire d’aperçus prend en charge les paramètres visuels fournis par l’hôte, tels que la couleur d’arrière-plan et la police, il doit également implémenter l’interface suivante :

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

Cette rubrique suppose que le gestionnaire d’aperçus est initialisé avec un flux et qu’il est inscrit pour une extension de nom de fichier particulière.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream :: Initialize

Stockez les paramètres [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) et mode afin de pouvoir lire les données de l’élément lorsque vous êtes prêt à afficher un aperçu de l’élément. Ne chargez pas les données dans [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Chargez les données dans [**IPreviewHandler ::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) juste avant le rendu.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite :: SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite :: GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite :: SetSite

Stocke le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour un accès ultérieur.

Si vous avez actuellement une référence à un objet [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , libérez-le. Utilisez le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) stocké pour appeler [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le site pour une nouvelle référence **IPreviewHandlerFrame** .

Si vous disposez actuellement d’une table d’accélérateurs, détruisez-la. Appelez [**IPreviewHandlerFrame :: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) pour obtenir une nouvelle table d’accélérateurs. Stockez cette table. Notez qu’il est utilisé uniquement comme une liste de touches accélérateur prises en charge par le frame. Les commandes dans les entrées d’accélérateur sont ignorées.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite :: GetSite

Retourne le pointeur de site, quelle que soit la façon dont il est.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow::GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Retournez E \_ NOTIMPL pour cette méthode.

### <a name="iolewindowgetwindow"></a>IOleWindow::GetWindow

Si la fenêtre du gestionnaire d’aperçus existe actuellement, retournez le **HWND** de cette fenêtre et s \_ OK. Si la fenêtre n’existe pas, retournez E \_ Fail.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler :: SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler :: SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler ::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler :: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler :: QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler :: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler :: Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler :: SetWindow

Définissez le paramètre *HWND* de cette méthode sur le parent du **HWND** du gestionnaire d’aperçus. Cette méthode peut être appelée plusieurs fois. Redimensionnez votre Aperçu afin qu’il s’affiche uniquement dans la zone décrite par le paramètre *PRC* .

Si le générateur d’aperçu est en cours de rendu, utilisez la méthode [**IPreviewHandler :: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) pour modifier le parent du générateur d’aperçu. Modifiez également la zone de rendu du générateur d’aperçu.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler :: SetRect

Redimensionnez votre Aperçu afin qu’il s’affiche uniquement dans la zone décrite par la *PRC* de cette méthode.

Si le générateur d’aperçu est en cours de rendu, modifiez la zone dans laquelle votre générateur d’aperçu effectue le rendu.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler ::D oPreview

C’est là que le véritable travail est effectué. Dans la mesure où un aperçu est dynamique, le contenu de l’aperçu doit être chargé uniquement lorsque cela est nécessaire. Ne chargez pas le contenu dans l’initialisation.

Si la fenêtre du gestionnaire d’aperçus n’existe pas, créez-la. Les fenêtres de votre gestionnaire d’aperçus doivent être les enfants de la fenêtre fournie par [**IPreviewHandler :: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Ils doivent correspondre à la taille fournie par **IPreviewHandler :: SetWindow** et [**IPreviewHandler :: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (selon la valeur la plus récente étant appelée).

Une fois que vous disposez d’une fenêtre, chargez les données à partir de l' [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) avec lequel le gestionnaire d’aperçus a été initialisé et affichez ces données dans la fenêtre de votre gestionnaire d’aperçus.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler :: SetFocus

Cette méthode est appelée lorsque le focus entre dans le volet de lecture via une action de tabulation. Dans la mesure où elle peut être entrée sous la forme d’un onglet suivant ou d’un onglet inverse, utilisez l’état actuel de la touche Maj pour décider si le premier ou le dernier taquet de tabulation dans le volet de lecture doit recevoir le focus.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler :: QueryFocus

Cette méthode doit appeler la fonction [**getFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) et retourner le résultat de cet appel dans le paramètre *phwnd* .

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler :: TranslateAccelerator

Cette méthode est appelée par la pompe de messages du processus du gestionnaire d’aperçus (qu’il s’agisse prevhost.exe ou d’un serveur local personnalisé) en réponse aux séquences de touches de l’utilisateur. Les gestionnaires d’aperçus doivent gérer ces séquences de touches ou les transférer à leur hôte en fonction de l’algorithme détaillé ci-dessous.

Toutefois, étant donné que les préversions sont en lecture seule, l’entrée au clavier doit être minime et les optimisations telles que celles-ci ne sont pas nécessaires dans de nombreux cas.

Si l’accélérateur clavier passé à cette méthode par le biais de la pompe de messages est un accélérateur accepté par votre gestionnaire d’aperçus, traitez-le et renvoyez-le \_ OK. Si votre gestionnaire n’accepte pas cet accélérateur, le message d’accélérateur peut être renvoyé jusqu’au frame à gérer.

Il existe deux options pour transférer les accélérateurs de clavier vers le frame :

Le modèle le plus simple consiste à transférer toutes les séquences de touches à l’hôte à l’aide de [**IPreviewHandlerFrame :: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). cette opération s’effectue dans l’exemple de gestionnaire d’aperçus fourni avec le kit de développement logiciel (SDK) Windows. Tous les gestionnaires d’aperçus de faible intégrité doivent utiliser ce modèle. Si l’accélérateur n’est pas géré par votre gestionnaire d’aperçus, appelez **IPreviewHandlerFrame :: TranslateAccelerator** et retournez son résultat.

L’autre modèle consiste à utiliser une table d’accélérateurs comme optimisation pour éviter d’envoyer un trop grand nombre de frappes de touches entre les limites de processus :

1.  Quand [**IObjectWithSite :: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) est appelé sur votre gestionnaire d’aperçus, vous obtenez la table d’accélérateurs via [**IPreviewHandlerFrame :: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Veillez à libérer le descripteur de la table d’accélérateurs lorsque votre générateur d’aperçu est détruit.)
2.  Si l’accélérateur est géré par votre gestionnaire d’aperçus, gérez-le et renvoyez \_ OK.
3.  Si l’accélérateur n’est pas géré par votre gestionnaire d’aperçus, comparez le message à l’aide de [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) à la table d’accélérateurs acquise.
4.  Si l’accélérateur correspond à une entrée dans cette table d’accélérateurs, appelez [**IPreviewHandlerFrame :: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) et retournez son résultat.
5.  Si l’accélérateur ne correspond à aucune entrée dans la table d’accélérateurs, retourne la \_ valeur false.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler :: Unload

Lorsque cette méthode est appelée, arrêtez tout rendu, libérez toutes les ressources allouées en lisant les données du flux, puis libérez le [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) lui-même.

Une fois cette méthode appelée, le gestionnaire doit être réinitialisé avant toute tentative d’appel de [**IPreviewHandler ::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals::SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Ces méthodes doivent être implémentées lors de la direction du gestionnaire d’aperçu pour répondre aux jeux de couleurs et de polices de l’hôte. L’hôte interroge le gestionnaire pour [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). S’il est jugé pris en charge, l’hôte lui fournit la couleur, la police et la couleur de texte.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Stockez cette couleur et utilisez-la pendant le rendu lorsque vous souhaitez fournir une couleur d’arrière-plan. Par exemple, pour remplir la fenêtre lorsque le gestionnaire est rendu à une zone plus petite que la zone fournie par [**IPreviewHandler :: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) et [**IPreviewHandler :: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Notez, toutefois, que vous ne devez pas dessiner en dehors de la zone fournie par ces méthodes.

Si cette méthode est appelée alors que l’aperçu est déjà en cours de restitution, le rendu doit être redémarré à l’aide de cette couleur d’arrière-plan.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals::SetFont

stockez ces informations de police et utilisez-les lors du rendu lorsque vous souhaitez afficher du texte cohérent avec les paramètres actuels de Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

stockez ces informations de couleur de texte et utilisez-les lors du rendu lorsque vous souhaitez afficher du texte cohérent avec les paramètres actuels de Windows Vista.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires d’aperçus et hôte de l’interpréteur de commandes](preview-handlers.md)
</dt> <dt>

[Comment inscrire un gestionnaire d’aperçus](how-to-register-a-preview-handler.md)
</dt> <dt>

[Instructions du gestionnaire d’aperçus](preview-handler-guidelines.md)
</dt> </dl>

 

 
