---
title: Constantes du journal des événements Windows (WinEvt. h)
description: 'Le journal des événements Windows définit les constantes suivantes :'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384612"
---
# <a name="windows-event-log-constants"></a>Constantes du journal des événements Windows

Le journal des événements Windows définit les constantes suivantes :

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_masque de \_ type \_ Variant evt**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Masque de bits que vous utilisez pour masquer le bit de tableau du type Variant, afin de pouvoir déterminer le type de données de la valeur variant contenue dans la structure de [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_tableau de \_ type \_ Variant evt**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



Ce bit est défini pour le membre de **type** de la structure de la [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) si le variant contient un pointeur vers un tableau de valeurs, plutôt que la valeur elle-même.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_accès en lecture \_ à evt**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Autorisation de lecture de contrôle d’accès qui permet la lecture d’informations à partir d’un journal des événements.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_accès en écriture \_ à evt**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Autorisation écrire le contrôle d’accès qui permet d’écrire des informations dans un journal des événements.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT- \_ effacer \_ l’accès**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Désactivez l’autorisation de contrôle d’accès qui autorise l’effacement de toutes les informations d’un journal des événements.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ tout \_ accès**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Autorisation de contrôle d’accès All (lire, écrire, effacer et supprimer).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





