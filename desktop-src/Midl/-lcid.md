---
title: /LCID (commutateur)
description: L’option de compilateur de/LCID MIDL vous permet d’utiliser des caractères internationaux dans vos fichiers d’entrée, noms de fichiers et chemins d’accès aux répertoires.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID, commutateur MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093917"
---
# <a name="lcid-switch"></a>/LCID (commutateur)

L’option de compilateur de **/LCID** MIDL vous permet d’utiliser des caractères internationaux dans vos fichiers d’entrée, noms de fichiers et chemins d’accès aux répertoires.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*localeID* 
</dt> <dd>

spécifie l’identificateur de paramètres régionaux 32 bits utilisé dans Windows prise en charge des langues nationales. L’identificateur de paramètres régionaux doit être spécifié au format décimal.

</dd> </dl>

## <a name="remarks"></a>Notes

Dans les fichiers d’entrée, vous pouvez utiliser des commentaires, des chaînes, des HelpStrings et des identificateurs localisés. En particulier, le commutateur **/LCID** offre une prise en charge complète des caractères DBCS, pour représenter des langues asiatiques telles que le japonais, le chinois et le coréen.

> [!Note]  
> Le commutateur **/LCID** est disponible avec la version 3.01.75 et ultérieure de MIDL.

 

## <a name="examples"></a>Exemples

**MIDL/LCID 1041 iface. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> </dl>

 

 




