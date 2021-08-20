---
title: Comment traiter la notification de DTN_WMKEYDOWN
description: Cette rubrique montre comment traiter une notification DTN \_ WMKEYDOWN. La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbef0804afb388f9cadad60b04bf93ce4730ef255476f0c7f216edfd24846a19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540349"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Comment traiter la notification DTN \_ WMKEYDOWN

Cette rubrique montre comment traiter une notification [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Les contrôles de sélecteur de date et d’heure (PAO) envoient le message [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) pour signaler que l’utilisateur a entré une entrée dans un champ de rappel. Si vous souhaitez émuler les mêmes réponses de clavier que celles prises en charge pour les champs de PAO standard ou fournir des réponses personnalisées, votre application doit inclure du code pour gérer cette notification.

L’exemple de code C++ suivant est une fonction définie par l’application qui traite la notification [ \_ WMKEYDOWN DTN](dtn-wmkeydown.md) .

**Avertissement de sécurité :** L’utilisation incorrecte de **lstrcmp** peut compromettre la sécurité de votre application. Par exemple, avant d’appeler **lstrcmp** dans l’exemple de code suivant, vous devez vous assurer que les deux chaînes se terminent par un caractère null. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)
</dt> <dt>

[Référence de contrôle de sélecteur de date et heure](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




