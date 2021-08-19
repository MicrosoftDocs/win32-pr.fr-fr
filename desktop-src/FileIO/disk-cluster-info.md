---
description: Représente les informations conservées sur le gestionnaire de partition sur un disque qui fait partie d’un cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Structure DISK_CLUSTER_INFO (NTDDDISK. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813791"
---
# <a name="disk_cluster_info-structure"></a>Structure des informations de \_ cluster de disque \_

Représente les informations conservées sur le gestionnaire de partition sur un disque qui fait partie d’un cluster.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Numéro de version. Cette valeur doit être définie sur la taille de cette structure.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Combinaison d’indicateurs liés aux disques et aux clusters.



| Valeur                                                                                                                                                                                                                                                                                               | Signification                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**Disque \_ Indicateur de CLUSTER \_ \_ activé**</dt> <dt>1</dt> </dl>                                          | Le disque est utilisé dans le cadre du service de cluster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**Disque \_ Indicateur de CLUSTER \_ \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Les volumes sur le disque sont exposés par CSVFS sur tous les nœuds du cluster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**Disque \_ \_Indicateur \_ de cluster dans la \_ maintenance**</dt> <dt>4</dt> </dl>                    | La ressource de cluster associée à ce disque est en mode maintenance.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**Disque \_ Indicateur de CLUSTER d' \_ \_ \_ arrivée PNP \_ terminé**</dt> <dt>8</dt> </dl> | Le pilote de disque en cluster pour le mode noyau (ClusDisk) a reçu une notification PnP de l’arrivée du disque.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Indicateurs qui sont modifiés dans le membre **Flags** .

</dd> <dt>

**Notifier**
</dt> <dd>

**True** pour envoyer une notification de modification de la disposition ; Sinon, **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NTDDDISK. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de gestion des disques](disk-management-structures.md)
</dt> <dt>

[**\_informations de \_ cluster d’extraction de disque IOCTL \_ \_**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**\_informations de \_ cluster d’ensemble de disques IOCTL \_ \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




