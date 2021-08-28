---
description: Le contrôle InkEdit est une super classe du contrôle RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Messages InkEdit (Win32 uniquement)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475035"
---
# <a name="inkedit-messages-win32-only"></a>Messages InkEdit (Win32 uniquement)

Le contrôle [InkEdit](inkedit-control-reference.md) est une super classe du contrôle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Chaque message **RichEdit** est transmis, directement dans la plupart des cas, et a exactement le même effet que dans **RichEdit**. Cela s’applique également aux messages de notification d’événement.

Pour envoyer ces messages, appelez la fonction SendMessage avec les paramètres suivants :




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>Message

La fenêtre parente du contrôle [InkEdit](inkedit-control-reference.md) reçoit des messages de notification d’événement par le biais du \_ message WM Notify :


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Obtient/définit le message                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_GETINKMODE em<br/>           | Obtient le mode d’encrage du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message renvoie l’une des valeurs définies dans l’énumération [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , qui spécifie si la collection d’encres est désactivée, si l’encre est collectée ou si les entrées et les gestes sont collectées.<br/>                                                                                                                                                                                                                                                         |
| \_SETINKMODE em<br/>           | Définit le mode d’encrage du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Spécifie l’une des valeurs de l’énumération [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , qui spécifie si la collection d’encres est désactivée, si l’encre est collectée ou si les entrées et les gestes sont collectées.<br/>*lParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/> Remarques :<br/> Cela ne doit être utilisé que si EM \_ GETSTATUS retourne la valeur \_ Idle.<br/>                                                                                                               |
| \_GETINKINSERTMODE em<br/>     | Obtient le mode d’insertion d’encre du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message retourne l’une des valeurs de l’énumération [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , qui spécifie si l’entrée manuscrite est insérée dans le contrôle sous forme de texte ou d’entrée manuscrite.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETINKINSERTMODE em<br/>     | Définit le mode d’insertion de l’encre du contrôle [InkEdit](inkedit-control-reference.md) . l’envoi de ce message n’a aucun effet s’il est utilisé avec un système d’exploitation autre que Microsoft Windows XP édition Tablet PC.<br/> Paramètres :<br/>*wParam* Spécifie l’une des valeurs de l’énumération [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , qui spécifie si l’entrée manuscrite est insérée dans le contrôle sous forme de texte ou d’entrée manuscrite.<br/>*lParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                       |
| \_GETDRAWATTR em<br/>          | Obtient les attributs de dessin actuels du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur (IInkDrawingAttributes \* \* pDrawAttr) pour recevoir l’objet [**InkDrawingAttributes**](inkdrawingattributes-class.md) actuel.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                |
| \_SETDRAWATTR em<br/>          | Définit les attributs de dessin à utiliser pour la collection d’encres ultérieures.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur (IInkDrawingAttributes \* pDrawAttr) vers un objet [**InkDrawingAttributes**](inkdrawingattributes-class.md) .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                                                                  |
| \_GETRECOTIMEOUT em<br/>       | Obtient le délai d’expiration de reconnaissance, en millisecondes, pour le contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message retourne le délai d’expiration de la reconnaissance, en millisecondes.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_SETRECOTIMEOUT em<br/>       | Définit le délai d’expiration de la reconnaissance, en millisecondes, pour le contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Spécifie le délai d’expiration de la reconnaissance, en millisecondes.<br/>*lParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                                                                                                    |
| \_GETGESTURESTATUS em<br/>     | Obtient l’état du mouvement du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Spécifie le type de mouvement, tel que défini dans l’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/> Valeurs de retour :<br/> Ce message retourne la **valeur true** si le contrôle [InkEdit](inkedit-control-reference.md) s’abonne au geste ou **false** si le contrôle InkEdit ne s’abonne pas au geste.<br/>                                                                                                                                                                       |
| \_SETGESTURESTATUS em<br/>     | Définit l’état du geste pour le contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Spécifie le type de mouvement, tel que défini dans l’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Spécifie **true** si l’abonnement au geste est activé ou **false** si l’écoute du mouvement n’est pas activée.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/> Remarques :<br/> Cela ne doit être utilisé que si EM \_ GETSTATUS retourne la valeur \_ Idle.<br/>                                                                                                               |
| \_GETRECOGNIZER em<br/>        | Obtient le module de reconnaissance utilisé par le contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur vers un IInkRecognizer \* pour recevoir l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilisé par le contrôle [InkEdit](inkedit-control-reference.md) .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                   |
| \_SETRECOGNIZER em<br/>        | Définit le module de reconnaissance utilisé par le contrôle [InkEdit](inkedit-control-reference.md) . Si un [Factoid](factoid-constants.md) est utilisé pour le contrôle InkEdit, il doit être réappliqué après l’envoi de ce message.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur vers un IInkRecognizer \* pour définir l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que le contrôle [InkEdit](inkedit-control-reference.md) utilise pour une utilisation ultérieure.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/> Remarques :<br/> Cela ne doit être utilisé que si EM \_ GETSTATUS retourne la valeur \_ Idle.<br/> |
| \_GETFACTOID em<br/>           | Obtient le [Factoid](factoid-constants.md) à utiliser pour la reconnaissance.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur vers un BSTR pour recevoir la chaîne Factoid.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETFACTOID em<br/>           | Définit le [Factoid](factoid-constants.md) à utiliser pour la reconnaissance.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie le BSTR qui contient la chaîne Factoid.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/> Remarques :<br/> Cela ne doit être utilisé que si EM \_ GETSTATUS retourne la valeur \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| \_GETSELINK em<br/>            | Obtient l’encre dans la sélection. L’encre doit être reconnue avant d’être accessible par le biais de ce message. S’il n’est pas reconnu en premier, EM \_ GETSELINK retourne toujours zéro objet [**InkDisp**](inkdisp-class.md) .<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur vers un VARIANT pour recevoir un tableau sécurisé afin de recevoir des objets [**InkDisp**](inkdisp-class.md) dans la sélection actuelle.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                     |
| \_SETSELINK em<br/>            | Définit l’encre dans la sélection. l’envoi de ce message n’a aucun effet s’il est utilisé avec un système d’exploitation autre que Windows XP édition Tablet PC.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un pointeur vers un VARIANT avec un tableau sécurisé d’objets [**InkDisp**](inkdisp-class.md) pour remplacer la sélection actuelle.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                     |
| \_GETSELINKDISPLAYMODE em<br/> | Retourne l’apparence actuelle de l’encre dans la plage sélectionnée à l’aide de l’une des valeurs de l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message renvoie l’une des valeurs de l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) ( \_ texte IDM ou \_ Ink IDM), qui spécifie la façon dont une sélection apparaît sur le contrôle.<br/>                                                                                                                                                                                                                           |
| \_SETSELINKDISPLAYMODE em<br/> | Définit l’apparence de l’encre dans la plage sélectionnée à l’aide de l’une des valeurs de l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie la manière dont l’entrée manuscrite apparaît dans la plage sélectionnée, comme défini dans l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit. l’envoi de ce message n’a aucun effet s’il est utilisé avec un système d’exploitation autre que Windows XP édition Tablet PC.<br/>                                                                                                   |
| EM \_ GETSTATUS<br/>            | Obtient l’état du contrôle [InkEdit](inkedit-control-reference.md) .<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message retourne l’une des valeurs de l’énumération [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) , qui spécifie si le contrôle est inactif, collecte d’encre ou reconnaissant l’encre.<br/>                                                                                                                                                                                                                                                                                                           |
| \_reconnaissance em<br/>            | Force la reconnaissance.<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_GETMOUSEICON em<br/>         | Obtient l’icône de la souris.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Spécifie un \* pointeur HICON qui est rempli avec l’actuel [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) HICON. Il peut s’agir d’un HICON ou d’une valeur **null** .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETMOUSEICON em<br/>         | Définit l’icône de la souris.<br/> Paramètres :<br/>*wParam* Spécifie une valeur BOOLÉENNE qui a la valeur **true** si le contrôle [InkEdit](inkedit-control-reference.md) doit posséder le handle HICON ou **false** si le contrôle InkEdit ne doit pas posséder le handle HICON. Si le contrôle InkEdit est propriétaire de HICON, il se charge et détruit correctement le HICON. Dans le cas contraire, l’appelant est propriétaire du HICON et est chargé de le supprimer.<br/>*lParam* Spécifie la nouvelle valeur HICON. Utilisez **null** pour effacer la valeur. La valeur par défaut est **NULL**.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                |
| \_GETMOUSEPOINTER em<br/>      | Obtient le pointeur de la souris.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Contient un \* pointeur InkMousePointer qui est rempli avec la valeur [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) actuelle. Cela se comporte de la même façon que la propriété **InkCollector :: obtenir \_ MousePointer** .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                                            |
| \_SETMOUSEPOINTER em<br/>      | Définit le pointeur de la souris.<br/> Paramètres :<br/>*wParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/>*lParam* Contient la nouvelle valeur [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) , qui est définie dans l’énumération [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) . Cela se comporte comme la propriété **InkCollector ::p ut \_** .<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/>                                                                                                                                                                                                                                    |
| \_GETUSEMOUSEFORINPUT em<br/>  | Obtient l’état indiquant si l’entrée de la souris est traitée comme une entrée de stylet.<br/> Paramètres :<br/> Ce message n’a pas de paramètre ; *wParam* et *lParam* doivent avoir la valeur 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 si la valeur est **false** ou 1 si la **valeur est true**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETUSEMOUSEFORINPUT em<br/>  | Définit l’état indiquant si l’entrée de la souris est traitée comme une entrée de stylet.<br/> Paramètres :<br/>*wParam* Spécifie une valeur booléenne qui détermine s’il faut traiter l’entrée de souris comme une entrée de stylet.<br/>*lParam* Ce paramètre n’est pas utilisé ; elle doit être égale à 0.<br/> Valeurs de retour :<br/> Ce message retourne 0 en cas de réussite ou une valeur différente de zéro si une erreur se produit.<br/> Remarques :<br/> Cela ne doit être utilisé que si EM \_ GETSTATUS retourne la valeur \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Message de notification d’événement         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IECN le \_ trait<br/>            | Notifie la fenêtre parente du contrôle [InkEdit](inkedit-control-reference.md) qu’un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) a été créé. Elle est envoyée dans un \_ message WM Notify avec les paramètres suivants.<br/> Paramètres :<br/>*wParam* Spécifie l’identificateur du contrôle qui a envoyé le message.<br/>*lParam* Spécifie un pointeur vers la structure [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) .<br/> Valeurs de retour :<br/> Le client retourne 0 pour accepter le trait et 1 pour annuler le trait.<br/> |
| \_mouvement IECN<br/>           | Notifie la fenêtre parente du contrôle [InkEdit](inkedit-control-reference.md) qu’un mouvement a été reconnu. Elle est envoyée dans un \_ message WM Notify avec les paramètres suivants.<br/> Paramètres :<br/>*wParam* Spécifie l’identificateur du contrôle qui a envoyé le message.<br/>*lParam* Spécifie un pointeur vers la structure [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) .<br/> Valeurs de retour :<br/> Le client retourne 0 pour accepter le geste et 1 pour annuler le mouvement.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Notifie la fenêtre parente du contrôle [InkEdit](inkedit-control-reference.md) que la reconnaissance s’est produite. Elle est envoyée dans un \_ message WM Notify avec les paramètres suivants.<br/> Paramètres :<br/>*wParam* Spécifie l’identificateur du contrôle qui a envoyé le message.<br/>*lParam* Spécifie un pointeur vers la structure [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) .<br/> Valeurs de retour :<br/> Le client retourne 0 s’il traite le message.<br/>                                  |



 

## <a name="applies-to"></a>S'applique à

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IEC \_ GESTUREINFO, structure (Win32 uniquement)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**IEC \_ STROKEINFO, structure (Win32 uniquement)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**IEC \_ RECOGNITIONRESULTINFO, structure (Win32 uniquement)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**MousePointer, propriété**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**Énumération InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**Énumération InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**Énumération InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDrawingAttributes, classe**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkDisp, classe**](inkdisp-class.md)
</dt> <dt>

[**Interface IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

