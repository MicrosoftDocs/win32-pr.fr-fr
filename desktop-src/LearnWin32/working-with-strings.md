---
title: Utilisation des chaînes
description: Utilisation des chaînes
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094254"
---
# <a name="working-with-strings"></a>Utilisation des chaînes

Windows prend en charge en mode natif les chaînes Unicode pour les éléments d’interface utilisateur, les noms de fichiers, etc. Unicode est l’encodage de caractères par défaut, car il prend en charge tous les jeux de caractères et toutes les langues. Windows représente des caractères Unicode à l’aide de l’encodage UTF-16, dans lequel chaque caractère est encodé sous la forme d’une valeur de 16 bits. Les caractères UTF-16 sont appelés caractères *larges* , afin de les distinguer des caractères ANSI 8 bits. Le compilateur Visual C++ prend en charge le type de données intégré **WCHAR \_ t** pour les caractères larges. Le fichier d’en-tête Winnt. h définit également le **typedef** suivant.


```C++
typedef wchar_t WCHAR;
```



Vous verrez les deux versions dans l’exemple de code MSDN. Pour déclarer un littéral à caractères larges ou un littéral de chaîne à caractères larges, placez **L** avant le littéral.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Voici d’autres typedefs liés à la chaîne qui s’affichent :



| Typedef                   | Définition       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** ou **LPSTR**     | `char*`          |
| **PCSTR** ou **LPCSTR**   | `const char*`    |
| **PWSTR** ou **LPWStr**   | `wchar_t*`       |
| **PCWSTR** ou **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Fonctions Unicode et ANSI

lorsque Microsoft a introduit la prise en charge d’Unicode pour Windows, il a facilité la transition en fournissant deux jeux d’api parallèles, l’un pour les chaînes ANSI et l’autre pour les chaînes Unicode. Par exemple, il existe deux fonctions pour définir le texte de la barre de titre d’une fenêtre :

-   **SetWindowTextA** prend une chaîne ANSI.
-   **SetWindowTextW** prend une chaîne Unicode.

En interne, la version ANSI convertit la chaîne en Unicode. les en-têtes Windows définissent également une macro qui correspond à la version Unicode lorsque le symbole de préprocesseur `UNICODE` est défini ou la version ANSI dans le cas contraire.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



Dans MSDN, la fonction est documentée sous le nom [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), bien que c’est vraiment le nom de la macro, et non le nom réel de la fonction.

Les nouvelles applications doivent toujours appeler les versions Unicode. De nombreux langages mondiaux requièrent Unicode. Si vous utilisez des chaînes ANSI, il est impossible de localiser votre application. Les versions ANSI sont également moins efficaces, car le système d’exploitation doit convertir les chaînes ANSI au format Unicode au moment de l’exécution. Selon votre préférence, vous pouvez appeler les fonctions Unicode explicitement, telles que **SetWindowTextW**, ou utiliser les macros. L’exemple de code sur MSDN appelle généralement les macros, mais les deux formes sont équivalentes exactement. la plupart des api plus récentes dans Windows ont simplement une version Unicode, sans version ANSI correspondante.

## <a name="tchars"></a>TCHARs

de retour lorsque les applications devaient prendre en charge à la fois Windows NT et Windows 95, Windows 98 et Windows, il était utile de compiler le même code pour les chaînes ANSI ou Unicode, en fonction de la plateforme cible. à cette fin, le SDK Windows fournit des macros qui mappent les chaînes au format Unicode ou ANSI, en fonction de la plateforme.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXTE ("x") | `L"x"`    | `"x"`  |



 

Par exemple, le code suivant :


```C++
SetWindowText(TEXT("My Application"));
```



correspond à l’un des éléments suivants :


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Les macros **Text** et **TCHAR** sont moins utiles aujourd’hui, car toutes les applications doivent utiliser Unicode. Toutefois, vous pouvez les voir dans du code plus ancien et dans certains exemples de code MSDN.

Les en-têtes des bibliothèques Runtime C de Microsoft définissent un ensemble de macros similaire. Par exemple, **\_ tcslen** se résout en **strlen** si `_UNICODE` n’est pas défini ; dans le cas contraire, il est résolu en **wcslen**, qui est la version à caractères larges de **strlen**.


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



ATTENTION : certains en-têtes utilisent le symbole de préprocesseur `UNICODE` , d’autres utilisent `_UNICODE` un préfixe de trait de soulignement. Définissez toujours les deux symboles. Visual C++ les définit toutes les deux par défaut lorsque vous créez un projet.

## <a name="next"></a>Suivant

[Qu’est-ce qu’une fenêtre ?](what-is-a-window-.md)

 

 
