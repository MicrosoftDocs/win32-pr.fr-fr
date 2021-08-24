---
title: Structure de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ structure de données spécifique au protocole \_ contient de la mémoire réservée pour les données spécifiques à un protocole de routage particulier.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe43e17827a4c6308c7bfd4499de60ec9105a9fa525ab5aad0226887d02ae8e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036459"
---
# <a name="protocol_specific_data-structure"></a>\_Structure de données spécifique au protocole \_

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure de **\_ \_ données spécifique au protocole** contient de la mémoire réservée pour les données spécifiques à un protocole de routage particulier.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Données PSD**
</dt> <dd>

Spécifie un tableau de variables **DWORD** . Cette mémoire est réservée pour les données spécifiques aux protocoles de routage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



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

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_itinéraire IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





