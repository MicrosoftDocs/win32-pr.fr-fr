---
description: L' \_ énumération des spécifications de clé CAPICOM \_ définit les spécifications de clé.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: Énumération CAPICOM_KEY_SPEC (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 211830b57d37240edf0df97524ef3865ebe600b33e814353f3a0d021b1b0d88c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772444"
---
# <a name="capicom_key_spec-enumeration"></a>\_Énumération des spécifications de clé CAPICOM \_

L’énumération des **\_ \_ spécifications de clé CAPICOM** définit les spécifications de clé.

## <a name="members"></a>Membres



| Membre                              | Description                                                | Valeur |
|-------------------------------------|------------------------------------------------------------|-------|
| **clé d’échange de la \_ spécification de clé CAPICOM \_ \_** | La clé peut être utilisée pour le chiffrement et la signature.<br/> | 1     |
| **SIGNATURE de la \_ spécification de clé CAPICOM \_ \_**   | La clé peut être utilisée uniquement pour la signature.<br/>           | 2     |



## <a name="remarks"></a>Remarques

L’énumération des **\_ \_ spécifications de clé CAPICOM** est utilisée par les propriétés et méthodes suivantes :

-   Propriété [**PrivateKey. KeySpec**](privatekey-keyspec.md) .
-   Méthode [**PrivateKey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




