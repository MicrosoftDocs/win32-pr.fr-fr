---
description: La saisie semi-automatique développe des chaînes qui ont été entrées partiellement dans un contrôle d’édition dans des chaînes complètes.
title: Utilisation de la saisie semi-automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412596"
---
# <a name="using-autocomplete"></a>Utilisation de la saisie semi-automatique

La saisie semi-automatique développe des chaînes qui ont été entrées partiellement dans un [contrôle d’édition](/windows/desktop/Controls/edit-controls) dans des chaînes complètes. par exemple, lorsqu’un utilisateur commence à entrer une URL dans le contrôle d’édition d’adresse qui est incorporé dans la Windows barre d’outils Internet Explorer, la saisie semi-automatique développe la chaîne en une ou plusieurs options d’URL complètes qui sont cohérentes avec la chaîne partielle existante. Une chaîne d’URL partielle telle que « MIC » peut être développée en « https://www.microsoft.com » ou «» https://www.microsoft.com/windows . La saisie semi-automatique est généralement utilisée avec les contrôles d’édition ou avec les contrôles qui disposent d’un contrôle d’édition incorporé, tel que le contrôle [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .

## <a name="adding-autocomplete-functionality-to-your-application"></a>Ajout de la fonctionnalité de saisie semi-automatique à votre application

Une application peut ajouter la fonctionnalité de saisie semi-automatique à un contrôle d’édition de deux manières :

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) est une fonction simple qui peut remplir de façon automatique un chemin ou une URL de fichier.
-   L’interface [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) est exposée par l’objet de saisie semi-automatique (CLSID \_ automatique). Elle permet aux applications d’initialiser, d’activer et de désactiver l’objet. **IAutoComplete** offre davantage de contrôle sur les sources de saisie semi-automatique, y compris la possibilité d’ajouter une source personnalisée. Le reste de cette rubrique traite de l’utilisation de **IAutoComplete**. Consultez [Comment activer la saisie semi-automatique manuellement](how-to-enable-autocomplete-manually.md) pour obtenir des exemples d’utilisation spécifiques.

## <a name="autocomplete-modes"></a>Modes de saisie semi-automatique

Lorsque vous utilisez [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), la saisie semi-automatique peut afficher la chaîne terminée dans deux modes : ajout automatique et suggestion automatique. Les modes sont indépendants. vous pouvez activer l’un ou l’autre ou les deux. Pour spécifier le mode, appelez [**IAutoComplete2 :: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Ajout
</dt> <dd>

En mode d’ajout automatique, la saisie semi-automatique ajoute le reste de la chaîne candidate la plus probable aux caractères existants, en mettant en surbrillance les caractères ajoutés. Si l’utilisateur continue à entrer des caractères, ceux-ci sont ajoutés à la chaîne partielle existante. Si l’utilisateur ajoute un caractère identique au caractère suivant mis en surbrillance, la mise en surbrillance de ce caractère est désactivée. Les autres caractères seront toujours mis en surbrillance. Si l’utilisateur ajoute un caractère qui ne correspond pas au caractère suivant en surbrillance, la saisie semi-automatique tente de générer une nouvelle chaîne candidate basée sur la plus grande chaîne partielle et ajoute le reste de la nouvelle chaîne candidate à la chaîne partielle actuelle. Si aucune chaîne candidate n’est trouvée, seuls les caractères typés apparaissent et la zone d’édition se comporte comme elle le ferait sans la saisie semi-automatique. Ce processus se poursuit jusqu’à ce que l’utilisateur accepte une chaîne.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Suggestion automatique
</dt> <dd>

Dans le mode de suggestion automatique, la saisie semi-automatique affiche une liste déroulante, avec une ou plusieurs chaînes complètes suggérées, sous le contrôle d’édition. L’utilisateur peut sélectionner l’une des chaînes suggérées ou continuer à taper. Au fur et à mesure de la saisie, la liste déroulante peut être modifiée en fonction de la chaîne partielle actuelle. Si vous définissez l' \_ indicateur de recherche réglementaires dans [**IAutoComplete2 :: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), la saisie semi-automatique fournit une option, en bas de la liste déroulante, pour rechercher la chaîne partielle actuelle. Cette option s’affiche même s’il n’y a pas de chaînes suggérées. Si l’utilisateur sélectionne l’option de recherche, votre application doit lancer un moteur de recherche pour aider l’utilisateur.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Utilisation de sources de saisie semi-automatique prédéfinies

La saisie semi-automatique dépend d’une source qui lui fournit des chaînes à faire correspondre à la chaîne partielle de l’utilisateur. Vous avez la possibilité de fournir une source de saisie semi-automatique personnalisée, mais plusieurs des sources les plus courantes sont fournies par le système.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory
</dt> <dd>

Source de saisie semi-automatique qui correspond à la liste d’URL dans la liste historique de l’utilisateur.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

Source de saisie semi-automatique qui correspond à la liste d’URL dans la liste des derniers fichiers utilisés.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

Source de saisie semi-automatique qui correspond aux éléments de l’espace de noms de l’interpréteur de commandes : les fichiers sur l’ordinateur de l’utilisateur et les éléments dans les dossiers virtuels tels que le panneau de configuration.

</dd> </dl>

Dans certains cas, au lieu de libérer immédiatement les ressources, vous souhaiterez peut-être conserver les pointeurs d’interface vers les différents objets impliqués dans la saisie semi-automatique. En particulier, cette opération est effectuée lorsque vous souhaitez ajuster dynamiquement le comportement de la saisie semi-automatique. L’instance la plus courante de cela se produit lors de l’utilisation de l' \_ objet CLSID ACListISF, qui se termine à partir de l’espace de noms Shell et a l’option ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de l’énumération à partir du répertoire actif. Par exemple, lorsque vous accédez à un nouveau dossier, Internet Explorer modifie le répertoire actuel de la barre d’adresses et les paramètres doivent donc être modifiés dynamiquement. Il existe deux façons de spécifier le répertoire que l' \_ objet ACLISTISF CLSID doit traiter en tant que répertoire actif :

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) spécifie le répertoire via un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) spécifie le répertoire par le biais d’une chaîne de chemin.

Dans l’exemple suivant, supposons que **PAL** est un pointeur vers l’interface [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) d’un \_ objet CLSID ACListISF :

-   Utilisation de [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):

    Pour indiquer à l' \_ objet CLSID ACListISF qu’un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) particulier doit être traité comme le répertoire actif, vous pouvez utiliser l’interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) de l’objet. Étant donné qu’un **ITEMIDLIST** peut faire référence à un dossier virtuel, cette méthode est plus souple que l’utilisation de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Notez que les exemples suivants utilisent l’appel de procédure QueryInterface, qui permet une liste de paramètres simplifiée.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Utilisation de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Pour attribuer à l' \_ objet CLSID ACListISF un chemin d’accès en tant que répertoire actif, vous pouvez utiliser l’interface [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) de l’objet.

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
