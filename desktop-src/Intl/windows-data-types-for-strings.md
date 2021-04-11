---
description: La plupart des opérations de chaîne peuvent utiliser la même logique pour Unicode et pour les pages de code Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Types de données Windows pour les chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042854"
---
# <a name="windows-data-types-for-strings"></a>Types de données Windows pour les chaînes

La plupart des opérations de chaîne peuvent utiliser la même logique pour [Unicode](unicode.md) et pour les [pages de code Windows](code-pages.md). La seule différence est que l’unité de base de l’opération est un caractère 16 bits (également appelé caractère élargi) pour Unicode et un caractère 8 bits pour les pages de codes Windows. Les fichiers d’en-tête Windows fournissent plusieurs définitions de type qui facilitent la création de sources pouvant être compilées pour Unicode ou pour les pages de codes Windows.

Windows prend en charge trois ensembles de types de données caractère et chaîne : un ensemble de définitions de types génériques qui peuvent être compilés pour les pages de codes Unicode ou Windows, et deux ensembles de définitions de types spécifiques. Un ensemble de définitions de types spécifiques est destiné à être utilisé avec Unicode, tandis que l’autre est destiné à être utilisé avec les pages de codes Windows.

Une application utilisant des types de données génériques peut être compilée pour Unicode simplement en définissant « UNICODE » avant les instructions **\# include** pour les fichiers d’en-tête, ou pendant la compilation. Les nouvelles applications Windows doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et simplifier la localisation. Elles doivent être écrites avec des types de données génériques et doivent définir « UNICODE » afin de compiler ces types en types Unicode. Dans les rares emplacements où une application doit fonctionner avec des données de type caractère 8 bits, elle peut utiliser les types pour les pages de codes Windows de façon explicite.

La possibilité de compiler les types génériques en types pour les pages de codes Windows existe principalement pour prendre en charge les applications héritées. Pour compiler des pages de codes Windows, l’application omet simplement la définition UNICODE.

L’exemple suivant illustre la méthode utilisée dans les fichiers d’en-tête Windows pour définir les trois jeux de types de données. Pour l’implémentation, consultez le fichier d’en-tête Winnt. h.


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



La lettre « T » dans une définition de type, par exemple TCHAR ou LPTSTR, désigne un type générique qui peut être compilé pour les pages de codes Windows ou Unicode. La lettre « W » dans une définition de type, par exemple WCHAR ou LPWSTR, désigne un type Unicode. Étant donné que les pages de codes Windows sont de l’ancien formulaire, elles ont des définitions de type simples, telles que CHAR et LPSTR. Pour obtenir une description complète des types de données dans Windows, consultez [types de données Windows](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
