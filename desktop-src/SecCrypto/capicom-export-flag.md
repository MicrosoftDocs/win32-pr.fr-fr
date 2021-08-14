---
description: Le \_ \_ type d’énumération de l’indicateur d’exportation CAPICOM définit si les erreurs d’exportation de clé privée sont ignorées.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Énumération CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772464"
---
# <a name="capicom_export_flag-enumeration"></a>\_Énumération de l’indicateur d’exportation CAPICOM \_

Le type d’énumération de l' **\_ \_ indicateur d’exportation CAPICOM** définit si les erreurs d’exportation de clé privée sont ignorées.

## <a name="members"></a>Membres



| Membre                                                            | Description                                               | Valeur |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **\_ \_ valeur par défaut d’exportation CAPICOM**                                      | Les erreurs d’exportation de clé privée ne sont pas ignorées.<br/> | 0     |
| **\_erreur Impossible d’exporter \_ la \_ \_ clé privée \_ \_ d’exportation \_ CAPICOM** | Toute erreur d’exportation de clé privée est ignorée.<br/>     | 1     |



## <a name="remarks"></a>Remarques

Le \_ \_ type d’énumération de l’indicateur d’exportation CAPICOM est utilisé par la méthode suivante :

-   [**Certificats. Save**](certificates-save.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




