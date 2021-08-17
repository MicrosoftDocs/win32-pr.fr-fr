---
description: la plupart des opérations de chaîne peuvent utiliser la même logique pour Unicode et pour Windows pages de codes.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Types de données Windows pour les chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bef3dc98b7b8649b6cb0fc5bd9450c6f22c8b2bb6e3345790dab0dd24587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146812"
---
# <a name="windows-data-types-for-strings"></a>Types de données Windows pour les chaînes

la plupart des opérations de chaîne peuvent utiliser la même logique pour [Unicode](unicode.md) et pour [Windows pages de codes](code-pages.md). la seule différence est que l’unité de base de l’opération est un caractère 16 bits (également appelé caractère élargi) pour Unicode et un caractère 8 bits pour Windows pages de codes. les fichiers d’en-tête Windows fournissent plusieurs définitions de type qui facilitent la création de sources pouvant être compilées pour Unicode ou pour Windows pages de codes.

Windows prend en charge trois jeux de types de données caractère et chaîne : un ensemble de définitions de types génériques qui peuvent être compilés pour des pages de codes Unicode ou Windows, et deux ensembles de définitions de types spécifiques. un ensemble de définitions de types spécifiques est destiné à être utilisé avec Unicode, tandis que l’autre est destiné à être utilisé avec des pages de codes Windows.

Une application utilisant des types de données génériques peut être compilée pour Unicode simplement en définissant « UNICODE » avant les instructions **\# include** pour les fichiers d’en-tête, ou pendant la compilation. les nouvelles Windows applications doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et simplifier la localisation. Elles doivent être écrites avec des types de données génériques et doivent définir « UNICODE » afin de compiler ces types en types Unicode. dans les rares emplacements où une application doit fonctionner avec des données de type caractère 8 bits, elle peut utiliser de façon explicite les types pour Windows pages de codes.

la possibilité de compiler les types génériques en types pour Windows pages de codes existe principalement pour prendre en charge les applications héritées. pour compiler des pages de codes Windows, l’application omet simplement la définition UNICODE.

l’exemple suivant illustre la méthode utilisée dans les fichiers d’en-tête Windows pour définir les trois jeux de types de données. Pour l’implémentation, consultez le fichier d’en-tête Winnt. h.


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



la lettre « T » dans une définition de type, par exemple TCHAR ou LPTSTR, désigne un type générique qui peut être compilé pour Windows pages de codes ou Unicode. La lettre « W » dans une définition de type, par exemple WCHAR ou LPWSTR, désigne un type Unicode. étant donné que Windows pages de codes sont de l’ancien format, elles ont des définitions de type simples, telles que CHAR et LPSTR. pour obtenir une description complète des types de données dans Windows, consultez [Windows types de données](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
