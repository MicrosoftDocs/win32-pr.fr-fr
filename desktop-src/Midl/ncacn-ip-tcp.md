---
title: attribut ncacn_ip_tcp
description: Le \_ \_ mot clé TCP IP NCACN identifie TCP/IP comme famille de protocoles pour le point de terminaison.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093373"
---
# <a name="ncacn_ip_tcp-attribute"></a>ncacn \_ TCP IP ( \_ attribut)

Le mot clé **\_ \_ TCP IP ncacn** identifie TCP/IP comme famille de protocoles pour le point de terminaison.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte. Le nom est une chaîne de caractères. L’adresse Internet est une notation d’adresse Internet courante.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un nombre 16 bits facultatif. Les valeurs inférieures à 1024 sont généralement réservées. Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.

</dd> </dl>

## <a name="remarks"></a>Notes

La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 