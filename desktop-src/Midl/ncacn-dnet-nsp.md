---
title: attribut ncacn_dnet_nsp
description: Le \_ \_ mot clé ncacn dnet NSP identifie DECnet comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101604"
---
# <a name="ncacn_dnet_nsp-attribute"></a>ncacn \_ dnet, \_ attribut NSP

Le mot clé **ncacn \_ dnet \_ NSP** identifie DECnet comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte. Le nom est une chaîne de caractères.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un nom d’objet DECnet ou un numéro d’objet. Le nom de l’objet peut comporter jusqu’à 16 caractères. Les numéros d’objet peuvent être précédés du signe dièse ( \# ).

</dd> </dl>

## <a name="remarks"></a>Notes

La syntaxe de la chaîne de port de transport DECnet, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

> [!Note]  
> Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.

 

## <a name="examples"></a>Exemples

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 