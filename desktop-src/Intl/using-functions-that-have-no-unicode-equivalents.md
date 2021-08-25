---
description: Les fonctions qui n’ont pas été implémentées avec une version Unicode ont généralement été remplacées par des fonctions plus puissantes ou étendues qui prennent en charge Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Utilisation de fonctions qui n’ont pas d’équivalents Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787879"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Utilisation de fonctions qui n’ont pas d’équivalents Unicode

Les fonctions qui n’ont pas été implémentées avec une version [Unicode](unicode.md) ont généralement été remplacées par des fonctions plus puissantes ou étendues qui prennent en charge Unicode. Par exemple, si vous portez du code qui appelle la fonction [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , votre application peut prendre en charge Unicode à l’aide de la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) à la place.

Si une fonction n’a pas d’équivalent Unicode, l’application peut mapper des caractères vers et depuis des jeux de caractères 8 bits avant et après l’appel de fonction. Par exemple, les fonctions de mise en forme des nombres **atoi** et **ITOA** utilisent uniquement les chiffres de 0 à 9. Normalement, le mappage Unicode sur des caractères 8 bits entraîne une perte de données, mais cela peut être évité en rendant le type de code indépendant et en rendant les expressions conditionnelles. Les instructions de l’exemple suivant, écrites pour les caractères de 8 bits, sont dépendantes du type et doivent être modifiées pour prendre en charge Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Ces instructions peuvent être réécrites comme suit pour les rendre indépendantes du type.


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



Dans cet exemple, la fonction de bibliothèque C standard **wcstombs** traduit Unicode en ASCII. L’exemple repose sur le fait que les chiffres de 0 à 9 peuvent toujours être convertis du format Unicode au format ASCII, même si une partie du texte environnant ne l’est pas. La fonction **atoi** s’arrête à n’importe quel caractère qui n’est pas un chiffre.

Votre application peut utiliser la fonction [**LCMAPSTRING**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) NLS (National Language Support) pour traiter le texte qui comprend les [chiffres natifs](digit-shapes.md) fournis pour certains scripts Unicode.

> [!Caution]  
> L’utilisation incorrecte de la fonction **wcstombs** peut compromettre la sécurité de votre application. Assurez-vous que la mémoire tampon d’application pour la chaîne de caractères de 8 bits est d’au moins la taille 2 \* (*\_ longueur de caractère* + 1), où la *\_ longueur de caractère* représente la longueur de la chaîne Unicode. Cette restriction est effectuée car, avec des [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS), chaque caractère Unicode peut être mappé à deux caractères 8 bits consécutifs. Si la mémoire tampon ne contient pas la chaîne entière, la chaîne de résultat ne se termine pas par un caractère null, ce qui pose un risque de sécurité. Pour plus d’informations sur la sécurité des applications, consultez Considérations sur la [sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’Unicode et de jeux de caractères](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
