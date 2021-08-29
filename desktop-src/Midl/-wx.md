---
title: /WX (commutateur)
description: Le commutateur/WX demande au compilateur MIDL de gérer toutes les erreurs au niveau d’avertissement donné comme des erreurs.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX, commutateur MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5255b7256b82889f50b6bcffbc323e405f31d1423bb51a5b35b716dca170a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913619"
---
# <a name="wx-switch"></a>/WX (commutateur)

Le commutateur **/WX** demande au compilateur MIDL de gérer toutes les erreurs au niveau d’avertissement donné comme des erreurs.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Si le commutateur **/WX** est spécifié et que le commutateur [**/w**](-w.md)*n* n’est pas spécifié, tous les avertissements au niveau par défaut, Level 1, sont traités comme des erreurs.

Le commutateur [**/w**](-w.md)*n* indique au compilateur d’afficher tous les avertissements au niveau *n* et **/WX** indique au compilateur de gérer tous les avertissements comme des erreurs. La combinaison de ces deux commutateurs indique au compilateur de gérer tous les avertissements au niveau *n* comme des erreurs.

Les erreurs sont différentes des avertissements. Les erreurs provoquent l’arrêt du traitement du fichier IDL par le compilateur MIDL. Les avertissements font en sorte que le compilateur MIDL émette un message d’information et continue le traitement du fichier IDL.

AVERTISSEMENT : le niveau zéro (0) indique au compilateur MIDL de supprimer les informations d’avertissement. Lorsque les commutateurs **/W0** et **/WX** sont combinés, le compilateur MIDL supprime toutes les informations d’avertissement. Dans ce cas, le commutateur **/WX** n’a aucun effet.

## <a name="examples"></a>Exemples

**MIDL/WX nom_fichier. idl**

**MIDL/W3/WX nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




