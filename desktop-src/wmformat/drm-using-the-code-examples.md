---
title: Utilisation des exemples de code du client Microsoft Windows Media DRM
description: Utilisation des exemples de code du client Microsoft Windows Media DRM
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, exemples de code
- Windows Media Format SDK, exemple de code
- Kit de développement logiciel (SDK) Windows Media format, exemples de code DRM
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383544"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>Utilisation des exemples de code du client Microsoft Windows Media DRM

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

 

 




