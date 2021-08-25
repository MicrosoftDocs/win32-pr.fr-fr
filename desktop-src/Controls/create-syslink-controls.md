---
title: Comment créer des contrôles SysLink
description: Implémentez les liens hypertexte du contrôle SysLink par le biais du balisage dans la chaîne d’initialisation du contrôle, ou en lui envoyant un \_ message LM SETITEM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878509"
---
# <a name="how-to-create-syslink-controls"></a>Comment créer des contrôles SysLink

Implémentez les liens hypertexte du contrôle SysLink par le biais du balisage dans la chaîne d’initialisation du contrôle, ou en lui envoyant un message [**LM \_ SETITEM**](lm-setitem.md) .

> [!Note]  
> Avant de créer des contrôles SysLink, vous devez appeler la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant la \_ classe de liaison ICC \_ .

 

Pour créer un SysLink, appelez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de [**\_ liaison WC**](common-control-window-classes.md) . Le paramètre *lpWindowName* qui est commun à ces fonctions spécifie un pointeur vers une chaîne se terminant par zéro qui contient le texte marqué à afficher. Pour les styles de fenêtre particuliers aux contrôles SysLink, consultez [Syslink Control styles](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-syslink-control"></a>Créer un contrôle SysLink

L’exemple de code suivant crée un contrôle SysLink qui affiche deux liens hypertexte. Le premier lien hypertexte est une URL Internet et le second est défini par l’application.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Remarques

Il est supposé que [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) a déjà été appelé.

Si vous spécifiez le style [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) , l’utilisateur est en mesure de sélectionner un lien en cliquant dessus et en appuyant sur la touche entrée.

La version 6 de ComCtl32.dll prend en charge Unicode uniquement. Par conséquent, vous ne pouvez pas créer de versions ANSI de contrôles SysLink (Unicode uniquement).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 