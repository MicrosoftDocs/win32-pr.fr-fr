---
title: attribut Ncalrpc
description: Le mot clé Ncalrpc identifie la communication interprocessus locale comme la famille de protocoles pour le point de terminaison. Ce mot clé est l’un des noms de famille de protocoles valides qui doivent être utilisés avec l’attribut \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- MIDL de l’attribut Ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093333"
---
# <a name="ncalrpc-attribute"></a>attribut Ncalrpc

Le mot clé **Ncalrpc** identifie la communication interprocessus locale comme la famille de protocoles pour le point de terminaison. Ce mot clé est l’un des noms de famille de protocoles valides qui doivent être utilisés avec l’attribut de **\[** [**point de terminaison**](endpoint.md) **\]** .

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du port* 
</dt> <dd>

Chaîne de caractères qui spécifie le port de communication (une application, un service ou une instance d’un service) qu’un client utilise pour effectuer des appels interprocessus à un serveur. La chaîne peut contenir jusqu’à 53 caractères et ne doit pas contenir de barre oblique inverse ( \\ ). Le nom d’ordinateur ne doit pas être utilisé avec le mot clé **Ncalrpc** .

</dd> </dl>

## <a name="remarks"></a>Notes

La syntaxe de la chaîne de port de communication interprocessus locale, comme toutes les chaînes de port, est définie par l’implémentation de transport et est indépendante de la spécification IDL. Le compilateur MIDL effectue une vérification de syntaxe limitée, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines classes d’erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
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

[**ncacn \_ réseaux virtuels \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> <dt>

[Liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 