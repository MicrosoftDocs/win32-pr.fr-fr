---
title: commutateur/cstub
description: Le commutateur/cstub spécifie le nom du fichier stub client pour une interface RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- MIDL du commutateur/cstub
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093945"
---
# <a name="cstub-switch"></a>commutateur/cstub

Le commutateur **/cstub** spécifie le nom du fichier stub client pour une interface RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_nom du fichier stub \_* 
</dt> <dd>

Spécifie un nom de fichier qui remplace le nom du fichier stub client par défaut. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le nom de fichier spécifié remplace le nom de fichier par défaut. Par défaut, le nom de fichier est obtenu en ajoutant l’extension \_ c. c au nom du fichier IDL. Ce commutateur n’affecte pas les interfaces OLE.

Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier stub : le fichier stub qui correspond au fichier IDL spécifié sur la ligne de commande.

Si *le \_ \_ nom du fichier stub* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) . Un chemin d’accès explicite dans le *\_ \_ nom du fichier stub* remplace la spécification du commutateur **/out** .

Le commutateur **/client** None est prioritaire sur le commutateur **/cstub** .

## <a name="examples"></a>Exemples

**MIDL/cstub My \_ cstub. c nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/Header**](-header.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




