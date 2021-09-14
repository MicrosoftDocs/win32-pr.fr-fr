---
title: Chaînes de commande
description: Chaînes de commande
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Chaînes de commande MCI, à propos de
- Chaînes de commande MCI, syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009556"
---
# <a name="command-strings"></a>Chaînes de commande

Pour envoyer une commande de chaîne à un appareil MCI, utilisez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , qui comprend les paramètres de la commande de chaîne et une mémoire tampon pour toutes les informations retournées.

La fonction **mciSendString** retourne la valeur zéro en cas de réussite. Si la fonction échoue, le mot de poids faible de la valeur de retour contient un code d’erreur. Vous pouvez transmettre ce code d’erreur à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.

## <a name="syntax-of-command-strings"></a>Syntaxe des chaînes de commande

Les chaînes de commande MCI utilisent une syntaxe de modificateur Verb-Object-modifier cohérente. Chaque chaîne de commande comprend une commande, un identificateur d’appareil et des arguments de commande. Les arguments sont facultatifs pour certaines commandes et requis pour d’autres.

Une chaîne de commande se présente sous la forme suivante :

*arguments de l’ID d’appareil de commande \_*

Ces composants contiennent les informations suivantes :

-   La *commande* spécifie une commande MCI, telle que [**ouvrir**](open.md), [**Fermer**](close.md)ou [**lire**](play.md).
-   L' *\_ ID d’appareil* identifie une instance d’un pilote MCI. L' *\_ ID d’appareil* est créé lors de l’ouverture de l’appareil.
-   Les *arguments* spécifient les indicateurs et les variables utilisés par la commande. Les indicateurs sont des mots clés reconnus avec la commande MCI. Les variables sont des nombres ou des chaînes qui s’appliquent à la commande ou à l’indicateur MCI.

    Par exemple, la commande **Play** utilise les arguments « from *position* » et « to *position* » pour indiquer les positions de début et de fin de lecture. Vous pouvez répertorier les indicateurs utilisés avec une commande dans n’importe quel ordre. Quand vous utilisez un indicateur auquel une variable est associée, vous devez fournir une valeur pour la variable.

    Les arguments de commande non spécifiés (et facultatifs) supposent une valeur par défaut.

L’exemple de fonction suivant envoie la commande [**Play**](play.md) avec les indicateurs « from » et « to ».


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>Types de données pour les variables de commande

Vous pouvez utiliser les types de données suivants pour les variables dans une chaîne de commande.



| **Type de données**        | **Description**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chaînes              | Les types de données String sont délimités par des espaces blancs de début et de fin et des guillemets. MCI supprime les guillemets simples d’une chaîne. Pour placer un guillemet dans une chaîne, utilisez un jeu de deux guillemets où vous souhaitez incorporer votre guillemet. Pour utiliser une chaîne vide, utilisez deux guillemets séparés par des espaces blancs de début et de fin. |
| Entiers longs signés | Les types de données entiers longs signés sont délimités par des espaces blancs de début et de fin. Sauf spécification contraire, les entiers peuvent être positifs ou négatifs. Si vous utilisez des entiers négatifs, vous ne devez pas séparer le signe moins et le premier chiffre par un espace.                                                                                                    |
| Rectangles           | Les types de données de rectangle sont une liste triée de quatre valeurs courtes signées. L’espace blanc délimite ce type de données et sépare chaque entier dans la liste.                                                                                                                                                                                                              |



 

 

 