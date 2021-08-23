---
description: Décrit comment initialiser un modèle d’objet XPS, qui permet à un programme de créer un document XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Initialiser un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16edb992efee7c9cba1d5bc454ca5bcb44bd3267a2e91d4ca714120182df0657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946991"
---
# <a name="initialize-an-xps-om"></a>Initialiser un modèle d’objet XPS

Décrit comment initialiser un modèle d’objet XPS, qui permet à un programme de créer un document XPS.

Les interfaces de l’API de document XPS sont créées par une interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) . Pour obtenir un pointeur vers un **IXpsOMObjectFactory** qui peut être utilisé dans votre programme, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).

## <a name="code-example"></a>Exemple de code

L’exemple suivant crée la fabrique d’objet qui sera utilisée pour créer des interfaces OM XPS dans d’autres exemples.


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a>Meilleures pratiques

Vous pouvez rendre votre programme plus efficace en obtenant un pointeur vers une interface [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la première fois que vous devez appeler **IXpsOMObjectFactory** pour créer une interface, puis enregistrer le pointeur pour l’utiliser dans d’autres zones du programme. Lorsque le programme n’a plus besoin de la fabrique d’objet ou qu’il n’en a plus besoin pendant un certain temps, le pointeur peut être relâché.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Créer un modèle d’objet XPS vide](create-a-blank-xps-om.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
