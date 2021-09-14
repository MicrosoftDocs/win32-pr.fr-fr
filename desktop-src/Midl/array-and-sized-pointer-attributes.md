---
title: Attributs de tableau et de Sized-Pointer
description: MIDL fournit un ensemble complet de fonctionnalités pour passer des tableaux de données et des pointeurs vers des données. Vous pouvez utiliser ces attributs pour spécifier les caractéristiques des tableaux et plusieurs niveaux de pointeurs.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- IDL MIDL, attributs, tableau et pointeur de dimensionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093785"
---
# <a name="array-and-sized-pointer-attributes"></a>Attributs de tableau et de Sized-Pointer

MIDL fournit un ensemble complet de fonctionnalités pour passer des tableaux de données et des pointeurs vers des données. Vous pouvez utiliser ces attributs pour spécifier les caractéristiques des tableaux et plusieurs niveaux de pointeurs.



| Attribut                       | Usage                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**la taille \_ est**](size-is.md)     | Spécifie la quantité de mémoire à allouer pour les pointeurs dimensionnés, les pointeurs dimensionnés aux pointeurs dimensionnés et les tableaux à une ou plusieurs dimensions.                                                         |
| [**le nombre maximal \_ est**](max-is.md)       | Valeur maximale d’un index de tableau.                                                                                                                                                                |
| [**la longueur \_ est**](length-is.md) | Nombre d’éléments de tableau à transmettre.                                                                                                                                                      |
| [**tout d’abord, \_**](first-is.md)   | Index du premier élément de tableau à transmettre.                                                                                                                                              |
| [**la dernière \_ est**](last-is.md)     | Indique l’index du dernier élément de tableau à transmettre.                                                                                                                                         |
| [**chaîne**](string.md)        | Indique que le tableau de [**caractères**](char-idl.md)unidimensionnel, [**WCHAR \_ t**](wchar-t.md), [**Byte**](byte.md) (ou équivalent), ou le pointeur vers ce type de tableau, doit être géré comme une chaîne. |
| [**vont**](range.md)          | Spécifie une plage de valeurs autorisées pour les arguments ou les champs dont les valeurs sont définies au moment de l’exécution.                                                                                                       |



 

MIDL prend en charge trois types de pointeurs : les pointeurs de référence, les pointeurs uniques et les pointeurs complets. Ces pointeurs sont spécifiés par les attributs de pointeur [**ref**](ref.md), [**unique**](unique.md)et [**ptr**](ptr.md).

Un attribut de pointeur peut être appliqué en tant qu’attribut de type ; en tant qu’attribut de champ qui s’applique à un membre de structure, un membre d’Union ou un paramètre ; ou en tant qu’attribut de fonction qui s’applique au type de retour de la fonction. L’attribut de pointeur peut également apparaître avec le mot clé [**\_ default du pointeur**](pointer-default.md) .

Pour permettre à un paramètre de pointeur de changer de valeur pendant une fonction distante, vous devez fournir un autre niveau d’indirection en fournissant plusieurs déclarateurs de pointeurs. L’attribut de pointeur explicite appliqué au paramètre affecte uniquement le déclarateur de pointeur le plus à droite pour le paramètre. Lorsqu’il existe plusieurs déclarateurs de pointeur dans une déclaration de paramètre, les autres déclarateurs utilisent par défaut l’attribut de pointeur spécifié par l’attribut de [**pointeur \_ par défaut**](pointer-default.md) . Pour appliquer différents attributs de pointeur à plusieurs déclarateurs de pointeurs, vous devez définir des types intermédiaires qui spécifient les attributs de pointeur explicites.

## <a name="default-pointer-attribute-values"></a>Valeurs de Pointer-Attribute par défaut

Quand aucun attribut de pointeur n’est associé à un pointeur qui est un paramètre, le pointeur est supposé être un pointeur [**ref**](ref.md) .

Quand aucun attribut de pointeur n’est associé à un pointeur qui est membre d’une structure ou d’une Union, le compilateur MIDL assigne des attributs de pointeur à l’aide des règles de priorité suivantes (1 est le plus élevé) :

1.  Attributs explicitement appliqués au type pointeur
2.  Attributs explicitement appliqués au paramètre ou au membre du pointeur
3.  Attribut [**\_ par défaut du pointeur**](pointer-default.md) dans le fichier IDL qui définit le type
4.  Attribut [**\_ par défaut du pointeur**](pointer-default.md) dans le fichier IDL qui importe le type
5.  [**ptr**](ptr.md) (mode OSF); [**unique**](unique.md) (mode Microsoft RPC par défaut)

Lorsque le fichier IDL est compilé en mode par défaut, les fichiers importés peuvent hériter des attributs de pointeur de l’importation des fichiers. Cette fonctionnalité n’est pas disponible quand vous compilez à l’aide du commutateur/[**OSF**](-osf.md) . Pour plus d’informations, consultez [**Import**](import.md).

## <a name="function-return-types"></a>Types de retour de fonction

Un pointeur retourné par une fonction doit être un pointeur [**unique**](unique.md) ou un pointeur complet. Le compilateur MIDL signale une erreur si un résultat de fonction est un pointeur de référence, soit explicitement, soit par défaut. Le pointeur retourné indique toujours un nouveau stockage.

Les fonctions qui retournent une valeur de pointeur peuvent spécifier un attribut de pointeur comme attribut de fonction. Si un attribut de pointeur n’est pas présent, le pointeur de fonction-result utilise la valeur fournie comme attribut [**\_ par défaut du pointeur**](pointer-default.md) .

## <a name="pointer-attributes-in-type-definitions"></a>Attributs de pointeur dans les définitions de type

Lorsque vous spécifiez un attribut de pointeur au niveau supérieur d’une instruction [**typedef**](typedef.md) , l’attribut spécifié est appliqué au déclarateur de pointeur, comme prévu. Quand aucun attribut de pointeur n’est spécifié, les déclarateurs de pointeurs au niveau supérieur d’une instruction typedef héritent du type d’attribut de pointeur lorsqu’ils sont utilisés.

L’IDL DCE n’autorise pas l’application explicite d’un même attribut de pointeur à deux reprises, par exemple dans la Déclaration [**typedef**](typedef.md) et la liste d’attributs de paramètres. Lorsque vous utilisez le mode par défaut (extensions Microsoft) du compilateur MIDL, cette contrainte est assouplie.

Pour plus d’informations sur l’utilisation de tableaux et de pointeurs MIDL dans les appels de procédure distante, consultez [tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).

 

 