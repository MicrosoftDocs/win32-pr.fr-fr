---
title: attribut ncadg_ipx
description: Le \_ mot clé IPX ncadg identifie IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725380"
---
# <a name="ncadg_ipx-attribute"></a>ncadg \_ IPX (attribut)

Le mot clé **\_ IPX NCADG** identifie IPX comme famille de protocoles pour le point de terminaison. Cette famille de protocoles est obsolète et ne doit pas être utilisée dans les nouvelles applications.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse de lien* 
</dt> <dd>

Spécifie le serveur hôte. Il peut s’agir d’une chaîne de caractères (nom du serveur) ou d’un nombre hexadécimal à 20 chiffres qui se compose de l’adresse réseau du serveur hôte (8 chiffres) concaténée avec l’adresse du nœud (12 chiffres). Pour obtenir des instructions sur l’obtention de l’adresse réseau et de l’adresse du nœud, consultez la section Notes. Une chaîne **null** spécifie l’ordinateur local.

</dd> <dt>

*nom du port* 
</dt> <dd>

Spécifie un nombre 16 bits facultatif qui représente l’adresse du Socket. Les valeurs peuvent être comprises entre 1 et 65535. Si aucune valeur n’est spécifiée, le service de mappage de point de terminaison sélectionne une valeur de *nom de port* valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Les restrictions suivantes s’appliquent aux protocoles de datagramme, **ncadg \_ IPX** et [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):

-   Ils ne prennent pas en charge les rappels. Toutes les fonctions qui utilisent l' **\[** attribut [**callback**](callback.md) **\]** échouent.
-   Ils ne prennent pas en charge l’utilisation du constructeur de type [**pipe**](pipe.md) .

Lorsque vous utilisez le transport **ncadg \_ IPX** , le nom du serveur est exactement le même que le nom du serveur Windows 32 bits. Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell. Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec le transport **\_ IPX ncadg** . Voici une liste partielle des caractères interdits dans les noms de serveurs Novell :

" \* + . / : ; < = > ? \[ \] \\ \|

Le **transport \_ IPX ncadg** est pris en charge par la version de NWLink fournie avec MS client 3,0.

les applications clientes Windows 16 bits qui utilisent le transport **\_ IPX ncadg** requièrent que le fichier Nwipxspx.dll être installé pour s’exécuter sous le sous-système wow. Contactez Novell pour obtenir ce fichier.

Pour obtenir les adresses du réseau et du nœud, utilisez l’utilitaire **ComCheck** de Novell ou l’API définie par Novell **IPXGetInternetAddress**. Sur Windows, vous pouvez également obtenir ces adresses à l’aide de la commande **ipxroute config** .

La syntaxe de la chaîne de port de transport TCP/IP, comme toutes les chaînes de port, est définie indépendamment de la spécification IDL. Le compilateur effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt qu’au moment de la compilation.

> [!Note]  
> Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.

 

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
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

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 