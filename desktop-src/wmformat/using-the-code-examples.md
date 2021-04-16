---
title: Utilisation des exemples de code du kit de développement logiciel (SDK) Windows Media format
description: Utilisation des exemples de code du kit de développement logiciel (SDK) Windows Media format
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, exemples de code
- Windows Media Format SDK, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383784"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="62e6d-105">Utilisation des exemples de code du kit de développement logiciel (SDK) Windows Media format</span><span class="sxs-lookup"><span data-stu-id="62e6d-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="62e6d-106">La plupart des sections explicatives de ce kit de développement logiciel incluent des exemples de code.</span><span class="sxs-lookup"><span data-stu-id="62e6d-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="62e6d-107">Les exemples sont écrits pour être aussi clairs et concis que possible.</span><span class="sxs-lookup"><span data-stu-id="62e6d-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="62e6d-108">Lors de la lecture des exemples, vous devez être conscient des conventions suivantes.</span><span class="sxs-lookup"><span data-stu-id="62e6d-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="62e6d-109">Tous les exemples sont supposés inclure Windows. h et WMSDK. h.</span><span class="sxs-lookup"><span data-stu-id="62e6d-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="62e6d-110">Tout autre fichier d’en-tête requis est mentionné dans le texte explicatif.</span><span class="sxs-lookup"><span data-stu-id="62e6d-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="62e6d-111">La vérification des erreurs a été limitée à la séparation de la fonction si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="62e6d-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="62e6d-112">Dans une application, vous devez vérifier les codes d’erreur spécifiques et fournir un type de rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="62e6d-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="62e6d-113">Lors de la vérification des valeurs de retour des méthodes ou des fonctions qui retournent une valeur **HRESULT** , vous devez utiliser la macro **failed** pour déterminer si la valeur de retour indique un échec.</span><span class="sxs-lookup"><span data-stu-id="62e6d-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="62e6d-114">La plupart des exemples de cette documentation utilisent une macro nommée GOTO \_ Exit \_ si \_ failed, qui est défini dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="62e6d-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="62e6d-115">Ces exemples de fonctions ont chacun une balise nommée « Exit : », après quoi toutes les interfaces et la mémoire allouées dans la fonction sont libérées et le code d’erreur, le cas échéant, est retourné.</span><span class="sxs-lookup"><span data-stu-id="62e6d-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="62e6d-116">Les interfaces et la mémoire sont libérées dans les exemples de code à l’aide de macros nommées libération SÉCURISÉe \_ et \_ Suppression de tableau sécurisé \_ .</span><span class="sxs-lookup"><span data-stu-id="62e6d-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="62e6d-117">Ces macros sont définies dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="62e6d-117">These macros are defined in the following code:</span></span>
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

    

-   <span data-ttu-id="62e6d-118">Souvent, vous devrez inclure la logique d’un exemple dans un autre exemple pour que l’exemple soit significatif.</span><span class="sxs-lookup"><span data-stu-id="62e6d-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="62e6d-119">Dans ces instances, un commentaire TODO est inclus, avec une référence à l’exemple de code approprié.</span><span class="sxs-lookup"><span data-stu-id="62e6d-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="62e6d-120">Pour faciliter la lecture du code, aucune des fonctions d’exemple de cette documentation ne valident leurs paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="62e6d-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="62e6d-121">Si vous copiez l’une de ces fonctions dans votre code, vous devez valider tous les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="62e6d-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62e6d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62e6d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62e6d-123">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="62e6d-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




