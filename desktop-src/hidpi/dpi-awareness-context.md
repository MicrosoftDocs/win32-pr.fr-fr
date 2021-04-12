---
title: Handle de DPI_AWARENESS_CONTEXT (WINDEF. h)
description: Identifie le contexte de sensibilisation pour une fenêtre.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317277"
---
# <a name="dpi_awareness_context-handle"></a>Handle de contexte de \_ détection PPP \_

Identifie le contexte de sensibilisation pour une fenêtre.

## <a name="syntax"></a>Syntaxe

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Constantes

**contexte de détection DPI ne \_ \_ \_ connaissant pas**<dl> Prise en charge de DPI ignorée. Cette fenêtre n’est pas mise à l’échelle pour les modifications PPP et est toujours supposée avoir un facteur d’échelle de 100% (96 ppp). Il est automatiquement mis à l’échelle par le système sur n’importe quel autre paramètre PPP.  
</dl>

**\_prise en \_ charge du contexte de détection dpi \_ \_**<dl> Prise en charge DPI système. Cette fenêtre n’est pas mise à l’échelle pour les modifications PPP. Elle interroge l’PPP une fois et utilise cette valeur pour la durée de vie du processus. Si les PPP changent, le processus ne s’ajuste pas à la nouvelle valeur PPP. Il est automatiquement mis à l’échelle par le système lorsque la valeur PPP change de la valeur système.  
</dl>

**\_prise en charge du contexte de détection dpi \_ \_ par \_ moniteur \_**<dl> Prise en charge de la résolution par moniteur. Cette fenêtre vérifie la résolution des PPP lorsqu’elle est créée et ajuste le facteur d’échelle à chaque modification de la résolution. Ces processus ne sont pas automatiquement mis à l’échelle par le système.  
</dl>

**\_Contexte de sensibilisation dpi \_ \_ par \_ analyse \_ \_ v2**<dl> Également appelé **par moniteur v2**. Progression sur le mode de prise en charge DPI par moniteur d’origine, qui permet aux applications d’accéder aux nouveaux comportements de mise à l’échelle en fonction de la DPI sur une base de fenêtre de niveau supérieur.  
Par moniteur V2 a été mis à disposition dans le créateur mise à jour de Windows 10, et n’est pas disponible dans les versions antérieures du système d’exploitation.  
Les comportements supplémentaires introduits sont les suivants :

-   **Notifications de modification dpi de la fenêtre enfant** : dans les contextes de l’analyse, la totalité de l’arborescence de la fenêtre est notifiée des modifications PPP qui se produisent.
-   **Mise à l’échelle d’une zone non cliente** : toutes les fenêtres ont automatiquement leur zone non cliente dessinée en fonction des PPP. Les appels à [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) ne sont pas nécessaires.
-   **Mise à l’échelle des menus Win32** : tous les menus Ntuser créés dans les contextes de par moniteur v2 feront l’d’une mise à l’échelle en fonction de chaque moniteur.
-   **Mise à l’échelle** de la boîte de dialogue : les boîtes de dialogue Win32 créées dans les contextes par moniteur v2 répondent automatiquement aux modifications PPP.
-   **Amélioration de la mise à l’échelle des contrôles Comctl32** : divers contrôles Comctl32 ont amélioré le comportement de mise à l’échelle PPP dans les contextes de chaque moniteur v2.
-   **Amélioration du comportement des thèmes** : les descripteurs Uxtheme ouverts dans le contexte d’une fenêtre par moniteur v2 fonctionnent en fonction de la résolution associée à cette fenêtre.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI ne connaissant pas la qualité améliorée du contenu basé sur GDI. Ce mode se comporte de la même façon que DPI_AWARENESS_CONTEXT_UNAWARE, mais il permet également au système d’améliorer automatiquement la qualité de rendu du texte et d’autres primitives basées sur GDI lorsque la fenêtre est affichée sur un moniteur haute résolution.

Pour plus d’informations, consultez [amélioration de l’expérience haute résolution dans les applications de bureau GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED a été introduite dans la mise à jour 2018 d’octobre de Windows 10 (également connue sous le nom de version 1809).


## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|----|-----------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1607 \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge <br/>  |
| En-tête<br/>                   | <dl> <dt>WINDEF. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AreDpiAwarenessContextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
