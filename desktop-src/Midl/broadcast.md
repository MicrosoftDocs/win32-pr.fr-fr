---
title: attribut de diffusion
description: Le mot clé \ Broadcast \ spécifie que les appels de procédure distante doivent être envoyés à tous les serveurs sur un réseau local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- attribut de diffusion MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093758"
---
# <a name="broadcast-attribute"></a>attribut de diffusion

Le mot clé **\[ Broadcast \]** spécifie que les appels de procédure distante doivent être envoyés à tous les serveurs sur un réseau local.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie des attributs supplémentaires à appliquer à la fonction. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction à laquelle l’attribut de **\[ diffusion \]** sera appliqué.

</dd> <dt>

*params* 
</dt> <dd>

Liste des paramètres de la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

Le mot clé **\[ Broadcast \]** spécifie que la routine est toujours diffusée à tous les serveurs sur le réseau, au lieu d’être remise à un serveur particulier. Le client reçoit la sortie de la première réponse pour qu’elle retourne correctement, tandis que les réponses suivantes sont ignorées.

Une opération avec l’attribut **\[ Broadcast \]** est implicitement une opération [**\[ idempotent \]**](idempotent.md) . Toutefois, l’attribut **\[ Broadcast \]** spécifie des propriétés supplémentaires que les fonctions avec l’attribut **\[ idempotent \]** n’ont pas. Plus précisément, les fonctions qui utilisent l’attribut **\[ Broadcast \]** spécifient que la routine peut être appelée plusieurs fois à la suite d’un appel de procédure distante. En même temps, ils peuvent être envoyés à plusieurs serveurs. Cela diffère de l’attribut **\[ idempotent \]** , qui spécifie uniquement qu’un appel peut être retenté s’il n’est pas terminé.

Si une procédure distante diffuse son appel à tous les ordinateurs hôtes sur un réseau local, elle doit utiliser la séquence de [**protocole \_ IPX**](ncadg-ipx.md) [**ncadg \_ \_ IP**](ncadg-ip-udp.md) ou ncadg. Notez que la taille d’un paquet de **\[ diffusion \]** est déterminée par le service de datagramme en cours d’utilisation.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**environ**](maybe.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**\_IPX ncadg**](ncadg-ipx.md)
</dt> </dl>

 

 




