---
title: Modification de la ressource de boîte de dialogue Echo
description: Modification de la ressource de boîte de dialogue Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
- Echo DSP, exemple de plug-in, ressource de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37dc88fe2c1b85dfc08727a00e744f1c5c16a2f25a4c5d429b2ab13898b0fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996139"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modification de la ressource de boîte de dialogue Echo

Vous devez modifier la ressource de boîte de dialogue qui est l’interface utilisateur de l’objet de page de propriétés. Vous pouvez d’abord modifier la zone d’édition et l’étiquette existantes afin qu’elles soient utiles pour la propriété délai, puis ajouter une deuxième zone d’édition et une autre étiquette pour la propriété de combinaison humide.

Pour modifier la ressource de boîte de dialogue dans Visual C++ :

1.  cliquez sur l’onglet **ResourceView** dans l’espace de travail Project.
2.  Développez l’arborescence ressources en ouvrant le dossier de niveau supérieur.
3.  Ouvrez le dossier **boîte de dialogue** .
4.  Double-cliquez sur le nom de la ressource de boîte de dialogue, IDD \_ ECHOPROPPAGE. L’éditeur de ressources s’affiche dans le volet droit.

## <a name="changing-the-existing-resources"></a>Modification des ressources existantes

Pour modifier les ressources de la page de propriétés existante pour la propriété Delay Time :

1.  Tout d’abord, modifiez le texte dans le contrôle de texte statique existant. Cliquez avec le bouton droit sur le contrôle, puis choisissez **Propriétés**. Dans le champ **légende** , tapez la nouvelle légende :
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Fermez la boîte de dialogue Propriétés du texte.
3.  À présent, modifiez le nom du contrôle zone d’édition. Pour ce faire, cliquez avec le bouton droit sur le contrôle, puis choisissez **Propriétés**. Dans le champ **ID** , tapez un nouveau nom pour le contrôle :
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Fermez la boîte de dialogue Modifier les propriétés.
5.  Enregistrez la ressource.
6.  Répondez **Oui** si vous êtes invité à recharger le fichier Resource. h.
7.  cliquez sur l’onglet **FileView** dans l’espace de travail Project. Ouvrez Resource. h
8.  Recherchez la \# ressource définir pour la zone d’édition du facteur d’échelle (IDC \_ SCALEFACTOR) et supprimez-la. Il doit avoir le même numéro d’ID qu’IDC \_ DELAYTIME.

## <a name="adding-the-new-resources"></a>Ajout des nouvelles ressources

Pour ajouter les nouvelles ressources de la page de propriétés pour la propriété de combinaison humide :

1.  cliquez sur l’onglet **ResourceView** dans l’espace de travail Project pour le sélectionner.
2.  Double-cliquez sur le nom de la boîte de dialogue page de propriétés, IDD \_ ECHOPROPPAGE. L’éditeur de ressources s’affiche dans le volet droit.
3.  Utilisez la boîte à outils pour ajouter un contrôle de texte statique et une zone d’édition à la page de propriétés.
4.  Cliquez avec le bouton droit sur le contrôle texte statique et choisissez **Propriétés**.
5.  Tapez un nouveau nom pour le contrôle de texte statique dans le champ **ID** :
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Tapez une légende pour l’étiquette :
    ```C++
    Effect level (%):
    
    ```

    

7.  Fermez la boîte de dialogue Propriétés du texte.
8.  Cliquez avec le bouton droit sur la zone d’édition et choisissez **Propriétés**.
9.  Tapez un nouveau nom pour la zone d’édition dans le champ **ID** :
    ```C++
    IDC_WETMIX
    
    ```

    

10. Fermez la boîte de dialogue Modifier les propriétés.

Lorsque vous enregistrez le projet, vous pouvez être invité à recharger Resource. h. Si cela se produit, cliquez sur **Oui** . L’éditeur de ressources de boîte de dialogue doit ajouter les noms de ressources et les numéros d’ID à Resource. h pour les éléments que vous avez ajoutés. Si, pour une raison quelconque, cela ne se produit pas, vous devez ouvrir Resource. h et taper de nouvelles entrées pour l’étiquette et le contrôle de zone d’édition, et assigner à chacun un numéro d’identification unique.

## <a name="modifying-and-adding-the-string-resources"></a>Modification et ajout des ressources de type chaîne

L’exemple de code de l’Assistant de plug-in spécifie une ressource de type chaîne nommée IDS \_ SCALERANGEERROR qui contient un message à afficher lorsque l’entrée utilisateur est hors limites. Vous pouvez modifier cette ressource en fonction de vos besoins pour la valeur de délai en procédant comme suit dans Visual C++ :

1.  Cliquez sur l’onglet **ResourceView** .
2.  Ouvrez le dossier **table de chaînes** .
3.  Double-cliquez sur l’icône de la **table de chaînes** pour ouvrir l’éditeur de ressources.
4.  Double-cliquez sur le nom de la ressource que vous souhaitez modifier, dans le cas présent, IDS \_ SCALERANGEERROR. La boîte de dialogue Propriétés de la chaîne s’affiche.
5.  Remplacez le nom dans le champ **ID** par IDS \_ DELAYRANGEERROR.
6.  Modifiez le texte dans le champ **légende** :
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Fermez la boîte de dialogue Propriétés de la chaîne.

Ensuite, ajoutez une nouvelle ressource de type chaîne pour le message d’erreur de propriété de combinaison humide.

1.  Double-cliquez sur la ligne vide en bas de l’éditeur de ressources.
2.  Remplacez le nom dans le champ **ID** par IDS \_ MIXRANGEERROR.
3.  Ajoutez le texte suivant au champ **Caption** :
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Fermez la boîte de dialogue Propriétés de la chaîne.

Il existe deux autres valeurs que vous pouvez modifier dans la table de chaînes. id \_ FRIENDLYNAME est le nom qui apparaît dans l’interface utilisateur Lecteur Windows Media pour identifier le plug-in. Description des ID \_ vous permet de donner à l’utilisateur des informations sur votre plug-in. Ces deux chaînes sont passées en tant que paramètres à la fonction **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin** , qui est appelée dans la méthode DllRegisterServer dans Echodll. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification de la page de propriétés de l’exemple Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




