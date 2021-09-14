---
title: commutateur/IID
description: Le commutateur/IID spécifie le nom du fichier d’identificateur d’interface pour une interface COM, en remplaçant le nom par défaut obtenu en ajoutant \_ i. c au nom de fichier IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL du commutateur/IID
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093918"
---
# <a name="iid-switch"></a>commutateur/IID

Le commutateur **/IID** spécifie le nom du fichier d’identificateur d’interface pour une interface com, en remplaçant le nom par défaut obtenu en ajoutant \_ i. c au nom de fichier IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*extension* 
</dt> <dd>

Spécifie un nom de fichier d’identificateur d’interface qui remplace le nom de fichier de l’identificateur d’interface par défaut pour une interface COM. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le commutateur **/IID** n’affecte pas les interfaces RPC.

Si *filename* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) . Un chemin d’accès explicite dans *filename* remplace la spécification du commutateur **/out** .

## <a name="examples"></a>Exemples

**MIDL/IID "My \_ IID. c" nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




