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
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="e1003-110">Utilisation des exemples de code du client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="e1003-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="e1003-111">Des exemples de code sont inclus dans cette documentation pour illustrer l’utilisation des composants.</span><span class="sxs-lookup"><span data-stu-id="e1003-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="e1003-112">Les exemples sont écrits pour être aussi clairs et concis que possible.</span><span class="sxs-lookup"><span data-stu-id="e1003-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="e1003-113">Lors de la lecture des exemples, vous devez être conscient des conventions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1003-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="e1003-114">Tous les exemples sont supposés inclure Windows. h et wmdrmsdk. h.</span><span class="sxs-lookup"><span data-stu-id="e1003-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="e1003-115">L’exemple inclut une note s’il requiert d’autres en-têtes pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="e1003-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="e1003-116">La vérification des erreurs a été limitée à la séparation de la fonction si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e1003-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="e1003-117">Dans une application, vous devez vérifier les codes d’erreur spécifiques et fournir un type de rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e1003-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="e1003-118">Les interfaces et la mémoire sont libérées dans les exemples de code à l’aide de macros nommées libération SÉCURISÉe \_ et \_ Suppression de tableau sécurisé \_ .</span><span class="sxs-lookup"><span data-stu-id="e1003-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="e1003-119">Ces macros sont définies dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e1003-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="e1003-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1003-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1003-121">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="e1003-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




