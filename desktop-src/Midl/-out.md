---
title: /out (commutateur)
description: Le commutateur/out spécifie le répertoire par défaut dans lequel le compilateur MIDL écrit les fichiers de sortie.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- MIDL du commutateur/out
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093865"
---
# <a name="out-switch"></a>/out (commutateur)

Le commutateur **/out** spécifie le répertoire par défaut dans lequel le compilateur MIDL écrit les fichiers de sortie.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*Path-Specification* 
</dt> <dd>

Spécifie le chemin d’accès au répertoire dans lequel le stub, l’en-tête et les fichiers de commutateur sont générés. Une spécification de lecteur, un chemin d’accès absolu au répertoire ou les deux peuvent être spécifiés. Les chemins d’accès peuvent être explicitement placés entre guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le répertoire de sortie peut être spécifié avec une lettre de lecteur, un nom de chemin d’accès absolu, ou les deux. L’option **/out** peut être utilisée avec n’importe quel commutateur qui active la spécification de fichier de sortie individuelle.

Lorsque le commutateur **/out** n’est pas spécifié, les fichiers sont écrits dans le répertoire actif.

Le répertoire par défaut spécifié par le commutateur **/out** peut être substitué par un nom de chemin d’accès explicite spécifié dans le cadre du commutateur [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)ou [**/sstub**](-sstub.md) .

## <a name="examples"></a>Exemples

**MIDL/out c : \\ mydir \\ mysubdir \\ SubDir2 plus profond nom de fichier. idl**

**MIDL/out c : nom_fichier. idl**

**MIDL/out \\ mydir \\ mysubdir \\ un autre nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




