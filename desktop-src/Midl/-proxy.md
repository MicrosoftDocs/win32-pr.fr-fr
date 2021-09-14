---
title: commutateur/proxy
description: Le commutateur/proxy spécifie le nom du fichier de proxy d’interface pour une interface COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- MIDL du commutateur/proxy
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093854"
---
# <a name="proxy-switch"></a>commutateur/proxy

Le commutateur **/proxy** spécifie le nom du fichier de proxy d’interface pour une interface com.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_nom du fichier proxy \_* 
</dt> <dd>

Spécifie un nom de fichier qui remplace le nom du fichier de proxy d’interface par défaut. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le nom de fichier spécifié remplace le nom de fichier par défaut obtenu en ajoutant \_ P. C au nom du fichier IDL. Le commutateur/ [**proxy**](proxy.md) n’affecte pas les interfaces RPC.

Si *le \_ \_ nom du fichier proxy* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) . Un chemin d’accès explicite dans le *\_ \_ nom du fichier proxy* remplace la spécification du commutateur **/out** .

Pour obtenir une description plus détaillée du fichier proxy d’interface et des autres fichiers générés par le compilateur MIDL, consultez [syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md).

## <a name="examples"></a>Exemples

**MIDL/proxy mon \_ proxy. c nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




