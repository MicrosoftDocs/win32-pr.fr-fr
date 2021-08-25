---
title: Pratiques de codage COM
description: Cette rubrique décrit comment rendre votre code COM plus efficace et plus robuste.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93febc4ee3dfd4f05f20fae8078bc2a5ebb7f9623a860f49ec9cd6ce4e69b95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913888"
---
# <a name="com-coding-practices"></a>Pratiques de codage COM

Cette rubrique décrit comment rendre votre code COM plus efficace et plus robuste.

-   [\_ \_ Opérateur uuidof](/windows)
-   [La \_ macro IID PPV \_ args](/windows)
-   [Modèle SafeRelease](#the-saferelease-pattern)
-   [Pointeurs intelligents COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>\_ \_ Opérateur uuidof

Lorsque vous générez votre programme, vous pouvez recevoir des erreurs de l’éditeur de liens semblables à ce qui suit :

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Cette erreur signifie qu’une constante GUID a été déclarée avec une liaison externe (**extern**) et que l’éditeur de liens n’a pas pu trouver la définition de la constante. La valeur d’une constante GUID est généralement exportée à partir d’un fichier de bibliothèque statique. si vous utilisez Microsoft Visual C++, vous pouvez éviter d’avoir à lier une bibliothèque statique à l’aide de l’opérateur **\_ \_ uuidof** . Cet opérateur est une extension de langage Microsoft. Elle retourne une valeur GUID à partir d’une expression. L’expression peut être un nom de type interface, un nom de classe ou un pointeur d’interface. À l’aide de **\_ \_ uuidof**, vous pouvez créer l’objet de boîte de dialogue d’élément commun comme suit :


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Le compilateur extrait la valeur GUID de l’en-tête, aucune exportation de bibliothèque n’est donc nécessaire.

> [!Note]  
> La valeur GUID est associée au nom de type en déclarant `__declspec(uuid( ... ))` dans l’en-tête. Pour plus d’informations, consultez la documentation relative à **\_ \_ declspec** dans la documentation Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>La \_ macro IID PPV \_ args

Nous avons vu que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) requièrent la conversion du paramètre final en **type \* \* void** . Cela crée le risque d’incompatibilité de type. Prenons le fragment de code suivant :


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Ce code demande l’interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , mais passe un pointeur [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . L’expression de **\_ cast de réinterprétation** contourne le système de type C++, de sorte que le compilateur n’intercepte pas cette erreur. Dans le meilleur des cas, si l’objet n’implémente pas l’interface demandée, l’appel échoue simplement. Dans le pire des cas, la fonction s’exécute correctement et vous avez un pointeur incompatible. En d’autres termes, le type pointeur ne correspond pas à la vtable réelle en mémoire. Comme vous pouvez l’imaginer, rien ne peut arriver à ce stade.

> [!Note]  
> Une table de méthodes virtuelles ( *vtable* ) est une table de pointeurs de fonction. La vtable est la manière dont COM lie un appel de méthode à son implémentation au moment de l’exécution. Par contre, les vtables sont la manière dont la plupart des compilateurs C++ implémentent des méthodes virtuelles.

 

La macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) permet d’éviter cette classe d’erreur. Pour utiliser cette macro, remplacez le code suivant :


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



par le code :


```C++
IID_PPV_ARGS(&pFileOpen)
```



La macro insère automatiquement `__uuidof(IFileOpenDialog)` pour l’identificateur d’interface. il est donc garanti qu’elle correspond au type de pointeur. Voici le code modifié (et correct) :


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Vous pouvez utiliser la même macro avec [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>Modèle SafeRelease

Le décompte de références est l’un des éléments de la programmation qui est fondamentalement facile, mais qui est également fastidieux, ce qui facilite le problème. Les erreurs sont généralement les suivantes :

-   Échec de la libération d’un pointeur d’interface lorsque vous avez fini de l’utiliser. Cette classe de bogue entraîne une fuite de mémoire et d’autres ressources par votre programme, car les objets ne sont pas détruits.
-   Appel de la [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) avec un pointeur non valide. Par exemple, cette erreur peut se produire si l’objet n’a jamais été créé. Cette catégorie de bogue entraîne probablement un blocage de votre programme.
-   Déréférencement d’un pointeur d’interface après l’appel de [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . Ce bogue peut provoquer le blocage de votre programme. Pire encore, cela peut entraîner un blocage aléatoire de votre programme, ce qui rend difficile le suivi de l’erreur d’origine.

Une façon d’éviter ces bogues consiste à appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) via une fonction qui libère le pointeur en toute sécurité. Le code suivant illustre une fonction qui effectue cette opérations :


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Cette fonction prend un pointeur d’interface COM en tant que paramètre et effectue les opérations suivantes :

1.  Vérifie si le pointeur a la **valeur null**.
2.  Appelle la [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) si le pointeur n’est pas **null**.
3.  Définit le pointeur sur la **valeur null**.

Voici un exemple d’utilisation de `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Si [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) s’exécute correctement, l’appel à `SafeRelease` libère le pointeur. Si **CoCreateInstance** échoue, *PFileOpen* conserve la **valeur null**. La `SafeRelease` fonction vérifie cela et ignore l’appel à [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

Il est également possible d’appeler `SafeRelease` plusieurs fois sur le même pointeur, comme illustré ici :


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Pointeurs intelligents COM

La `SafeRelease` fonction est utile, mais elle vous oblige à vous souvenir de deux choses :

-   Initialise chaque pointeur d’interface avec la **valeur null**.
-   Appelez `SafeRelease` avant que chaque pointeur soit hors de portée.

En tant que programmeur C++, vous pensez probablement que vous ne devriez pas avoir à vous souvenir de l’un de ces éléments. Après tout, c’est pourquoi C++ a des constructeurs et des destructeurs. Il serait intéressant d’avoir une classe qui encapsule le pointeur d’interface sous-jacent et initialise et libère automatiquement le pointeur. En d’autres termes, nous souhaitons obtenir ce qui suit :


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



La définition de classe présentée ici est incomplète et n’est pas utilisable comme indiqué. Au minimum, vous devez définir un constructeur de copie, un opérateur d’assignation et un moyen d’accéder au pointeur COM sous-jacent. heureusement, vous n’avez pas besoin d’effectuer ce travail, car Microsoft Visual Studio fournit déjà une classe de pointeur intelligent dans le cadre de la Active Template Library (ATL).

La classe de pointeur intelligent ATL est nommée **CComPtr**. (Il existe également une classe **CComQIPtr** , qui n’est pas abordée ici.) Voici l’exemple de [boîte de dialogue Ouvrir](example--the-open-dialog-box.md) réécrit pour utiliser **CComPtr**.


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



La principale différence entre ce code et l’exemple d’origine est que cette version n’appelle pas explicitement [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Lorsque l’instance **CComPtr** est hors de portée, le destructeur appelle **Release** sur le pointeur sous-jacent.

**CComPtr** est un modèle de classe. L’argument template est le type d’interface COM. En interne, **CComPtr** contient un pointeur de ce type. **CComPtr** remplace **Operator-> ()** et **Operator& ()** afin que la classe agisse comme le pointeur sous-jacent. Par exemple, le code suivant est équivalent à l’appel direct de la méthode **IFileOpenDialog :: Show** :


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** définit également une méthode **CComPtr :: CoCreateInstance** , qui appelle la fonction com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec des valeurs de paramètre par défaut. Le seul paramètre obligatoire est l’identificateur de classe, comme le montre l’exemple suivant :


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



La méthode **CComPtr :: CoCreateInstance** est fournie à titre purement pratique ; vous pouvez toujours appeler la fonction COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , si vous préférez.

## <a name="next"></a>Suivant

[Gestion des erreurs dans COM](error-handling-in-com.md)

 

 