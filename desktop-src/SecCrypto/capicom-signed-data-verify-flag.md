---
description: Indique ce qui est vérifié lorsqu’une signature numérique est vérifiée.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Énumération CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324754"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>\_Énumération de l' \_ \_ indicateur de vérification des données signées CAPICOM \_

L’énumération de l' **\_ indicateur de \_ \_ vérification \_ des données signées CAPICOM** indique ce qui est vérifié lorsqu’une [*signature numérique*](../secgloss/d-gly.md) est vérifiée.

## <a name="members"></a>Membres



| Membre                                           | Description                                                                                                 | Valeur |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **\_signature de vérification CAPICOM \_ \_ uniquement**             | Seule la signature est vérifiée.<br/>                                                                   | 0     |
| **\_vérification \_ de la signature et du \_ \_ certificat de CAPICOM** | La signature et la validité du certificat utilisé pour créer la signature sont vérifiées.<br/> | 1     |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
