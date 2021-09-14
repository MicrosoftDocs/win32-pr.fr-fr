---
title: commutateur/Protocol
description: Le commutateur/Protocol spécifie quel protocole câble est pris en charge par le stub généré.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- MIDL du commutateur/Protocol
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555482677afff83d9f52e06c7b8e445504d222c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093857"
---
# <a name="protocol-switch"></a>commutateur/Protocol

Le commutateur **/Protocol** spécifie quel protocole câble est pris en charge par le stub généré.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>DCE * * * * *


</dt> <dd>

Le stub généré prend en charge uniquement le protocole DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

Le stub généré prend en charge uniquement le protocole Microsoft NDR64.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tous les * * * *


</dt> <dd>

Le stub généré prend en charge tous les protocoles disponibles pour un environnement donné.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

RPC marshale et démarshale les données en fonction d’un protocole strict Wire, également appelé syntaxe de transfert, qui définit la représentation de la transmission de données, telles que l’ordre dans lequel les données membres sont marshalées, l’alignement des données sur le câble, les informations supplémentaires incluses avec les données, entre autres. Microsoft RPC est compatible avec le protocole NDR (Network Data Representation) de l’ETCD OSF. dans la version 64 bits de Windows XP, Microsoft introduit un NDR64 de protocole expérimental qui est optimisé pour le transfert de données 64 bits. NDR64 n’est pas à compatibilité descendante avec le protocole DCE.

Le protocole **DCE** est compatible avec la syntaxe de transfert de NDR de l’ETCD OSF. Ce protocole est optimisé pour le transfert de données 32 bits.

Le protocole **ndr64** est actuellement pris en charge uniquement lorsqu’il est utilisé conjointement avec le commutateur [**/Win64**](-win64.md) . Si un client ndr64 uniquement tente de se connecter à un serveur DCE uniquement, ou vice versa, l’appel est rejeté avec la valeur de \_ \_ trans syn non prise en charge par RPC \_ \_ .

L’option **All** crée un stub qui peut utiliser n’importe quel protocole disponible. Pour les stubs 32 bits, le seul protocole actuellement disponible est DCE. Pour les stubs 64 bits, créés à l’aide du commutateur [**/Win64**](-win64.md) , DCE et NDR64 sont disponibles.

## <a name="examples"></a>Exemples

**MIDL/Protocol tous/Win64 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/&lt;requise&gt;**](-system-.md)
</dt> </dl>

 

 




