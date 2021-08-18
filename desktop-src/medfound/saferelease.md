---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034867"
---
# <a name="saferelease"></a>SafeRelease


La plupart des exemples de code de cette documentation utilisent la fonction suivante pour libérer des pointeurs d’interface COM.


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



> [!Note]  
> Cette fonction n’est pas définie dans un en-tête du kit de développement logiciel (SDK). Pour utiliser cette fonction, vous devez la définir dans votre propre code.

 

Cette fonction libère le pointeur *ppT* et lui affecte la **valeur null**.

Une autre option consiste à utiliser une classe de pointeur intelligent, telle que **CComPtr**, qui est définie dans la Active Template Library (ATL).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
