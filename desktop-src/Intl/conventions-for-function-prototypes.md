---
description: le SDK Windows fournit des prototypes de fonction dans des versions génériques, Windows page de codes et Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Conventions pour les prototypes de fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746139"
---
# <a name="conventions-for-function-prototypes"></a>Conventions pour les prototypes de fonctions

le SDK Windows fournit des prototypes de fonction dans des versions génériques, [Windows page de codes](code-pages.md)et [Unicode](unicode.md) . les prototypes peuvent être compilés pour produire Windows prototypes de pages de codes ou des prototypes Unicode. Les trois prototypes sont présentés dans cette rubrique et sont illustrés par des exemples de code pour la fonction [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .

Voici un exemple de prototype générique.


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



Le fichier d'en-tête fournit le nom de la fonction générique implémentée comme macro.


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



le préprocesseur développe la macro dans le Windows la page de codes ou le nom de la fonction Unicode. La lettre « A » (ANSI) ou « W » (Unicode) est ajoutée à la fin du nom de fonction générique, le cas échéant. le fichier d’en-tête fournit ensuite deux prototypes spécifiques, l’un pour Windows pages de codes et l’autre pour Unicode, comme indiqué dans les exemples suivants.


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



comme expliqué dans [Windows Types de données pour les chaînes](windows-data-types-for-strings.md), le prototype de fonction générique utilise le type de données LPCTSTR pour le paramètre text. Toutefois, le prototype de page de codes Windows utilise le type LPCSTR, et le prototype Unicode utilise LPCWSTR.

Pour toutes les fonctions avec des arguments de texte, les applications doivent normalement utiliser les prototypes des fonctions génériques. Si une application définit « UNICODE » avant les instructions **\# include** pour les fichiers d’en-tête ou pendant la compilation, les instructions sont compilées en fonctions Unicode.

> [!Note]  
> les nouvelles Windows applications doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et pour faciliter la localisation. Elles doivent être écrites avec des fonctions génériques et doivent définir UNICODE pour compiler les fonctions en fonctions Unicode. dans les rares emplacements où une application doit fonctionner avec des données de caractères 8 bits, elle peut utiliser de façon explicite les fonctions pour Windows pages de codes.

 

Votre application doit toujours utiliser un prototype de fonction générique avec la chaîne et les types de caractères génériques. Tous les noms de fonctions qui se terminent par un « W » majuscule utilisent Unicode, c.-à-d. des paramètres à caractère large. Certaines fonctions existent uniquement dans les versions Unicode et peuvent être utilisées uniquement avec les types de données appropriés. Par exemple, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) et [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) ont uniquement des versions Unicode.

La section relative à la configuration requise de la documentation de référence pour chaque fonction Unicode et de jeu de caractères fournit des informations sur les versions de fonction implémentées par les systèmes d’exploitation pris en charge. si une ligne commençant par « Unicode » est incluse, la fonction a des versions Unicode et Windows de page de codes distinctes.

> [!Note]  
> Lorsqu’une fonction a un paramètre de longueur pour une chaîne de caractères, la longueur doit être documentée en tant que nombre de valeurs TCHAR dans la chaîne. ce type de données fait référence aux octets des versions de Windows page de codes de la fonction ou des mots 16 bits pour les versions Unicode. Toutefois, les fonctions qui requièrent ou retournent des pointeurs vers des blocs de mémoire non typés, tels que la fonction [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , prennent généralement une taille en octets, quel que soit le prototype utilisé. Si l’allocation de mémoire non typée est pour une chaîne, l’application doit multiplier le nombre de caractères par sizeof (TCHAR). Pour plus d’informations, consultez [utilisation des types de données génériques](using-generic-data-types.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Unicode dans l'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
