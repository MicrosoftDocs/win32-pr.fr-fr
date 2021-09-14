---
title: gestion des erreurs dans COM (Prise en main avec Win32 et C++)
description: gestion des erreurs dans COM (Prise en main avec Win32 et C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094390"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>gestion des erreurs dans COM (Prise en main avec Win32 et C++)

COM utilise des valeurs **HRESULT** pour indiquer la réussite ou l’échec d’un appel de méthode ou de fonction. Divers en-têtes du kit de développement logiciel (SDK) définissent différentes constantes **HRESULT** . Un ensemble commun de codes à l’ensemble du système est défini dans WinError. h. Le tableau suivant présente certains de ces codes de retour à l’ensemble du système.



| Constante            | Valeur numérique | Description                                          |
|---------------------|---------------|------------------------------------------------------|
| **\_ACCESSDENIED E** | 0x80070005    | Accès refusé.                                       |
| **E \_ échec**         | 0x80004005    | Erreur non spécifiée.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Valeur de paramètre non valide.                             |
| **\_OUTOFMEMORY E**  | 0x8007000E    | Mémoire insuffisante.                                       |
| **\_pointeur E**      | 0x80004003    | La valeur **null** a été transmise de manière incorrecte pour une valeur de pointeur. |
| **E \_ inattendu**   | 0x8000FFFF    | Condition inattendue.                                |
| **\_OK**           | 0x0           | Réussite.                                             |
| **S \_ false**        | 0x1           | Réussite.                                             |



 

Toutes les constantes avec le préfixe « E \_ » sont des codes d’erreur. Les constantes **s \_ OK** et **s \_ false** sont les deux codes de réussite. Il se peut que 99% des méthodes COM retournent **S \_ OK** quand elles ont été correctement exécutées, mais n’autorisent pas ce fait à vous tromper. Une méthode peut retourner d’autres codes de réussite, donc toujours tester les erreurs à l’aide de la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) ou [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . L’exemple de code suivant montre une méthode incorrecte et la bonne façon de tester la réussite d’un appel de fonction.


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



Le code de réussite **S \_ false** mérite de mentionner. Certaines méthodes utilisent **S \_ false** pour signifier, à peu près, une condition négative qui n’est pas un échec. Il peut également indiquer un « no-op », la méthode a réussi, mais n’a aucun effet. Par exemple, la fonction [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) retourne **S \_ false** si vous l’appelez une deuxième fois à partir du même thread. Si vous avez besoin de faire la distinction entre **s \_ OK** et **s \_ false** dans votre code, vous devez tester la valeur directement, mais utilisez toujours l' [**échec**](/windows/desktop/api/winerror/nf-winerror-failed) ou le [**succès**](/windows/desktop/api/winerror/nf-winerror-succeeded) pour gérer les cas restants, comme illustré dans l’exemple de code suivant.


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



Certaines valeurs **HRESULT** sont spécifiques à une fonctionnalité particulière ou à un sous-système de Windows. Par exemple, l’API graphique Direct2D définit le code d’erreur **D2DERR \_ \_ \_ format de pixel non pris en charge**, ce qui signifie que le programme a utilisé un format de pixel non pris en charge. La documentation MSDN fournit souvent une liste de codes d’erreur spécifiques qu’une méthode peut retourner. Toutefois, vous ne devez pas considérer que ces listes sont définitives. Une méthode peut toujours retourner une valeur **HRESULT** qui n’est pas indiquée dans la documentation. Là encore, utilisez les macros ayant [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) et [**échoué**](/windows/desktop/api/winerror/nf-winerror-failed) . Si vous testez un code d’erreur spécifique, incluez également un cas par défaut.


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>Modèles pour la gestion des erreurs

Cette section présente certains modèles pour la gestion structurée des erreurs COM. Chaque modèle présente des avantages et des inconvénients. Dans une certaine mesure, le choix est une question de saveur. Si vous travaillez sur un projet existant, il a peut-être déjà des instructions de codage qui découpent un style particulier. Quel que soit le modèle que vous adoptez, le code fiable obéit aux règles suivantes.

-   Pour chaque méthode ou fonction qui retourne un **HRESULT**, vérifiez la valeur de retour avant de continuer.
-   Libérer des ressources une fois qu’elles sont utilisées.
-   N’essayez pas d’accéder à des ressources non valides ou non initialisées, telles que des pointeurs **null** .
-   N’essayez pas d’utiliser une ressource après l’avoir libérée.

Avec ces règles à l’esprit, Voici quatre modèles pour la gestion des erreurs.

-   [IFS imbriqué](#nested-ifs)
-   [IFS en cascade](#cascading-ifs)
-   [Sauter en cas d’échec](#jump-on-fail)
-   [Lever en cas d’échec](#throw-on-fail)

### <a name="nested-ifs"></a>IFS imbriqué

Après chaque appel qui retourne un **HRESULT**, utilisez une instruction **If** pour tester la réussite. Ensuite, placez l’appel de méthode suivant dans la portée de l’instruction **If** . Plus d’instructions **If** peuvent être imbriquées aussi profondément que nécessaire. Les exemples de code précédents de ce module ont tous utilisé ce modèle, mais ici encore :


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



Avantages

-   Les variables peuvent être déclarées avec une étendue minimale. Par exemple, *pItem* n’est pas déclaré tant qu’il n’est pas utilisé.
-   Dans chaque instruction **If** , certains invariants sont vrais : tous les appels précédents ont réussi et toutes les ressources acquises sont toujours valides. Dans l’exemple précédent, lorsque le programme atteint l’instruction **If** la plus profonde, *pItem* et *pFileOpen* sont reconnus comme étant valides.
-   Il est clair quand il faut libérer des pointeurs d’interface et d’autres ressources. Vous publiez une ressource à la fin de l’instruction **If** qui suit immédiatement l’appel qui a acquis la ressource.

Inconvénients

-   Certaines personnes recherchent une imbrication profonde difficile à lire.
-   La gestion des erreurs est mélangée à d’autres instructions de création de branche et de bouclage. Cela peut rendre la logique de programme globale plus difficile à suivre.

### <a name="cascading-ifs"></a>IFS en cascade

Après chaque appel de méthode, utilisez une instruction **If** pour tester la réussite. Si la méthode est réussie, placez l’appel de méthode suivant à l’intérieur du bloc **If** . Mais au lieu d’imbriquer d’autres instructions **If** , placez chaque test [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) suivant après le bloc **If** précédent. Si une méthode échoue, tous les tests **réussis** restants échouent uniquement jusqu’à ce que le bas de la fonction soit atteint.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Dans ce modèle, vous libérez des ressources à la fin de la fonction. Si une erreur se produit, certains pointeurs peuvent être non valides lorsque la fonction se termine. L’appel de [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur un pointeur non valide entraîne un blocage du programme (ou pire). vous devez donc initialiser tous les pointeurs vers la **valeur null** et vérifier s’ils ont la **valeur null** avant de les libérer. Cet exemple utilise la `SafeRelease` fonction ; les pointeurs intelligents sont également un bon choix.

Si vous utilisez ce modèle, vous devez faire attention aux constructions de boucle. À l’intérieur d’une boucle, arrêter à partir de la boucle en cas d’échec d’un appel.

Avantages

-   Ce modèle crée moins d’imbrication que le modèle « IFS imbriqué ».
-   Le workflow de contrôle global est plus facile à voir.
-   Les ressources sont libérées à un seul point du code.

Inconvénients

-   Toutes les variables doivent être déclarées et initialisées en haut de la fonction.
-   Si un appel échoue, la fonction effectue plusieurs vérifications d’erreurs inutiles au lieu de quitter la fonction immédiatement.
-   Étant donné que le déroulement du contrôle continue via la fonction après une défaillance, vous devez faire attention dans le corps de la fonction et non pas pour accéder aux ressources non valides.
-   Les erreurs à l’intérieur d’une boucle requièrent un cas particulier.

### <a name="jump-on-fail"></a>Sauter en cas d’échec

Après chaque appel de méthode, tester l’échec (pas de succès). En cas d’échec, accédez à une étiquette près du bas de la fonction. Après l’étiquette, mais avant de quitter la fonction, libérez des ressources.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Avantages

-   Le workflow de contrôle global est facile à voir.
-   À chaque point du code après un [**échec**](/windows/desktop/api/winerror/nf-winerror-failed) de vérification, si vous n’avez pas sauté l’étiquette, il est garanti que tous les appels précédents ont réussi.
-   Les ressources sont libérées à un seul emplacement dans le code.

Inconvénients

-   Toutes les variables doivent être déclarées et initialisées en haut de la fonction.
-   Certains programmeurs n’aiment pas utiliser **goto** dans leur code. (Toutefois, il convient de noter que cette utilisation de **goto** est très structurée ; le code ne passe jamais en dehors de l’appel de fonction actuel.)
-   les instructions **goto** ignorent les initialiseurs.

### <a name="throw-on-fail"></a>Lever en cas d’échec

Au lieu d’accéder à une étiquette, vous pouvez lever une exception en cas d’échec d’une méthode. Cela peut générer un style plus idiomatique C++ si vous êtes utilisé pour écrire du code sécurisé à l’exception.


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



Notez que cet exemple utilise la classe **CComPtr** pour gérer les pointeurs d’interface. En général, si votre code lève des exceptions, vous devez suivre le modèle RAII (Resource Acquisition Is Initialization). Autrement dit, chaque ressource doit être gérée par un objet dont le destructeur garantit que la ressource est libérée correctement. Si une exception est levée, il est garanti que le destructeur est appelé. Dans le cas contraire, votre programme peut provoquer des fuites de ressources.

Avantages

-   Compatible avec le code existant qui utilise la gestion des exceptions.
-   Compatible avec les bibliothèques C++ qui lèvent des exceptions, telles que la bibliothèque STL (Standard Template Library).

Inconvénients

-   Requiert des objets C++ pour gérer des ressources telles que la mémoire ou les handles de fichiers.
-   Nécessite une bonne compréhension de la manière d’écrire du code sécurisé contre les exceptions.

## <a name="next"></a>Suivant

[Module 3. Windows Graphismes](module-3---windows-graphics.md)

 

 
