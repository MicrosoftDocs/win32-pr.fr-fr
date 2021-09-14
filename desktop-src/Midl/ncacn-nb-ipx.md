---
title: attribut ncacn_nb_ipx
description: Le \_ \_ mot clé ncacn NB IPX identifie NetBIOS sur IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093370"
---
# <a name="ncacn_nb_ipx-attribute"></a>\_attribut ncacn NB \_ IPX

Le mot clé **ncacn \_ NB \_ IPX** identifie NetBIOS sur IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du port* 
</dt> <dd>

Spécifie une valeur 8 bits facultative comprise entre 1 et 254. Les valeurs inférieures à 0x20 sont réservées. Si la valeur de *nom de port* n’est pas spécifiée, le service de mappage de point de terminaison sélectionne la valeur de port.

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
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ au \_ fournisseur DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> <dt>

[**liaison de chaîne**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 