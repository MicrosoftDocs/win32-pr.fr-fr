---
title: commutateur/sstub
description: Le commutateur/sstub spécifie le nom du fichier stub serveur pour une interface RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- MIDL du commutateur/sstub
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106513502"
---
# <a name="sstub-switch"></a>commutateur/sstub

Le commutateur **/sstub** spécifie le nom du fichier stub serveur pour une interface RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_nom du fichier stub \_* 
</dt> <dd>

Spécifie un nom de fichier qui remplace le nom du fichier stub du serveur par défaut. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le nom de fichier spécifié remplace le nom de fichier par défaut. Par défaut, le nom de fichier est obtenu en ajoutant \_ S. C au nom du fichier IDL. Ce commutateur n’affecte pas les interfaces OLE.

Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier stub : le fichier stub qui correspond au fichier IDL spécifié sur la ligne de commande.

Si *le \_ \_ nom du fichier stub* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) . Un chemin d’accès explicite dans le *\_ \_ nom du fichier stub* remplace la spécification du commutateur **/out** .

Le commutateur **/Server** None est prioritaire par rapport au commutateur **/sstub**

## <a name="examples"></a>Exemples

**MIDL/sstub My \_ sstub. c nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




