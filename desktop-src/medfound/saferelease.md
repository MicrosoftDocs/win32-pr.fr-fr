---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520425"
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

 

 
