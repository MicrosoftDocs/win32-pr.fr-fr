---
title: Structure de IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ structure d' \_ adresse IP de tronçon suivant \_ contient l’adresse du routeur de tronçon suivant pour un itinéraire IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS de la structure RAS
- PIP_NEXT_HOP_ADDRESS de la structure RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222529"
---
# <a name="ip_next_hop_address-structure"></a>Structure d’adresse IP de \_ \_ tronçon suivant \_

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure d' **adresse IP de \_ \_ tronçon \_ suivant** contient l’adresse du routeur de tronçon suivant pour un itinéraire IP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**N \_ numéro Netnumber**
</dt> <dd>

Spécifie l’adresse réseau IP exprimée sous la forme d’une adresse IP dans l’ordre des octets de l’ordinateur.

</dd> <dt>

**N \_ masque réseau**
</dt> <dd>

Spécifie le masque de réseau. Appliquez ce masque à l’adresse IP afin d’extraire l’adresse réseau. Le masque de réseau est dans l’ordre des octets de l’ordinateur.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure d' **\_ \_ \_ adresse de tronçon suivant IP** est un typedef de la structure de [**\_ réseau IP**](ip-network.md) . Le typedef se trouve dans RTM. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Structures de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_réseau IP**](ip-network.md)
</dt> <dt>

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





