---
title: utilisation des exemples de Code du Client Microsoft Windows Media DRM
description: utilisation des exemples de Code du Client Microsoft Windows Media DRM
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, exemples de code
- Windows Media Format SDK, exemple de code
- Windows Media Format SDK, exemples de code DRM
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704212"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>utilisation des exemples de Code du Client Microsoft Windows Media DRM

Des exemples de code sont inclus dans cette documentation pour illustrer l’utilisation des composants. Les exemples sont écrits pour être aussi clairs et concis que possible. Lors de la lecture des exemples, vous devez être conscient des conventions suivantes.

-   Tous les exemples sont supposés inclure Windows. h et wmdrmsdk. h. L’exemple inclut une note s’il requiert d’autres en-têtes pour la compilation.
-   La vérification des erreurs a été limitée à la séparation de la fonction si une erreur se produit. Dans une application, vous devez vérifier les codes d’erreur spécifiques et fournir un type de rapport d’erreurs.
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

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](drm-getting-started.md)
</dt> </dl>

 

 




