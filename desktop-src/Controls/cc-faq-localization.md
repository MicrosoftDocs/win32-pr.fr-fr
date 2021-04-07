---
title: Prise en charge de la localisation des contrôles communs
description: Cette rubrique décrit la prise en charge des langues nationales intégrées aux contrôles communs.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939757"
---
# <a name="localization-support-for-common-controls"></a>Prise en charge de la localisation des contrôles communs

Cette rubrique décrit la prise en charge des langues nationales intégrées aux contrôles communs. La prise en charge intégrée du langage national simplifie l’implémentation des applications localisées.

Cette rubrique contient les sections suivantes :

-   [Spécification d’une langue pour les contrôles communs](#specifying-a-language-for-the-common-controls)
-   [Spécification d’une langue pour les contrôles dans une boîte de dialogue](#specifying-a-language-for-controls-in-a-dialog-box)
-   [Rubriques connexes](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>Spécification d’une langue pour les contrôles communs

Si vous souhaitez spécifier une langue pour les contrôles communs qui est différente de la langue du système, appelez [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). Le langage spécifié par cette fonction s’applique uniquement au processus à partir duquel la fonction est appelée.

Pour déterminer la langue actuellement utilisée par les contrôles communs, appelez [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage). Elle retourne la valeur qui a été définie par un appel précédent à [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). Le langage retourné est celui qui a été spécifié pour le processus à partir duquel il est appelé. Si **InitMUILanguage** n’a pas été appelé ou a été appelé à partir d’un autre processus, **GetMUILanguage** retourne une valeur par défaut.

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>Spécification d’une langue pour les contrôles dans une boîte de dialogue

Contrairement aux contrôles communs, les contrôles prédéfinis, tels que les boutons ou les zones d’édition, n’utilisent pas la langue actuelle du système par défaut. Le contrôle de police natif est un contrôle invisible qui fonctionne en arrière-plan pour permettre aux contrôles prédéfinis d’une boîte de dialogue d’afficher la langue actuelle du système.

Pour utiliser le contrôle de police natif, procédez comme suit.

1.  Initialisez le contrôle de police natif en appelant [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Définissez le membre **dwICC** de la structure [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) désignée par *lpInitCtrls* à la \_ classe ICC NATIVEFNTCTL \_ .
2.  Ajoutez le contrôle au script de ressources pour la boîte de dialogue. Définissez un ou plusieurs des indicateurs de style suivants pour spécifier les contrôles qui seront affectés. 

    | Indicateur              | S’applique à                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_modification NFS         | Contrôles d’édition                                                                                                                                                                                                                                                    |
    | NFS \_ statique       | Contrôles statiques                                                                                                                                                                                                                                                  |
    | \_LISTCOMBO NFS    | Contrôles List, ComboBox, List-View et ComboBoxEx                                                                                                                                                                                                               |
    | \_bouton NFS       | Contrôles boutons                                                                                                                                                                                                                                                  |
    | \_tout NFS          | Tous les contrôles                                                                                                                                                                                                                                                     |
    | \_USEFONTASSOC NFS | Plateforme d’Extrême-Orient. Le contrôle utilise la fonctionnalité d’association de polices au lieu de basculer vers la police native. Toutes les autres plateformes l’ignorent. Cela est déconseillé pour Windows Vista et n’est pas pris en charge dans COMCTL V6. Cela existe dans COMCTL V5 pour des raisons d’héritage. |

    

     

L’exemple suivant montre comment ajouter un contrôle de police natif à un script de ressources. Les contrôles Edit, List et zone de liste modifiable de la boîte de dialogue affichent le texte à l’aide de la langue système actuelle.


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles communs](common-controls-intro.md)
</dt> </dl>

 

 




