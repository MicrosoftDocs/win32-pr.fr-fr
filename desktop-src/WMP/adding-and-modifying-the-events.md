---
title: Ajout et modification des événements
description: Ajout et modification des événements
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Exemple de plug-in DSP Echo, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310606"
---
# <a name="adding-and-modifying-the-events"></a>Ajout et modification des événements

Vous devez fournir des gestionnaires d’événements pour les \_ événements en modification qui se produisent lorsque l’utilisateur modifie le texte dans les zones d’édition de la page de propriétés. Ces gestionnaires d’événements ont une implémentation simple qui active simplement **apply** dans la boîte de dialogue page de propriétés.

## <a name="modifying-the-scale-factor-event-handler"></a>Modification du gestionnaire d’événements de facteur d’échelle

Vous devez modifier le nom du gestionnaire d’événements existant fourni par l’Assistant de plug-in pour la zone d’édition facteur d’échelle. Vous devez remplacer le nom OnChangeScale par OnChangeDelay dans trois emplacements :

1.  Dans EchoPropPage. h, modifiez le nom dans la section macro de la table des messages. Remplacez la ligne qui mappe l’événement de modification du facteur d’échelle à la méthode OnChangeScale par le code suivant :
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  Dans EchoPropPage. h, modifiez le nom de la ligne qui prototype la fonction OnChangeScale :
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  Dans EchoPropPage. cpp, modifiez le nom dans l’en-tête de fonction :
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Ajout du gestionnaire d’événements de mélange mouillé

Vous pouvez facilement ajouter le gestionnaire d’événements pour l' \_ événement en modification attaché au \_ contrôle de zone d’édition WETMIX d’IDC. Dans l’éditeur de ressources de boîte de dialogue :

1.  Cliquez avec le bouton droit sur la \_ zone d’édition IDC WETMIX et choisissez **événements**. La boîte de dialogue nouveaux messages et gestionnaires d’événements Windows s’affiche.
2.  Dans la zone **classe ou objet à gérer** , cliquez sur le nom de la ressource de zone d’édition, IDC \_ WETMIX.
3.  Dans la zone **nouveaux messages/événements Windows** , cliquez sur \_ Modifier pour le sélectionner.
4.  Cliquez sur **Ajouter un gestionnaire**. La boîte de dialogue Ajouter une fonction membre s’affiche.
5.  Dans la zone nom de la **fonction membre** , tapez le nom OnChangeWetmix.
6.  Cliquez sur **OK** pour fermer la boîte de dialogue Ajouter une fonction membre.
7.  Cliquez sur **OK** pour revenir à l’éditeur de ressources de la boîte de dialogue.

Visual C++ ajoute automatiquement le code pour la table des messages et pour la fonction de gestionnaire d’événements à EchoPropPage. h. Le code qu’il insère fournit un commentaire TODO dans lequel vous pouvez ajouter l’implémentation dans l’en-tête pour la fonction. Il s’agit d’un style légèrement différent de celui utilisé par l’exemple de code du plug-in du lecteur Windows Media, mais il est acceptable.

Que vous souhaitiez écrire votre implémentation dans le fichier d’en-tête ou la déplacer vers EchoPropPage. cpp vous convient. Dans les deux cas, l’implémentation a besoin d’une seule ligne de code supplémentaire pour activer l' **application** dans la boîte de dialogue de la page de propriétés. Insérez cette ligne de code avant la ligne qui retourne à partir de la fonction :


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




