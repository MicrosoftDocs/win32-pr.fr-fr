---
title: commutateur/ACF
description: Le commutateur/ACF permet à l’utilisateur de fournir un nom de fichier ACF explicite. Le commutateur autorise également l’utilisation de différents noms d’interface dans les fichiers IDL et ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- MIDL du commutateur/ACF
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940489"
---
# <a name="acf-switch"></a>commutateur/ACF

Le commutateur **/ACF** permet à l’utilisateur de fournir un nom de fichier ACF explicite. Le commutateur autorise également l’utilisation de différents noms d’interface dans les fichiers IDL et ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_nom de fichier ACF* 
</dt> <dd>

Spécifie le nom du CCP. Un espace blanc peut ou non être présent entre le commutateur **/ACF** et le nom de fichier.

</dd> </dl>

## <a name="remarks"></a>Notes

Par défaut, le compilateur MIDL construit le nom du CCP en remplaçant l’extension de nom de fichier IDL (généralement. idl) par. ACF. Quand le commutateur **/ACF** est présent, le CCP prend son nom à partir du nom de fichier spécifié. Le commutateur **/ACF** s’applique uniquement au fichier IDL spécifié sur la ligne de commande du compilateur MIDL. Elle ne s’applique pas aux fichiers importés.

Lorsque le commutateur **/ACF** est utilisé, le nom d’interface dans le ACF n’a pas besoin d’être identique au nom de l’interface MIDL. Cette fonctionnalité permet aux interfaces de partager une spécification ACF.

Lorsqu’un chemin d’accès absolu à un ACF n’est pas spécifié, le compilateur MIDL recherche dans le répertoire actif, les répertoires fournis par l’option [**/i**](-i.md) et les répertoires dans le chemin d’accès include.

Si le ACF est introuvable, le compilateur MIDL suppose qu’il n’existe aucun CCP pour cette interface. Pour plus d’informations sur la séquence de répertoires, consultez les entrées de référence pour les commutateurs [**/i**](-i.md) et [**/non \_ Def \_ idir**](-no-def-idir.md) . Pour plus d’informations sur **/ACF**, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Exemples

**MIDL/ACF. ACF nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/non \_ Def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




