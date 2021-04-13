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
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312961"
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

## <a name="remarks"></a>Notes

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

 

 




