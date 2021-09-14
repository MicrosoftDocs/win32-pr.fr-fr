---
title: Gestion de la durée de vie d’un objet
description: Découvrez comment gérer les méthodes AddRef et Release pour contrôler la durée de vie d’un objet.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094358"
---
# <a name="managing-the-lifetime-of-an-object"></a>Gestion de la durée de vie d’un objet

Il existe une règle pour les interfaces COM que nous n’avons pas encore mentionnées. Chaque interface COM doit hériter, directement ou indirectement, d’une interface nommée [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Cette interface fournit des fonctionnalités de base que tous les objets COM doivent prendre en charge.

L’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) définit trois méthodes :

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Version release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

La méthode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permet à un programme d’interroger les fonctionnalités de l’objet au moment de l’exécution. Pour plus d’informations à ce sujet, nous allons [demander un objet pour une interface](asking-an-object-for-an-interface.md). Les méthodes [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sont utilisées pour contrôler la durée de vie d’un objet. Il s’agit de l’objet de cette rubrique.

## <a name="reference-counting"></a>Décompte de références

À un moment donné, un programme peut allouer et libérer des ressources. L’allocation d’une ressource est simple. Il est difficile de savoir quand libérer la ressource, surtout si la durée de vie de la ressource s’étend au-delà de la portée actuelle. Ce problème n’est pas propre à COM. Tout programme qui alloue de la mémoire du tas doit résoudre le même problème. Par exemple, C++ utilise des destructeurs automatiques, tandis que C# et Java utilisent garbage collection. COM utilise une approche appelée *décompte de références*.

Chaque objet COM gère un nombre interne. C’est ce que l’on appelle le décompte de références. Le nombre de références effectue le suivi du nombre de références à l’objet actuellement actives. Lorsque le nombre de références chute à zéro, l’objet se supprime lui-même. La dernière partie est la plus intéressante : l’objet se supprime lui-même. Le programme ne supprime jamais l’objet de manière explicite.

Voici les règles pour le décompte de références :

-   Lorsque l’objet est créé pour la première fois, son nombre de références est 1. À ce stade, le programme a un seul pointeur vers l’objet.
-   Le programme peut créer une nouvelle référence en dupliquant (copiant) le pointeur. Lorsque vous copiez le pointeur, vous devez appeler la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) de l’objet. Cette méthode incrémente le nombre de références d’une unité.
-   Lorsque vous avez terminé d’utiliser un pointeur vers l’objet, vous devez appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). La méthode **Release** décrémente le nombre de références d’une unité. Il invalide également le pointeur. N’utilisez pas le pointeur une fois que vous avez appelé **Release**. (Si vous avez d’autres pointeurs vers le même objet, vous pouvez continuer à utiliser ces pointeurs.)
-   Quand vous avez appelé [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) avec chaque pointeur, le nombre de références d’objet de l’objet atteint zéro, et l’objet se supprime lui-même.

Le diagramme suivant illustre un cas simple mais classique.

![Diagramme qui montre un cas simple de décompte de références.](images/com04.png)

Le programme crée un objet et stocke un pointeur (*p*) sur l’objet. À ce stade, le nombre de références est 1. Quand le programme a fini d’utiliser le pointeur, il appelle [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Le décompte de références est décrémenté à zéro et l’objet se supprime lui-même. Désormais, *p* n’est pas valide. L’utilisation de *p* pour d’autres appels de méthode est une erreur.

Le diagramme suivant montre un exemple plus complexe.

![illustration illustrant le décompte de références](images/com05.png)

Ici, le programme crée un objet et stocke le pointeur *p*, comme précédemment. Ensuite, le programme copie *p* vers une nouvelle variable, *q*. À ce stade, le programme doit appeler [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour incrémenter le décompte de références. Le décompte de références est maintenant 2 et il existe deux pointeurs valides pour l’objet. Supposons maintenant que le programme a fini d’utiliser *p*. Le programme appelle [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), le décompte de références atteint 1 et *p* n’est plus valide. Toutefois, *q* est toujours valide. Plus tard, le programme se termine à l’aide de *q*. Par conséquent, il appelle à nouveau la **version** . Le décompte de références atteint zéro, et l’objet se supprime lui-même.

Vous vous demandez peut-être pourquoi le programme copiera *p*. Il existe deux raisons principales : tout d’abord, vous souhaiterez peut-être stocker le pointeur dans une structure de données, telle qu’une liste. Deuxièmement, vous souhaiterez peut-être conserver le pointeur au-delà de la portée actuelle de la variable d’origine. Par conséquent, vous pouvez la copier dans une nouvelle variable avec une portée plus étendue.

L’un des avantages du décompte de références est que vous pouvez partager des pointeurs entre différentes sections de code, sans que les différents chemins de code ne coordonnent la suppression de l’objet. Au lieu de cela, chaque chemin de code appelle simplement [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quand ce chemin de code est effectué à l’aide de l’objet. L’objet gère sa suppression à l’heure correcte.

## <a name="example"></a>Exemple

Voici à nouveau le code de l' [exemple de boîte de dialogue Ouvrir](example--the-open-dialog-box.md) .

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

Le décompte de références se produit à deux emplacements dans ce code. Tout d’abord, si le programme crée correctement l’objet de boîte de dialogue d’élément commun, il doit appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pFileOpen* .

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

Deuxièmement, lorsque la méthode [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) retourne un pointeur vers l’interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , le programme doit appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pItem* .

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Notez que dans les deux cas, l’appel de [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) est la dernière chose qui se produit avant que le pointeur ne soit hors de portée. Notez également que **Release** est appelé uniquement après que vous avez testé la réussite de **HRESULT** . Par exemple, si l’appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) échoue, le pointeur *pFileOpen* n’est pas valide. Par conséquent, il serait erroné d’appeler **Release** sur le pointeur.

## <a name="next"></a>Suivant

[Demande d’un objet pour une interface](asking-an-object-for-an-interface.md)