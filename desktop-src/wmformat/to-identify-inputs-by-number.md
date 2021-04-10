---
title: Pour identifier les entrées par nombre
description: Pour identifier les entrées par nombre
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- ASF (Advanced Systems Format), identification des entrées par numéro
- ASF (format avancé des systèmes), identification des entrées par numéro
- profils, identification des entrées par numéro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030793"
---
# <a name="to-identify-inputs-by-number"></a>Pour identifier les entrées par nombre

Chaque exemple que vous transmettez à l’enregistreur doit être associé à un numéro d’entrée. Chaque numéro d’entrée correspond à un ou plusieurs flux du profil utilisé par le writer pour écrire le fichier. Dans un profil, les sources de média sont identifiées par un nom de connexion. Le writer associe un numéro d’entrée à chaque nom de connexion lorsque vous définissez le profil pour le writer. Avant de pouvoir passer des exemples au writer, vous devez déterminer quelles sont les données attendues par chaque entrée. Vous ne pouvez pas supposer que les entrées seront dans le même ordre que les flux dans un profil, même si c’est souvent le cas. Par conséquent, la seule façon fiable de faire correspondre les entrées aux flux consiste à comparer le nom de connexion de l’entrée avec le nom de connexion du flux.

Pour identifier les noms de connexion et les numéros d’entrée correspondants pour un profil chargé, procédez comme suit :

1.  Créez un objet Writer et définissez un profil à utiliser. Pour plus d’informations sur la définition des profils dans le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md). Vous devez connaître les noms de connexion utilisés pour les flux dans le profil. Vous pouvez obtenir le nom de la connexion dans le profil en obtenant l’objet de configuration Stream pour chaque flux et en appelant [**IWMStreamConfig :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Pour plus d’informations sur les profils et les objets de configuration de flux, consultez [utilisation des profils](working-with-profiles.md).
2.  Récupérez le nombre total d’entrées en appelant [**IWMWriter :: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Parcourez toutes les entrées, en procédant comme suit pour chacun d’entre eux.
    -   Récupérez l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour l’entrée en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Récupérez le nom de la connexion qui correspond au numéro d’entrée en appelant [**IWMInputMediaProps :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). Une fois que vous avez le nom de la connexion, vous connaissez les flux associés aux numéros d’entrée affectés par le writer.

L’exemple de code suivant affiche le nom de la connexion pour chaque entrée. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




