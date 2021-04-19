---
title: Bouton/w
description: Le commutateur/W spécifie le niveau d’avertissement du compilateur MIDL. Le niveau d’avertissement indique la gravité de l’avertissement.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W, commutateur MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511657"
---
# <a name="w-switch"></a>Bouton/w

Le commutateur **/w** spécifie le niveau d’avertissement du compilateur MIDL. Le niveau d’avertissement indique la gravité de l’avertissement.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*level* 
</dt> <dd>

Spécifie le niveau d’avertissement, un entier compris entre 0 et 4. Il n’y a pas d’espace entre le commutateur **/w** et le chiffre indiquant la valeur de niveau avertissement.

</dd> </dl>

## <a name="remarks"></a>Notes

Les niveaux d’avertissement sont compris entre 1 et 4, avec une valeur égale à zéro pour ne pas afficher d’informations d’avertissement. L’avertissement de gravité la plus élevée est de niveau 1. Le tableau suivant décrit les avertissements pour chaque niveau d’avertissement.



| Niveau d’avertissement | Description                                             | Exemple                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Aucun avertissement.                                            |                                                                           |
| W1            | Avertissements sérieux qui peuvent provoquer des erreurs d’application.      | Aucun handle de liaison spécifié, pointeurs non attributés, commutateurs en conflit. |
| W2            | Peut entraîner des problèmes dans l’environnement d’exploitation de l’utilisateur. | La longueur de l’identificateur dépasse 31 caractères. Aucun ARM d’Union par défaut n’a été spécifié.  |
| W3            | Réservé.                                               |                                                                           |
| W4            | Niveau d’avertissement le plus bas.                                   | Constructions non-ANSI C.                                                    |



 

Les avertissements sont différents des erreurs. Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL. Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.

Le niveau d’avertissement défini par le commutateur **/w** peut être utilisé avec le commutateur [**/WX**](-wx.md) pour faire en sorte que le compilateur MIDL arrête le traitement du fichier IDL.

Le commutateur **/w** se comporte de la même façon que le commutateur [**/WARN**](-warn.md) .

## <a name="examples"></a>Exemples

**MIDL/W2 NomFichier. idl**

**/W4. idl de la barre MIDL**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/WARN**](-warn.md)
</dt> </dl>

 

 




