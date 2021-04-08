---
title: Considérations relatives à Unicode
description: La fonction de service WriteFmtUserTypeStg, utilisée dans la méthode IPaper Save, requiert des paramètres de chaîne Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840058"
---
# <a name="unicode-considerations"></a>Considérations relatives à Unicode

La fonction de service **WriteFmtUserTypeStg** , utilisée dans la méthode [**IPaper :: Save**](ipaper--save.md) , requiert des paramètres de chaîne Unicode. C’est le cas avec les appels de service COM/OLE qui prennent des paramètres de chaîne. Lors de la compilation pour les chaînes ANSI, les paramètres Unicode attendus doivent être converties d’ANSI en Unicode. Ce processus est réalisé à l’aide de certaines macros dans APPUTIL. h qui peuvent masquer les conversions. Par exemple, consultez **WriteFmtUserTypeStg**.

L’appel suivant apparaît dans la méthode [**Save**](ipaper--save.md) .


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Quand **StoServe** est compilé pour ANSI (et non pour Unicode), cet appel réduit en fait un appel à une fonction de substitution apputil interne. Pour prendre cela en charge, le schéma de macro suivant est utilisé dans apputil. h, qui est un fichier inclus dans tout l’exemple de code. Fichiers CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



Le schéma utilise des fonctions d’appel de service de substitution. Les versions ANSI des appels commencent par un \_ . Ces fonctions ANSI de substitution sont implémentées dans apputil. cpp. Ils sont utilisés lorsque l’exemple de code est compilé pour les chaînes ANSI (valeur par défaut dans les Makefiles). Les fonctions de service que les substituts sont en place ne prennent en charge que les paramètres de chaîne Unicode. Cela force certaines conversions de chaînes d’ANSI en Unicode avant l’appel du service COM/OLE réel dans le substitut.

Par exemple, si UNICODE n’est pas défini lors de la compilation, tous les appels dans les exemples à la fonction de service **WriteFmtUserTypeStg** com sont en fait modifiés par les macros dans les appels à une \_ fonction WriteFmtUserTypeStg qui est implémentée dans apputil. Cotisations. Cette fonction accepte le pointeur de chaîne ANSI d’entrée, le convertit en copie Unicode et passe cette copie Unicode comme paramètre de chaîne dans un appel à la fonction **WriteFmtUserTypeStg** réelle.

Voici un \_ WriteFmtUserTypeStg de apputil. cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




