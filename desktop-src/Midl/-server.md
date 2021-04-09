---
title: commutateur/Server
description: Le commutateur/Server indique au compilateur MIDL de générer des fichiers sources C côté serveur pour une interface RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- MIDL du commutateur/Server
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030254"
---
# <a name="server-switch"></a>commutateur/Server

Le commutateur **/Server** indique au compilateur MIDL de générer des fichiers sources C côté serveur pour une interface RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * *


</dt> <dd>

Génère les fichiers côté serveur.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>aucun * * * * *


</dt> <dd>

Ne génère pas de fichiers côté serveur.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Lorsque le commutateur **/Server** n’est pas spécifié, le compilateur MIDL génère le fichier stub serveur. Ce commutateur n’affecte pas les interfaces OLE.

L’option **None** n’entraîne pas la génération de fichiers.

Le commutateur **/Server** est prioritaire par rapport au commutateur **/sstub**

## <a name="examples"></a>Exemples

**MIDL/Server aucun**

**stub/Server MIDL**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




