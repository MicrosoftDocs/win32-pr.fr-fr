---
title: attribut ncadg_ip_udp
description: Le \_ \_ mot clé IP UDP ncadg identifie la version de datagramme de TCP/IP comme famille de protocole pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093346"
---
# <a name="ncadg_ip_udp-attribute"></a>\_ \_ attribut UDP IP ncadg

Le mot clé **\_ IP \_ UDP ncadg** identifie la version de datagramme de TCP/IP comme famille de protocole pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Spécifie le nom ou l’adresse Internet du serveur ou de l’ordinateur hôte. Le nom est une chaîne de caractères et peut être un nom de domaine complet. L’adresse Internet est une notation d’adresse Internet courante.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un nombre 16 bits facultatif. Les valeurs inférieures à 1024 sont généralement réservées. Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Les restrictions suivantes s’appliquent aux protocoles de datagramme, [**ncadg \_ IPX**](ncadg-ipx.md) et **ncadg \_ IP \_ UDP**:

-   Ils ne prennent pas en charge les rappels. Toutes les fonctions qui utilisent l' **\[** attribut [**callback**](callback.md) **\]** échouent.
-   Ils ne prennent pas en charge l’utilisation du constructeur de type [**pipe**](pipe.md) .

La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> <dt>

[Liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 