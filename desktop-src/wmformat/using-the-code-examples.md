---
title: utilisation des exemples de Code du kit de développement logiciel (SDK) Windows Media Format
description: utilisation des exemples de Code du kit de développement logiciel (SDK) Windows Media Format
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, exemples de code
- Windows Media Format SDK, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a5b6718bf7665d04fedb5d5a0bad473a632cbeeabdfd756a52877ccdc84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963938"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>utilisation des exemples de Code du kit de développement logiciel (SDK) Windows Media Format

La plupart des sections explicatives de ce kit de développement logiciel incluent des exemples de code. Les exemples sont écrits pour être aussi clairs et concis que possible. Lors de la lecture des exemples, vous devez être conscient des conventions suivantes.

-   Tous les exemples sont supposés inclure Windows. h et WMSDK. h. Tout autre fichier d’en-tête requis est mentionné dans le texte explicatif.
-   La vérification des erreurs a été limitée à la séparation de la fonction si une erreur se produit. Dans une application, vous devez vérifier les codes d’erreur spécifiques et fournir un type de rapport d’erreurs.

    Lors de la vérification des valeurs de retour des méthodes ou des fonctions qui retournent une valeur **HRESULT** , vous devez utiliser la macro **failed** pour déterminer si la valeur de retour indique un échec.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    La plupart des exemples de cette documentation utilisent une macro nommée GOTO \_ Exit \_ si \_ failed, qui est défini dans le code suivant.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Ces exemples de fonctions ont chacun une balise nommée « Exit : », après quoi toutes les interfaces et la mémoire allouées dans la fonction sont libérées et le code d’erreur, le cas échéant, est retourné.

-   Les interfaces et la mémoire sont libérées dans les exemples de code à l’aide de macros nommées libération SÉCURISÉe \_ et \_ Suppression de tableau sécurisé \_ . Ces macros sont définies dans le code suivant :
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   Souvent, vous devrez inclure la logique d’un exemple dans un autre exemple pour que l’exemple soit significatif. Dans ces instances, un commentaire TODO est inclus, avec une référence à l’exemple de code approprié.
-   Pour faciliter la lecture du code, aucune des fonctions d’exemple de cette documentation ne valident leurs paramètres d’entrée. Si vous copiez l’une de ces fonctions dans votre code, vous devez valider tous les paramètres d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

 




