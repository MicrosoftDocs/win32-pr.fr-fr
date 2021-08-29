---
title: attribut ncacn_spx
description: Le \_ mot clé ncacn SPX identifie SPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12cb0a9c2e3b7d3a6d78b0e4feda46357f60773b16d67c1d38f57049df3a4d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067069"
---
# <a name="ncacn_spx-attribute"></a>\_attribut ncacn SPX

Le mot clé **ncacn \_ SPX** identifie SPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse de lien* 
</dt> <dd>

Spécifie le serveur hôte. Il peut s’agir d’une chaîne de caractères (nom du serveur) ou d’un nombre hexadécimal à 20 chiffres qui se compose de l’adresse réseau du serveur hôte (8 chiffres) concaténée avec l’adresse du nœud (12 chiffres). Pour obtenir des instructions sur l’obtention de l’adresse réseau et de l’adresse du nœud, consultez la section Notes. Une chaîne **null** spécifie l’ordinateur local.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un nombre 16 bits facultatif qui représente l’adresse du Socket. Les valeurs peuvent être comprises entre 1 et 65 535. Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.

</dd> </dl>

## <a name="remarks"></a>Remarques

lorsque vous utilisez le transport **ncacn \_ spx** , le nom du serveur est exactement le même que le nom de l’Windows 32 bits. Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell. Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec le transport **ncacn \_ SPX** . Voici une liste partielle des caractères interdits dans les noms de serveurs Novell :

" \* + . / : ; < = > ? \[ \] \\ \|

Le transport **ncacn \_ SPX** n’est pas pris en charge par la version de NWLink fournie avec MS client 3,0.

les applications clientes Windows 16 bits qui utilisent le transport **ncacn \_ spx** requièrent que le fichier Nwipxspx.dll soit installé pour pouvoir s’exécuter sous le sous-système WOW. Contactez Novell pour obtenir ce fichier.

> [!Note]  
> Pour obtenir les adresses du réseau et du nœud, utilisez l’utilitaire **ComCheck** de Novell ou l’API définie par Novell **IPXGetInternetAddress**. sur Windows, vous pouvez également obtenir ces adresses à l’aide de la commande **ipxroute config** .

 

La syntaxe de la chaîne de port de transport SPX, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
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

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 