---
description: Définit le type d’attribut associé à une signature.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Énumération CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 26562af3716648540843684bf6c7c901174d36ee1bd615a75d3d98094cc61c77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772815"
---
# <a name="capicom_attribute-enumeration"></a>CAPICOM ( \_ énumération d’attribut)

Le type d’énumération d' **\_ attribut CAPICOM** définit le type d’attribut associé à une [*signature*](../secgloss/d-gly.md).

## <a name="members"></a>Membres



| Membre                                                       | Description                                                                | Valeur |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| **\_heure de signature de l' \_ attribut \_ authentifié \_ CAPICOM**         | L’attribut contient l’heure à laquelle la signature a été créée.<br/> | 0     |
| **\_nom du document de l' \_ attribut \_ authentifié \_ CAPICOM**        | L’attribut contient le nom du document signé.<br/>         | 1     |
| **\_Description du document de l' \_ attribut \_ authentifié \_ CAPICOM** | L’attribut contient une description du document signé.<br/>    | 2     |



## <a name="remarks"></a>Remarques

Le type d’énumération d' **\_ attribut CAPICOM** est utilisé par la propriété [**attribute.Name**](attribute-name.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
