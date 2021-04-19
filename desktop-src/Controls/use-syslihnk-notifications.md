---
title: Utilisation des notifications SysLink
description: Deux messages de notification sont associés au contrôle SysLink \ 8212 ; un pour la souris (en- \_ cliquant sur Syslink) et l’autre pour le clavier (retour nm \_ ).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "106511277"
---
# <a name="how-to-use-syslink-notifications"></a>Utilisation des notifications SysLink

Deux messages de notification sont associés au contrôle SysLink : un pour la souris (un[clic nm ( \_ Syslink)](nm-click-syslink.md)) et l’autre pour le clavier ([ \_ retour nm](nm-return.md)).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="use-syslink-notifications"></a>Utiliser des notifications SysLink

L’exemple de code suivant montre comment traiter les notifications SysLink générées lorsque l’utilisateur clique sur l’un des deux liens dans l' [exemple précédent](create-syslink-controls.md). Lorsque l’utilisateur clique sur l’URL Internet, la page Web associée s’ouvre dans le navigateur par défaut. Quand l’utilisateur clique sur le lien hypertexte défini par l’application, une boîte de message s’affiche.


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles SysLink](using-syslink-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




