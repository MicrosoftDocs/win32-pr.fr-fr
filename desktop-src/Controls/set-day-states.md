---
title: Comment définir les États des jours
description: Cette rubrique montre comment définir les informations d’État du jour. Le contrôle Month Calendar utilise les informations d’État du jour pour déterminer comment il dessine des jours spécifiques dans le contrôle.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116981"
---
# <a name="how-to-set-day-states"></a>Comment définir les États des jours

Cette rubrique montre comment définir les informations d’État du jour. Le contrôle Month Calendar utilise les informations d’État du jour pour déterminer comment il dessine des jours spécifiques dans le contrôle.

Les contrôles de calendrier mensuel qui utilisent les États du jour du support de style [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) . Les informations d’État du jour sont exprimées sous la forme d’un type de données 32 bits, [**MONTHDAYSTATE**](monthdaystate.md). Chaque bit dans un champ de bits **MONTHDAYSTATE** (0 à 30) spécifie l’état d’un jour dans un mois. Si un bit est activé, le jour correspondant est affiché en gras.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Une application peut définir explicitement des informations d’état de jour en envoyant le message [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) ou en utilisant la macro correspondante, [**calendrier monthcal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Toutefois, les informations d’État du jour sont généralement définies en réponse au code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , qui est envoyé chaque fois que le contrôle doit être actualisé car, par exemple, un autre mois a fait défiler la vue.

L’exemple de code suivant montre comment traiter le code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) dans un gestionnaire de messages [**WM \_ Notify**](wm-notify.md) . Il traite MCN \_ GETDAYSTATE en spécifiant que le premier et le quinzième jour de chaque mois visible doivent être mis en surbrillance. Le membre **cDayState** de la structure [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) spécifie le nombre de valeurs [**MONTHDAYSTATE**](monthdaystate.md) nécessaires dans le tableau, qui reçoit une taille maximale arbitraire. Le code effectue ensuite une boucle pour définir les bits appropriés dans chaque élément valide du tableau, à l’aide de la macro **BOLDDAY** définie par l’application.



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle Month Calendar](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[À propos des contrôles Month Calendar](month-calendar-controls.md)
</dt> <dt>

[Utilisation des contrôles Month Calendar](using-month-calendar-controls.md)
</dt> </dl>

 

 




