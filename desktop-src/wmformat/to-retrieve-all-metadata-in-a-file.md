---
title: Pour récupérer toutes les métadonnées dans un fichier
description: Pour récupérer toutes les métadonnées dans un fichier
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows Media Format SDK, récupération des métadonnées
- ASF (Advanced Systems Format), récupération des métadonnées
- ASF (format des systèmes avancés), récupération des métadonnées
- métadonnées, récupérer tout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc5d63a27cd4455d8d39cebee894dfbfc8d5bf2c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511875"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>Pour récupérer toutes les métadonnées dans un fichier

L’exemple de code suivant est une fonction qui affiche toutes les métadonnées dans un fichier. Pour pouvoir utiliser la fonction, vous devez lui passer un pointeur vers l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) d’un objet d’éditeur de métadonnées, d’un objet lecteur, d’un objet lecteur synchrone ou d’un objet Writer. Vous devez également inclure le fichier d’en-tête stdio. h quelque part dans votre projet. Pour plus d’informations sur l’utilisation de cet exemple, consultez [utilisation des exemples de code](using-the-code-examples.md).

Par souci de clarté, cet exemple n’affiche pas les valeurs des attributs binary et GUID. Pour les attributs binaires, vous devez vérifier si le nom d’attribut correspond à l’un des attributs de métadonnées complexes connus. Si c’est le cas, vous devez mettre en forme la sortie en fonction de la structure utilisée pour cet attribut. De même, les valeurs d’attribut GUID peuvent être affichées de plusieurs façons. Vous pouvez choisir d’afficher un à la fois chaque membre de la structure ou de convertir la structure en une chaîne et de l’afficher comme une seule valeur.


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Récupération des attributs de métadonnées**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




