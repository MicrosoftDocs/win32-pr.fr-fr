---
description: dans Windows Vista, le panneau de saisie Tablet PC intègre de nouvelles fonctionnalités de saisie semi-automatique qui permettent à la liste de saisie semi-automatique d’une application d’être mise à jour en temps réel lorsque l’encre d’un utilisateur est reconnue dans le panneau de saisie.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Utilisation de la saisie semi-automatique du panneau de saisie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb0589cca00a45d007c7df6a605f051161c07a62c864504780c307693fe8897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934376"
---
# <a name="using-input-panel-autocomplete"></a>Utilisation de la saisie semi-automatique du panneau de saisie

dans Windows Vista, le panneau de saisie Tablet PC intègre de nouvelles fonctionnalités de saisie semi-automatique qui permettent à la liste de saisie semi-automatique d’une application d’être mise à jour en temps réel lorsque l’encre d’un utilisateur est reconnue dans le panneau de saisie. En outre, la liste de saisie semi-automatique de l’application est positionnée dans un emplacement pratique pour les utilisateurs du panneau de saisie. Sans la saisie semi-automatique du panneau de saisie, l’utilisation des fonctionnalités de saisie semi-automatique avec le panneau de saisie est un processus difficile, qui oblige les utilisateurs à insérer un caractère à la fois et à déplacer le panneau de saisie pour accéder aux suggestions de saisie semi-automatique. Avec l’intégration, la saisie semi-automatique est un outil puissant pour les utilisateurs de Tablet PC qui accélère et augmente la facilité d’entrée de texte avec le panneau de saisie.

![panneau de saisie avec la liste de saisie semi-automatique IE](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Il existe trois options pour la façon dont une application peut tirer parti de l’intégration de la saisie semi-automatique du panneau de saisie. les Applications qui contiennent la fonctionnalité de saisie semi-automatique construite à l’aide de la saisie semi-automatique de l’interpréteur de commandes (via l’interface [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) ) ou .NET Framework la saisie semi-automatique (via l’énumération [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) ) reçoivent l’intégration de la saisie semi-automatique du panneau de saisie sans Les applications qui incluent des champs de texte de saisie semi-automatique personnalisés peuvent utiliser l’API de saisie semi-automatique du panneau de saisie pour obtenir la même fonctionnalité.

Dans tous les cas, vous pouvez apporter ces modifications à la liste de saisie semi-automatique de l’application sans dupliquer ni modifier l’interface utilisateur ou la logique de prédiction utilisée par une application pour générer une liste de saisie semi-automatique. La liste de saisie semi-automatique continue d’être propriétaire de l’application et le contenu de la liste de saisie semi-automatique est le même que si le texte a été tapé directement dans le champ d’édition.

l’intégration de la saisie semi-automatique du panneau de saisie est prise en charge sur le système d’exploitation Windows Vista ou les versions ultérieures. l’intégration de la saisie semi-automatique du panneau de saisie est intégrée à la saisie semi-automatique de l’interpréteur de commandes à partir de Windows Vista et Windows Forms développement à partir de .NET Framework version 3,0. tandis que [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) et [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) sont exécutés sur des versions antérieures de Windows, l’intégration de la saisie semi-automatique du panneau de saisie n’est pas prise en charge sur Microsoft Windows XP Tablet PC Edition ou les systèmes d’exploitation antérieurs. Si vous exécutez la saisie semi-automatique du panneau de saisie sur des versions antérieures de Tablet PC, les applications reprennent le comportement de pré-intégration.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Raisons pour intégrer les listes de saisie semi-automatique des applications au panneau de saisie

L’intégration de la liste de saisie semi-automatique d’une application permet d’accélérer et de réduire la vitesse d’entrée pour les utilisateurs qui entrent du texte dans un champ de texte qui comprend la fonctionnalité de saisie semi-automatique. En outre, une application qui comprend l’intégration de la saisie semi-automatique du panneau de saisie apparaît immédiatement comme si elle avait été développée avec le Tablet PC à l’esprit, ce qui rend l’application plus attrayante pour les utilisateurs de Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Interaction entre le panneau de saisie et la liste de saisie semi-automatique sans intégration

Utilisation du panneau de saisie pour entrer du texte dans un champ de texte qui comprend une liste de saisie semi-automatique mais qui n’est pas intégré au panneau de saisie :

1.  L’utilisateur place le focus dans le champ de texte et ouvre le panneau de saisie.
2.  L’utilisateur écrit un ou deux caractères.
3.  L’utilisateur appuie sur **Inser**. Le panneau de saisie entre le texte dans le champ de texte de l’application. La liste de saisie semi-automatique de l’application s’affiche et est probablement partiellement ou complètement masquée par le panneau de saisie.
4.  L’utilisateur fait glisser le panneau de saisie pour découvrir la liste de saisie semi-automatique de l’application.
5.  En supposant que l’entrée correcte est incluse dans la liste de saisie semi-automatique, l’utilisateur peut maintenant sélectionner cette entrée. dans le cas contraire, l’utilisateur doit répéter les étapes 2 et 3.

Ce processus est clairement fastidieux. Les attentes de l’utilisateur quant à la façon dont une liste de saisie semi-automatique doit fonctionner sont en tirets et leur capacité à effectuer des tâches en pâtit.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Amélioration de l’interaction entre le panneau de saisie et la liste de saisie semi-automatique

Utilisation du panneau de saisie pour entrer du texte dans un champ de texte qui comprend une liste de saisie semi-automatique intégrée au panneau de saisie :

1.  L’utilisateur place le focus dans le champ de texte et ouvre le panneau de saisie.
2.  L’utilisateur écrit un ou deux caractères. La liste de saisie semi-automatique de l’application apparaît juste au-dessus ou directement sous le panneau de saisie lorsque l’utilisateur écrit du texte.
3.  L’utilisateur sélectionne l’entrée dans la liste de saisie semi-automatique. l’entrée est insérée directement dans le champ de texte de l’application, ou l’utilisateur répète l’étape 2 jusqu’à ce que l’entrée correcte apparaisse.

En raison de l’intégration, la liste de saisie semi-automatique s’affiche et est mise à jour pendant que l’utilisateur écrit dans le panneau de saisie. En outre, la liste est positionnée de manière à ce qu’elle soit à la fois pratique pour l’utilisateur et pour l’accès en écriture et non masquée par le panneau de saisie. Enfin, lorsque l’utilisateur sélectionne un élément dans une liste de saisie semi-automatique, l’élément est inséré directement dans le champ d’entrée de texte de l’application, ce qui permet à l’utilisateur de contourner l’étape d’insertion du texte à partir du panneau de saisie.

![panneau de saisie avec la liste de saisie semi-automatique Outlook Express](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Composants de saisie semi-automatique standard incluant l’intégration de la saisie semi-automatique du panneau de saisie

[**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) et [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) incluent une intégration intégrée de la saisie semi-automatique du panneau de saisie. Les applications utilisant l’un de ces composants standard de saisie semi-automatique peuvent tirer parti de la fonctionnalité de saisie semi-automatique du panneau de saisie, avec peu de travail supplémentaire. en outre, alors que la saisie semi-automatique du panneau de saisie est uniquement prise en charge sur Windows Vista ou les nouvelles versions du système d’exploitation Windows, les applications qui ont été créées à l’aide de **IAutoComplete** avant la sortie de Windows vista obtiennent automatiquement l’intégration de la saisie semi-automatique du panneau de saisie lorsqu’elles sont exécutées sur Windows Vista. Les sections suivantes contiennent des informations supplémentaires sur les éléments **IAutoComplete** et AutoCompleteMode spécifiques qui incluent l’intégration de la saisie semi-automatique du panneau de saisie.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Saisie semi-automatique du shell avec intégration de la saisie semi-automatique du panneau de saisie

Les applications qui utilisent [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) bénéficient de l’intégration de la saisie semi-automatique du panneau de saisie gratuitement. alors que les api de saisie semi-automatique de l’interpréteur de commandes sont incluses dans Windows 2000, l’intégration de la saisie semi-automatique du panneau de saisie est uniquement prise en charge sur Windows Vista et versions ultérieures toutefois, les applications générées avant la version de Windows vista qui utilisent **IAutoComplete** bénéficient automatiquement de l’intégration de la saisie semi-automatique du panneau de saisie lorsqu’elles sont exécutées sur Windows Vista.

Pour tirer parti de la saisie semi-automatique des tablettes de cette façon, vous devez utiliser l’objet de saisie semi-automatique (**\_ saisie semi**-automatique CLSID). Si vous souhaitez fournir une fonctionnalité de saisie semi-automatique pour les URL ou les noms de fichiers, utilisez la fonction [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) pour créer l’objet de saisie semi-automatique.

En plus de [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete), vous pouvez implémenter [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) ou [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)s directement, tout en continuant à bénéficier automatiquement de l’intégration de la saisie semi-automatique du panneau de saisie.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>intégration de la saisie semi-automatique du panneau de saisie avec les Applications .NET Framework

à partir de .NET Framework 3,0, Windows Forms zones de texte incluent la saisie semi-automatique. Windows La saisie semi-automatique des zones de texte est basée sur la saisie semi-automatique du shell, ce qui signifie également que l’intégration de la saisie semi-automatique du panneau de saisie est intégrée. .NET Framework 3,0 est pris en charge sur les éditions Windows antérieures à Windows Vista. toutefois, étant donné que l’intégration de la saisie semi-automatique du panneau de saisie est uniquement prise en charge sur Windows vista ou versions ultérieures, l’intégration de la saisie semi-automatique du panneau de saisie ne fonctionne que dans une application .NET Framework 3,0 lorsqu’elle est installée sur Windows Vista ou versions ultérieures.

les Applications qui souhaitent tirer parti de l’intégration de la saisie semi-automatique du panneau de saisie dans .NET Framework 3,0 doivent utiliser une [zone de texte](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Windows Forms avec la propriété [AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) activée. vous n’avez pas besoin d’effectuer d’autres tâches en plus de Windows Forms la saisie semi-automatique pour travailler pour tirer parti de l’intégration de la saisie semi-automatique du panneau de saisie.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Utilisation directe des API de saisie semi-automatique du panneau de saisie

Les développeurs de zones de texte à saisie semi-automatique personnalisée doivent travailler directement avec les API de saisie semi-automatique du panneau de saisie pour obtenir une expérience d’entrée de texte améliorée que l’intégration de la saisie semi-automatique du panneau de saisie permet dans leurs applications. les api de saisie semi-automatique du panneau de saisie sont incluses dans le système d’exploitation Windows Vista et dans le cadre du kit de développement logiciel (SDK) de plateforme Tablet 1,9 ou version ultérieure. Les interfaces de saisie semi-automatique du panneau de saisie sont des interfaces basées sur COM.

La section suivante décrit l’utilisation de ces interfaces en détail pour une application C++. Toutefois, ces interfaces COM peuvent être implémentées dans la plupart des langages, y compris C \# , via l’utilisation de COM Interop.

Afin d’implémenter l’intégration de la saisie semi-automatique du panneau de saisie dans une zone de texte de saisie semi-automatique personnalisée, les deux interfaces requises sont l' [**interface ITipAutocompleteProvider**](itipautocompleteprovider.md) et l' [**interface ITipAutocompleteClient**](itipautocompleteclient.md). Les définitions de ces interfaces se trouvent dans TipAutoComplete. h et TipAutoComplete \_ i.c.

Tout d’abord, une application doit définir et instancier une classe de fournisseur de saisie semi-automatique, qui implémente [**ITipAutocompleteProvider**](itipautocompleteprovider.md) pour chaque champ d’entrée de texte qui comprend une liste de saisie semi-automatique. Cette classe gère le côté de l’application de l’intégration de la saisie semi-automatique. Toutes les demandes de saisie semi-automatique à partir du panneau de saisie sont effectuées du client de saisie semi-automatique à l’application via le fournisseur de saisie semi-automatique de l’application. Le fournisseur de saisie semi-automatique de l’application doit avoir accès à la fois à HWND pour la liste de saisie semi-automatique de l’application et à HWIND pour le champ d’entrée de texte associé. En outre, les méthodes suivantes de **ITipAutocompleteProvider** doivent être implémentées :

-   [**ITipAutocompleteProvider :: UpdatePendingText, méthode**](itipautocompleteprovider-updatependingtext.md): cette méthode est utilisée par le client de saisie semi-automatique pour notifier l’application du texte qu’un utilisateur a écrit dans le panneau de saisie. Lors de la réception de cette notification, le fournisseur est responsable de la génération d’une liste de saisie semi-automatique comme si le texte avait été tapé dans le champ d’entrée de texte de l’application. La chaîne transmise au fournisseur de saisie semi-automatique au moyen de la **méthode ITipAutocompleteProvider :: UpdatePendingText** comprend uniquement le texte actuellement dans le panneau de saisie. Par conséquent, s’il y a du texte supplémentaire dans le champ d’entrée de texte, il incombe au fournisseur de l’ajouter correctement au texte envoyé par le client. Le passage de chaîne par la **méthode ITipAutocompleteProvider :: UpdatePendingText** doit être traité comme un remplacement de la sélection actuelle dans le champ. S’il n’y a aucune sélection actuelle, elle doit être placée à la position du point d’insertion actuel. Une fois la liste de saisie semi-automatique générée, le fournisseur doit appeler la [**méthode ITipAutocompleteProvider :: Show**](itipautocompleteprovider-show.md) en passant la **valeur true** pour afficher la liste de saisie semi-automatique. L’application ne doit pas mettre en cache les appels à **UpdatePendingText** , mais traiter chaque appel supplémentaire à **UpdatePendingText** en tant qu’annulation de l’appel précédent afin d’éviter le clignotement d’une interface utilisateur de liste de saisie semi-automatique obsolète. L’exemple de code suivant illustre ces pratiques.

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**ITipAutocompleteProvider :: Show, méthode**](itipautocompleteprovider-show.md): cette méthode est appelée à partir de [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md), mais elle peut également être appelée par le client de saisie semi-automatique à tout moment. Lors de la réception de cet appel, le fournisseur de saisie semi-automatique doit masquer ou afficher le fournisseur de saisie semi-automatique comme indiqué par le paramètre. Avant d’afficher la liste de saisie semi-automatique, le fournisseur de saisie semi-automatique est censé consulter le client de saisie semi-automatique concernant l’emplacement de la liste de saisie semi-automatique. Plus d’informations sur le positionnement de la liste de saisie semi-automatique apparaissent plus loin dans cet article.

Ensuite, l’application doit utiliser la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) Active Template Library (ATL) pour produire une instance de l' [**interface ITipAutocompleteClient**](itipautocompleteclient.md) avec l’ID de classe **CLSID \_ TipAutoCompleteClient** en tant que serveur in-process, puis inscrire le fournisseur auprès du client. La [**méthode ITipAutocompleteClient :: AdviseProvider**](itipautocompleteclient-adviseprovider.md) du client de saisie semi-automatique inscrit le fournisseur auprès du client pour permettre au client d’appeler l’objet fournisseur de saisie semi-automatique de l’application. Si tiptsf.dll n’est pas présent sur le système, la fonction **CoCreateInstance** échoue et retourne **RegDB \_ E \_ CLASSNOTREG**. À ce stade, l’application peut ignorer son objet [**ITipAutocompleteProvider**](itipautocompleteprovider.md) et se poursuivre comme si le panneau de saisie n’existait pas, car il ne s’agit pas d’un système de ce type.

L’application peut choisir de créer une instance de [**ITipAutocompleteClient**](itipautocompleteclient.md) ou une instance par champ de texte. La première option requiert l’annulation de l’inscription et de l’inscription du fournisseur chaque fois que le focus est modifié. Pour plus d’informations sur l’annulation de l’inscription du fournisseur de saisie semi-automatique, plus loin dans cette rubrique.

Plusieurs étapes sont nécessaires pour positionner la liste de saisie semi-automatique qui doit être coordonnée entre le fournisseur de saisie semi-automatique (application) et le client de saisie semi-automatique (panneau de saisie). Avant que la liste de saisie semi-automatique ne soit affichée, à la suite d’un appel à la méthode [**Show**](itipautocompleteprovider-show.md) du fournisseur de saisie semi-automatique ou en raison de l’entrée de texte par l’utilisateur à l’aide du clavier, le fournisseur est tenu de consulter le client sur l’emplacement de la liste de saisie semi-automatique. Le fournisseur doit effectuer les étapes suivantes :

-   Utilisez la [**méthode ITipAutocompleteClient :: RequestShowUI**](itipautocompleteclient-requestshowui.md) du client de saisie semi-automatique pour déterminer si le panneau de saisie est prêt à afficher la liste de saisie semi-automatique. **RequestShowUI** prend le paramètre *HWND* qui est le HWND de la fenêtre Liste de saisie semi-automatique, et la méthode retourne **true** ou **false** pour indiquer s’il s’agit de l’État dans lequel la liste de saisie semi-automatique peut être affichée. Si le client retourne la **valeur false**, le fournisseur ne doit pas tenter d’afficher la liste de saisie semi-automatique.
-   Appelez [**RequestShowUI**](itipautocompleteclient-requestshowui.md) pour définir le handle de fenêtre de la liste de saisie semi-automatique des fenêtres contextuelles avant d’appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md). Dans le cas contraire, une erreur d' **E \_ INVALIDARG** se produira lors de l’appel de **PreferredRects**.
-   Si [**RequestShowUI**](itipautocompleteclient-requestshowui.md) retourne la **valeur true**, le fournisseur doit calculer le rectangle de coordonnée d’écran par défaut de la liste de saisie semi-automatique en fonction de l’emplacement du champ d’entrée de texte, puis appeler la [**méthode ITipAutocompleteClient ::P referredrects**](itipautocompleteclient-preferredrects.md)du client de saisie semi-automatique. Cela permet au client de saisie semi-automatique d’ajuster le rectangle pour éviter que la liste de saisie semi-automatique se chevauche avec le panneau de saisie. La méthode **PreferredRects** accepte quatre paramètres :

    -   RECT *rcACList*: rectangle de coordonnée d’écran par défaut de la liste de saisie semi-automatique.
    -   RECT *rcField*: rectangle de la coordonnée d’écran du champ d’entrée de texte correspondant.
    -   RECT *\* prcModifiedACList*: rectangle de coordonnées d’écran ajusté pour la saisie semi-automatique
    -   BOOL *\* pfShowAbove*: ce paramètre indique au fournisseur si le rectangle *prcModifiedACList* place la liste de saisie semi-automatique au-dessus ou en dessous du panneau de saisie. L’application peut utiliser ces informations pour dessiner correctement les éléments d’interface utilisateur tels que les poignées de redimensionnement et les barres de défilement. Le fournisseur doit passer initialement dans la direction selon laquelle la liste de saisie semi-automatique est positionnée par rapport au champ d’entrée de texte par *rcACList*. Le client ne change pas *pfShowAbove* s’il définit *PrcModifiedACList* égal à *rcACList*.

    Utilisez les valeurs de retour des arguments *prcModifiedACList* et *pfShowAbove* out pour positionner et afficher la fenêtre Liste de saisie semi-automatique. Si le panneau de saisie n’est pas utilisé, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) retourne toujours **true** et *PrcModifiedACList* est toujours identique à *rcACList*. *pfShowAbove* est également inchangé, le résultat est que les appels n’ont aucun effet sur le comportement de l’application. L’exemple de code suivant illustre ces pratiques.


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



Lorsque l’utilisateur sélectionne un élément dans la liste de saisie semi-automatique, le fournisseur doit appeler la [**méthode ITipAutocompleteClient :: UserSelection**](itipautocompleteclient-userselection.md) du client en plus de l’insertion du texte de l’élément sélectionné dans le champ d’entrée de texte. Le panneau de saisie utilise cette notification pour ignorer tout le texte restant qui n’a pas encore été inséré à partir du panneau de saisie.

Enfin, lorsque le fournisseur n’est plus nécessaire, le fournisseur doit être dissocié du client de saisie semi-automatique en appelant la [**méthode ITipAutocompleteClient :: UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) du client de saisie semi-automatique pour annuler l’inscription du fournisseur. Il peut être nécessaire d’annuler l’inscription du fournisseur pour l’une des deux raisons suivantes : étant donné que le champ d’entrée de texte auquel le fournisseur est associé a été détruit, ou parce que l’application choisit de créer un seul client de saisie semi-automatique par champ d’entrée de texte. Dans cette instance, le fournisseur doit être désinscrit chaque fois que le focus est éloigné du champ de texte.

## <a name="conclusion"></a>Conclusion

l’intégration de la saisie semi-automatique du panneau de saisie est un outil puissant pour améliorer l’expérience utilisateur dans Windows applications qui incluent des listes de saisie semi-automatique sur les Tablet pc. Sans intégration, les utilisateurs du panneau de saisie doivent suivre un processus fastidieux d’insertion du texte un caractère à la fois et de repositionner le panneau de saisie pour pouvoir utiliser la saisie semi-automatique. Avec l’intégration, les listes de saisie semi-automatique s’affichent à un emplacement pratique en tant qu’utilisateurs manuscrits dans le panneau de saisie, ce qui améliore la vitesse et la facilité d’entrée de texte. dans les applications qui incluent une fonctionnalité de saisie semi-automatique basée sur la saisie semi-automatique du Shell ou la saisie semi-automatique .NET Framework 3,0, l’intégration de la saisie semi-automatique du panneau de saisie est une fonctionnalité gratuite et attrayante. En outre, un ensemble simple d’interfaces basées sur COM est fourni pour activer la même expérience intégrée pour les applications qui choisissent d’utiliser des contrôles de saisie semi-automatique personnalisés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 
