---
description: Cette rubrique décrit les différences entre les fonctions de chaîne utilisées pour gérer les informations Unicode et les jeux de caractères. ces fonctions ont à la fois des implémentations de pages de codes unicode et Windows pour prendre en charge les paramètres de page de codes unicode et Windows.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Différences de fonction de chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121846"
---
# <a name="string-function-differences"></a>Différences de fonction de chaîne

Cette rubrique décrit les différences entre les fonctions de chaîne utilisées pour gérer les informations Unicode et les jeux de caractères. ces fonctions ont à la fois des implémentations de [pages de codes](code-pages.md) [unicode](unicode.md) et Windows pour prendre en charge les paramètres de page de codes unicode et Windows.

Les fonctions de chaîne suivantes ne requièrent pas de commentaire spécial. leurs implémentations Unicode et Windows page de codes fonctionnent de manière identique.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

la valeur de longueur récupérée par l’une des fonctions de longueur de chaîne est toujours basée sur la largeur de caractère normale : 8 bits pour les pages de codes Windows, 16 bits pour Unicode. Cette valeur est souvent appelée « nombre de caractères ». ce terme est strictement correct, car Windows pages de codes qui utilisent des [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (dbcs) ont des caractères à pleine chasse qui sont réellement représentés par deux octets consécutifs. Une situation similaire se produit pour les [substituts](surrogates-and-supplementary-characters.md) en Unicode.

Les fonctions de chaîne suivantes sont sensibles aux paramètres régionaux du thread actuel, dérivées de la langue sélectionnée par l’utilisateur dans le panneau de configuration. Les fonctions [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) et [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) n’effectuent pas de comparaisons d’octets comme leurs namesakes ANSI, par exemple, [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Au lieu de cela, ils comparent les chaînes en fonction des règles des paramètres régionaux.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

les fonctions suivantes effectuent une conversion entre le jeu de caractères OEM et la page de codes ou Unicode actuelle Windows, selon la version utilisée :

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Les fonctions d’impression, par exemple [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), prennent en charge Unicode en fournissant les types de données nouveaux et modifiés suivants dans leurs spécifications de format. Ces spécifications de format affectent la manière dont les fonctions interprètent le paramètre d’entrée correspondant.



| Spécification de format | type de données pour Windows version de la page de codes | Type de données pour la version Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, hC               | CHAR                                    | CHAR                          |
| HS, hS               | LPSTR                                   | LPSTR                         |
| LC, lC               | WCHAR                                   | WCHAR                         |
| LS, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

Le type de données du texte de sortie dépend toujours de la version de la fonction. lorsque le type de données du paramètre d’entrée et le type de données du texte de sortie ne correspondent pas, la fonction print effectue une conversion d’Unicode vers la page de codes Windows actuelle, ou vice versa, selon les besoins.

Pour la version Unicode des fonctions d’impression, la chaîne de format est Unicode, comme le texte de sortie.

> [!Caution]  
> Une mauvaise gestion de la mémoire tampon est impliquée dans de nombreux problèmes de sécurité qui impliquent des dépassements de mémoire tampon. Consultez [référence de strsafe. h](../menurc/strsafe-ovw.md). Les fonctions définies dans strsafe. h fournissent un traitement supplémentaire pour la gestion correcte de la mémoire tampon dans votre code. pour cette raison, ils sont destinés à remplacer leurs équivalents C/C++ intégrés, ainsi que les implémentations spécifiques de Microsoft Windows. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
