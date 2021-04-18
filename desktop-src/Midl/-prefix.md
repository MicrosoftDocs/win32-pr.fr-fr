---
title: commutateur/prefix
description: Le commutateur/prefix indique au compilateur MIDL d’ajouter des chaînes de préfixe aux noms de routines du client et/ou du stub serveur.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL du commutateur/prefix
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507626"
---
# <a name="prefix-switch"></a>commutateur/prefix

Le commutateur **/prefix** indique au compilateur MIDL d’ajouter des chaînes de préfixe aux noms de routines du client et/ou du stub serveur. Cela peut être utilisé pour permettre à un seul programme d’être à la fois un client et un serveur de la même interface, sans que les noms de routines côté client et côté serveur ne soient en conflit.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>client * * * *


</dt> <dd>

Affecte uniquement les noms de routines stub client.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub****


</dt> <dd>

Identique au *client*. Affecte uniquement les noms de routines stub client.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>serveur * * * *


</dt> <dd>

Affecte uniquement les noms de routines appelés par la routine de stub serveur.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub****


</dt> <dd>

Identique au *serveur*. Affecte uniquement les noms de routines appelés par la routine de stub serveur.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>commutateur * * * *


</dt> <dd>

Affecte un prototype supplémentaire ajouté au fichier d’en-tête.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tous les * * * *


</dt> <dd>

Affecte à la fois les noms de routines du client et du serveur.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Si le préfixe pour les routines côté client est différent du préfixe pour les routines côté serveur, le fichier d’en-tête généré aura à la fois des prototypes de routine côté client et des prototypes de routine côté serveur.

Le commutateur **/prefix** est utile lorsqu’un seul fichier d’en-tête est utilisé avec les stubs de plusieurs exécutions du compilateur MIDL. Cela force des prototypes de routine supplémentaires dans le fichier d’en-tête.

Dans tous les cas, les préfixes client, serveur et commutateur remplacent un préfixe All.

## <a name="examples"></a>Exemples

**MIDL/prefix client « c \_ » serveur « s \_ »**

**MIDL/prefix tous « mugissement \_ »**

**MIDL/prefix client « écorce \_ »**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




