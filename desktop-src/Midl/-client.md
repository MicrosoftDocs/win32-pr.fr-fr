---
title: commutateur/client
description: Le commutateur/client indique au compilateur MIDL de générer des fichiers sources C côté client pour une interface RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL du commutateur/client
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8361a41aa0e7c87c42eb41508fee0973d6fd4dd821e2008aa2148c8460fc63ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764359"
---
# <a name="client-switch"></a>commutateur/client

Le commutateur **/client** indique au compilateur MIDL de générer des fichiers sources C côté client pour une interface RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * *


</dt> <dd>

Génère les fichiers côté client.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>aucun * * * * *


</dt> <dd>

Ne génère pas de fichiers côté client.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque le commutateur **/client** n’est pas spécifié, le compilateur MIDL génère le fichier stub client. Ce commutateur n’affecte pas les interfaces OLE.

Le commutateur **/client** est prioritaire sur le commutateur [**/cstub**](-cstub.md) .

## <a name="examples"></a>Exemples

**MIDL/client None nom_fichier. idl**

**MIDL/client stub nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




