---
description: La classe CBaseWindow est une classe de base pour la gestion de Windows.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: CBaseWindow, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923696"
---
# <a name="cbasewindow-class"></a>CBaseWindow, classe

La `CBaseWindow` classe est une classe de base pour la gestion de Windows. Les convertisseurs vidéo peuvent utiliser cette classe pour créer des fenêtres vidéo. Pour utiliser cette classe, créez une classe dérivée qui hérite de `CBaseWindow` . Dans la classe dérivée :

-   Implémentez la méthode virtuelle pure [**CBaseWindow :: GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), qui définit les styles de fenêtre.
-   Substituez la méthode [**CBaseWindow :: OnReceiveMessage**](cbasewindow-onreceivemessage.md) , qui gère les messages de fenêtre.
-   Implémentez un destructeur qui appelle la méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) .

Avant d’utiliser une instance de la classe dérivée, appelez la méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) .



| Variables membres protégées                                           | Description                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ HINSTANCE**](cbasewindow-m-hinstance.md)                      | Handle de l’instance de module.                                                 |
| [**HWND de m \_**](cbasewindow-m-hwnd.md)                                | Handle de la fenêtre de l’objet.                                                 |
| [**HDC de m \_**](cbasewindow-m-hdc.md)                                  | Handle vers le contexte de périphérique de la fenêtre.                                         |
| [**\_largeur m**](cbasewindow-m-width.md)                              | Largeur de la zone cliente, en pixels.                                           |
| [**\_hauteur m**](cbasewindow-m-height.md)                            | Hauteur de la zone cliente, en pixels.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Indicateur qui spécifie si la fenêtre a été activée.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Chaîne statique qui contient le nom de la classe de fenêtre.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Styles de classe pour la fenêtre.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Styles de fenêtre pour la fenêtre.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Styles de fenêtre étendus pour la fenêtre.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Message privé qui amène la fenêtre au premier plan.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Message privé qui réalise la palette.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Handle vers le contexte de périphérique de mémoire.                                           |
| [**m \_ HPALETTE**](cbasewindow-m-hpalette.md)                        | Handle vers la palette de la fenêtre.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Indicateur qui spécifie si la fenêtre doit réaliser sa palette.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Indicateur qui spécifie si la palette doit être une palette d’arrière-plan.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Indicateur qui spécifie si une nouvelle palette est réalisée.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Section critique, pour sérialiser l’accès à l’objet.                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Indicateur qui spécifie s’il faut récupérer le contexte de périphérique (Device Context).                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Indicateur qui spécifie si la fenêtre publie ou envoie son message de destruction. |
| Méthodes protégées                                                    | Description                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Gère les messages de modification de palette. Virtuels.                                      |
| M&#233;thodes publiques                                                       | Description                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Méthode de constructeur.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Détruit la fenêtre. Virtuels.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Crée la fenêtre. Virtuels.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Désactive la fenêtre. Virtuels.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Dimensionne la fenêtre en fonction des exigences de la classe dérivée. Virtuels.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Gère \_ les messages de taille WM. Virtuels.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Gère \_ les messages de fermeture WM. Virtuels.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Récupère la taille par défaut de la zone cliente. Virtuels.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Libère les ressources de la fenêtre. Virtuels.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Initialise la fenêtre. Virtuels.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifie la fenêtre que la broche d’entrée du convertisseur a été connectée.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Crée la fenêtre.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Aligne la fenêtre sur une limite **DWORD** , pour des performances maximales.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Définit l’état d’affichage de la fenêtre.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Provoque la redessination de la fenêtre.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Met la fenêtre au premier plan.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Installe une palette pour la fenêtre. Virtuels.                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | Spécifie si la fenêtre réalise des palettes.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Réalise la palette actuelle de la fenêtre. Virtuels.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Permet à une classe dérivée de transférer des messages à une autre fenêtre. Virtuels.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Récupère la largeur actuelle de la fenêtre.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Récupère la hauteur actuelle de la fenêtre.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Récupère un handle vers la fenêtre.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Récupère un handle vers le contexte de périphérique de mémoire.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Récupère un handle vers le contexte de périphérique de la fenêtre.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Gère les messages de fenêtre. Virtuels.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Supprime la palette active de la fenêtre et restaure la palette système par défaut.  |
| Méthodes virtuelles pures                                                 | Description                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Récupère les styles de classe et les styles de fenêtre de la fenêtre.                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




