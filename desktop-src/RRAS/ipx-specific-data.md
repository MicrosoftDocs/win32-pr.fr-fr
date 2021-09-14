---
title: Structure de IPX_SPECIFIC_DATA (RTM. h)
description: La \_ structure de \_ données spécifique à IPX contient des données spécifiques à IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013883"
---
# <a name="ipx_specific_data-structure"></a>\_Structure de données spécifique à IPX \_

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure de **\_ \_ données spécifique à IPX** contient des données spécifiques à IPX.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Indicateurs FSD**
</dt> <dd>

Spécifie des indicateurs qui décrivent l’itinéraire. Actuellement, ce membre est soit zéro, soit la valeur d’indicateur suivante.



| Valeur                                                                                                                                                                                                      | Signification                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**\_ \_ itinéraire WAN du client global \_ IPX \_**</dt> </dl> | Spécifie que cet itinéraire est destiné au réseau global alloué pour tous les clients WAN.<br/> |



 

</dd> <dt>

**FSD \_ TickCount**
</dt> <dd>

Spécifie le nombre de cycles nécessaires pour atteindre le réseau de destination. Les protocoles de routage autres que RIP doivent convertir leurs mesures en graduations.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Spécifie le nombre de tronçons associé à l’itinéraire.

</dd> </dl>

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

[**\_itinéraire IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





