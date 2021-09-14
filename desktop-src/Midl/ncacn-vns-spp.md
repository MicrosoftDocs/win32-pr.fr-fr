---
title: attribut ncacn_vns_spp
description: Le \_ \_ mot clé ncacn réseaux virtuels spp identifie Banyan VINES spp comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093350"
---
# <a name="ncacn_vns_spp-attribute"></a>\_ \_ attribut spp ncacn réseaux virtuels

Le mot clé **ncacn \_ réseaux virtuels \_ spp** identifie Banyan VINES spp comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Spécifie le nom StreetTalk du serveur. Le nom se présente sous la forme item@group @organization . L’élément peut contenir jusqu’à 31 caractères et le groupe et l’organisation peuvent comporter jusqu’à 15 caractères.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un port de Banyan VINES SPP. La plage valide pour les points de terminaison statiques est 250 – 511.

</dd> </dl>

## <a name="remarks"></a>Notes

pour pouvoir utiliser le protocole de transport **ncacn \_ réseaux virtuels \_ spp** dans des applications distribuées exécutées sur Windows 2000, le logiciel Client Banyan Enterprise approprié doit être installé. Après l’installation, ouvrez **le panneau** de **configuration, choisissez Configuration et ajouter**, puis sélectionnez **service \| Banyan \| RPC services pour Banyan**. La prise en charge des clients 16 bits requiert le logiciel Vines approprié. pour plus d’informations sur le produit Enterprise Client banyan et le logiciel de la vigne 16 bits, contactez banyan.

La syntaxe de la chaîne du port de transport Banyan VINES SPP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

> [!Note]  
> cette famille de protocoles n’est pas prise en charge dans Windows XP.

 

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
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

[**ncacn \_ au \_ fournisseur DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ NP**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 