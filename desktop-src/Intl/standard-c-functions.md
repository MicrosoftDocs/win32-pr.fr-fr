---
description: Les bibliothèques Runtime C standard contiennent des versions Unicode UTF-16 (caractères larges) de fonctions de chaîne qui peuvent être utilisées avec des versions Unicode et octet des fonctions de chaîne qui peuvent être utilisées avec des caractères provenant de jeux de caractères codés sur un octet (SBCSs). Le type de données Unicode WCHAR est compatible avec le type de données WCHAR \_ t en ANSI C, et autorise l’accès aux fonctions de chaîne Unicode. Les versions Unicode des fonctions commencent par les lettres &\# 0034 ; wcs&\# 0034 ; (ou parfois &\# 0034 ; \_ WCS&\# 0034 ;). Le type de données CHAR utilisé pour les pages de codes est compatible avec le type de données character en C ANSI, afin d’autoriser l’accès aux fonctions de chaîne de caractères. Les versions caractère des fonctions commencent par les lettres &\# 0034 ; str&\# 0034 ;. Il existe également des versions spéciales pour les jeux de caractères codés sur deux octets (DBCS) qui commencent par les lettres &\# 0034 ; \_ MBS&\# 0034 ;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Fonctions C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121850"
---
# <a name="standard-c-functions"></a>Fonctions C standard

Les bibliothèques Runtime C standard contiennent des versions Unicode UTF-16 (caractères larges) de fonctions de chaîne qui peuvent être utilisées avec des versions [Unicode](unicode.md) et octet des fonctions de chaîne qui peuvent être utilisées avec des caractères provenant de jeux de caractères codés sur [un octet](single-byte-character-sets.md) (SBCSs). Le type de données Unicode WCHAR est compatible avec le type de données WCHAR \_ t en ANSI C, et autorise l’accès aux fonctions de chaîne Unicode. Les versions Unicode des fonctions commencent par les lettres « WCS » (ou parfois « \_ WCS »). Le type de données CHAR utilisé pour les pages de codes est compatible avec le type de données character en C ANSI, afin d’autoriser l’accès aux fonctions de chaîne de caractères. Les versions caractère des fonctions commencent par les lettres « Str ». Il existe également des versions spéciales pour les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS) qui commencent par les lettres « \_ MBS ».

Les bibliothèques Runtime C standard incluent des fonctions génériques pour toutes les fonctions de chaîne C standard. Ils commencent par « \_ TCS » et sont répertoriés dans le fichier d’en-tête Tchar. h. Ces fonctions utilisent le type de données TCHAR générique.

Une application doit ajouter les lignes suivantes pour utiliser les fonctions génériques et compiler pour Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Notez que les fichiers Tchar. h et WCHAR. h sont tous les deux requis et que le trait de soulignement de début de la \_ variable Unicode est également requis. Cette nomenclature est spécifique à la bibliothèque C standard. « UNICODE » s’affiche sans le trait de soulignement pour les runtimes Microsoft Windows.

Les fonctions [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) et [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) peuvent convertir le jeu de caractères pris en charge par la bibliothèque C standard en Unicode et inversement, avec certaines limitations. Pour plus d’informations sur la traduction de chaînes vers et à partir d’Unicode, consultez [translation between types String](translation-between-string-types.md).

La fonction [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) définie dans Tchar. h prend en charge les mêmes spécifications de format que les fonctions d’impression strsafe. h, par exemple [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). De même, Tchar. h définit une fonction [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , dans laquelle la chaîne de format elle-même est une chaîne Unicode.

> [!Caution]  
> Une mauvaise gestion de la mémoire tampon est impliquée dans de nombreux problèmes de sécurité qui impliquent des dépassements de mémoire tampon. Consultez [référence de strsafe. h](../menurc/strsafe-ovw.md). Les fonctions définies dans strsafe. h fournissent un traitement supplémentaire pour la gestion correcte de la mémoire tampon dans votre code. ils sont destinés à remplacer leurs équivalents C/C++ intégrés, ainsi que les implémentations spécifiques de Microsoft Windows. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
