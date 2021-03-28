---
description: Pour obtenir un contrôle plus détaillé sur le comportement de la saisie semi-automatique, ou pour ajouter une source personnalisée de chaînes de saisie semi-automatique, vous devez gérer vous-même l’objet de saisie semi-automatique.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Procédure d’activation manuelle de la saisie semi-automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973158"
---
# <a name="how-to-enable-autocomplete-manually"></a>Procédure d’activation manuelle de la saisie semi-automatique

Pour obtenir un contrôle plus détaillé sur le comportement de la saisie semi-automatique, ou pour ajouter une source personnalisée de chaînes de saisie semi-automatique, vous devez gérer vous-même l’objet de saisie semi-automatique. Vous pouvez activer la saisie semi-automatique manuellement de l’une des manières suivantes.

## <a name="instructions"></a>Instructions

### <a name="creating-a-simple-autocomplete-object"></a>Création d’un objet de saisie semi-automatique simple

Les étapes suivantes montrent comment créer et initialiser un objet de saisie semi-automatique simple. Un objet de saisie semi-automatique simple effectue des chaînes à partir d’une source unique. La vérification des erreurs a été intentionnellement omise dans cet exemple.

1.  Créez l’objet de saisie semi-automatique.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Créez la source de saisie semi-automatique. Vous pouvez utiliser une [source de saisie semi-automatique prédéfinie](ac-ovw.md) ou vous pouvez écrire votre propre source personnalisée.

    Le code suivant utilise l’une des sources de saisie semi-automatique prédéfinies.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    Le code suivant utilise une source de saisie semi-automatique personnalisée. Vous pouvez écrire votre propre source de saisie semi-automatique en implémentant un objet qui expose l’interface [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) . L’objet peut également implémenter les interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) et [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Définissez les options sur la source de saisie semi-automatique (facultatif).

    Vous pouvez personnaliser le comportement de la source de saisie semi-automatique en définissant ses options si la source expose l’interface [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) . Lorsque vous utilisez les sources de saisie semi-automatique prédéfinies, seul CLSID \_ ACListISF exporte **IACList2**. Pour obtenir la liste complète des options et leurs valeurs, consultez [**IACList2 :: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Initialise l’objet de saisie semi-automatique.

    Dans cet exemple, **hwndEdit** est le handle de la fenêtre de contrôle d’édition pour laquelle la saisie semi-automatique doit être activée. Consultez [**IAutoComplete :: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) pour obtenir une description des deux derniers paramètres inutilisés.

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Définissez les options de l’objet de saisie semi-automatique (facultatif).

    Vous pouvez personnaliser le comportement de l’objet de saisie semi-automatique en définissant ses options. Pour obtenir la liste complète des options et leurs valeurs, consultez la documentation de [**IACList2 :: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Libère les objets.

    > [!Note]  
    > L’objet de saisie semi-automatique reste attaché au contrôle d’édition même après sa publication. Si vous prévoyez d’avoir accès à ces objets ultérieurement, si vous souhaitez modifier les options de saisie semi-automatique ultérieurement, par exemple, il n’est pas nécessaire de les libérer à ce stade.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Création d’un objet de saisie semi-automatique composée

Un objet de saisie semi-automatique composée correspond aux chaînes de plusieurs sources. Par exemple, la barre d’adresses Windows Internet Explorer utilise un objet de saisie semi-automatique composée, car l’utilisateur peut commencer à taper le nom d’un fichier ou d’une URL. La plupart des étapes impliquées dans la création d’un objet de saisie semi-automatique composée sont identiques à celles décrites dans la section « création d’un objet à saisie semi-automatique simple ». Ces étapes sont indiquées comme telles.

1.  Créez l’objet de saisie semi-automatique. Il s’agit du même que celui de l’étape 1 ci-dessus.

2.  Créez le gestionnaire d’objets de source composée automatique.

    L’objet source composée automatique permet de combiner plusieurs sources de saisie semi-automatique en une seule source de saisie semi-automatique.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Créez et définissez des options pour chacune des sources de saisie semi-automatique. Répétez les étapes 2 et 3 ci-dessus pour chaque source.

4.  Attachez chaque source de saisie semi-automatique au gestionnaire d’objets source.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Initialise l’objet de saisie semi-automatique.

    Il s’agit du même que celui de l’étape 4 ci-dessus, mais au lieu de passer la source de saisie semi-automatique simple à [**IAutoComplete :: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), vous transmettez le gestionnaire d’objets source composite.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Définissez les options de l’objet de saisie semi-automatique. Il s’agit du même que celui de l’étape 5 ci-dessus.

7.  Libère les objets.

    Comme dans le cas simple, vous pouvez libérer les objets dès que vous avez terminé de les utiliser, mais vous pouvez également les conserver pour modifier les options ultérieurement.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
