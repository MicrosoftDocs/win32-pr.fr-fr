---
title: attribut ncacn_nb_nb
description: Le \_ \_ mot clé ncacn NB NB identifie NetBEUI sur NetBIOS comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093361"
---
# <a name="ncacn_nb_nb-attribute"></a>ncacn \_ NB \_ NB (attribut)

Le mot clé **ncacn \_ NB \_ NB** identifie NetBEUI sur NetBIOS comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du port* 
</dt> <dd>

Spécifie une valeur 8 bits facultative comprise entre 1 et 255. Les valeurs inférieures à 0x20 sont réservées. Si la valeur de *nom de port* n’est pas spécifiée, le service de mappage de point de terminaison sélectionne la valeur de port.

</dd> </dl>

## <a name="remarks"></a>Notes

La syntaxe de la chaîne de port NetBIOS, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL. Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

> [!Note]  
> Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.

 

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
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

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
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

 

 