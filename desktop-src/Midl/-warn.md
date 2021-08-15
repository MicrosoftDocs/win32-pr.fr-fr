---
title: commutateur/WARN
description: Le commutateur/WARN spécifie le niveau d’avertissement du compilateur MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- commutateur/WARN MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067454"
---
# <a name="warn-switch"></a>commutateur/WARN

Le commutateur **/WARN** spécifie le niveau d’avertissement du compilateur MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*level* 
</dt> <dd>

Spécifie le niveau d’avertissement, un entier compris entre 0 et 4. Il n’y a pas d’espace entre le commutateur **/WARN** et le chiffre indiquant la valeur de niveau avertissement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le niveau d’avertissement indique la gravité de l’avertissement. Les niveaux d’avertissement sont compris entre 1 et 4, avec une valeur égale à zéro pour ne pas afficher d’informations d’avertissement. L’avertissement de gravité la plus élevée est le niveau 1. Le tableau suivant décrit les avertissements pour chaque niveau d’avertissement.



| Niveau d’avertissement | Description                                             |  Exemple                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Aucun avertissement.                                            |                                                                           |
| 1             | Avertissements sérieux qui peuvent provoquer des erreurs d’application.      | Aucun handle de liaison spécifié, pointeurs non attributés, commutateurs en conflit. |
| 2             | Peut entraîner des problèmes dans l’environnement d’exploitation de l’utilisateur. | La longueur de l’identificateur dépasse 31 caractères. Aucun ARM d’Union par défaut n’a été spécifié.  |
| 3             | Réservé.                                               |                                                                           |
| 4             | Niveau d’avertissement le plus bas.                                   | Constructions non-ANSI C.                                                    |



 

Les avertissements sont différents des erreurs. Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL. Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.

Le niveau d’avertissement défini par le commutateur **/WARN** peut être utilisé avec le commutateur [**WX**](-wx.md) pour faire en sorte que le compilateur MIDL arrête le traitement du fichier IDL.

Le commutateur **/WARN** se comporte de la même façon que le commutateur [**/w**](-w.md) .

## <a name="examples"></a>Exemples

**MIDL/warn2 NomFichier. idl**

**/warn4. idl de la barre MIDL**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




