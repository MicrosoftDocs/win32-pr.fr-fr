---
description: Si vous utilisez des types de données génériques dans votre code, il peut être compilé pour Unicode simplement à l’aide d’une directive de préprocesseur pour définir &\# 0034 ; UNICODE&\# 0034 ; avant les \# instructions include pour les fichiers d’en-tête.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Utilisation des types de données génériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224044"
---
# <a name="using-generic-data-types"></a>Utilisation des types de données génériques

Si vous utilisez des types de données génériques dans votre code, il peut être compilé pour [Unicode](unicode.md) simplement à l’aide d’une directive de préprocesseur pour définir « Unicode » avant les instructions **\# include** pour les fichiers d’en-tête. pour compiler le code pour les [pages de codes Windows (ANSI)](code-pages.md), omettez la définition « UNICODE ». les nouvelles Windows applications doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et simplifier la localisation.

pour créer du code source qui peut être compilé soit pour utiliser des chaînes et des caractères Unicode, soit pour utiliser des caractères et des chaînes à partir de Windows pages de codes :

1.  Utilisez des types de données génériques, tels que TCHAR, LPTSTR et LPTCH, pour tous les types de caractères et de chaînes utilisés pour le texte. pour plus d’informations sur les types génériques, consultez [Windows types de données pour les chaînes](windows-data-types-for-strings.md).
2.  Assurez-vous que les pointeurs vers des mémoires tampons de données non textuelles ou des tableaux d’octets binaires sont codés avec des types de données tels que LPBYTE ou LPWORD, au lieu du type LPTSTR ou LPTCH.
3.  Déclarez les pointeurs de type indéterminé explicitement comme pointeurs void en utilisant LPVOID comme il convient.
4.  Rendre le type arithmétique du pointeur indépendant. L’utilisation d’unités de taille TCHAR génère des variables de 2 octets si UNICODE est défini et 1 octet si UNICODE n’est pas défini. L’utilisation de l’arithmétique de pointeur retourne toujours le nombre d’éléments indiqués par le pointeur, que la taille des éléments soit de 1 ou 2 octets. L’expression suivante récupère toujours le nombre d’éléments, qu’UNICODE soit défini ou non.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    L’expression suivante détermine le nombre d’octets utilisés.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Il n’est pas nécessaire de modifier une instruction comme celle qui suit, car l’incrément du pointeur pointe vers l’élément de caractère suivant.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Remplacez les chaînes littérales et les constantes de caractère de manifeste par des macros. Modifiez les expressions comme suit.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Utilisez la macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) comme suit dans cette expression.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    La macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) fait en sorte que les chaînes soient évaluées en tant que L "String" lorsque Unicode est défini, et en tant que "String" dans le cas contraire. Pour faciliter la gestion, déplacez des chaînes littérales dans des ressources, en particulier si elles contiennent des caractères en dehors de la plage ASCII (0x00 à 0x7F) ou sont exposées au niveau de l’interface utilisateur. Pour prendre en charge la localisation de votre application dans différentes langues nationales, il est très important que toutes les chaînes d’interface utilisateur se trouvent dans des ressources localisables.

6.  utilisez les versions génériques des fonctions Windows. Pour plus d’informations, consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).
7.  Utilisez les versions génériques des fonctions de chaîne de la bibliothèque C standard et n’oubliez pas de définir « Unicode », ainsi que \_ « Unicode », comme indiqué dans [fonctions C standard](standard-c-functions.md).
8.  si vous adaptez une application écrite à l’origine pour Windows pages de codes, n’oubliez pas de modifier le code qui s’appuie sur 255 comme valeur la plus élevée pour un caractère.

quand vous compilez le code que vous avez écrit comme indiqué ci-dessus, le compilateur peut créer des versions Unicode et Windows page de codes de votre application à partir de la même source. selon les définitions pour unicode, les fonctions génériques sont résolues pour produire les mêmes fichiers binaires que si vous avez écrit du code exclusivement pour UNICODE ou exclusivement pour Windows pages de codes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’Unicode et de jeux de caractères](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



