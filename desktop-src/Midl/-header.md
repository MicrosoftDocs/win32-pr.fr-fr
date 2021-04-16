---
title: commutateur/Header
description: Le commutateur/Header spécifie le nom du fichier d’en-tête.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- MIDL du commutateur/Header
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380890"
---
# <a name="header-switch"></a>commutateur/Header

Le commutateur **/header** spécifie le nom du fichier d’en-tête.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*extension* 
</dt> <dd>

Spécifie un nom de fichier d’en-tête qui remplace le nom du fichier d’en-tête par défaut. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter des caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le nom de fichier spécifié remplace le nom de fichier par défaut. Le nom de fichier par défaut est obtenu en remplaçant l’extension de nom de fichier IDL (généralement. idl) par l’extension de nom de fichier. h. Pour les interfaces OLE, le commutateur **/header** remplace le nom par défaut du fichier d’en-tête d’interface.

Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier d’en-tête : le fichier d’en-tête qui correspond au fichier IDL spécifié sur la ligne de commande.

Si *filename* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) . Un chemin d’accès explicite dans *filename* remplace la spécification du commutateur **/out** .

## <a name="examples"></a>Exemples

**MIDL/Header « bar. h » NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




