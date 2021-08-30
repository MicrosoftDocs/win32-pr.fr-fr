---
description: Définit les certificats d’une chaîne qui sont enregistrés.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Énumération CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 5b6bb2cd36d6ce8ca422d680a05a1e84318d745981a8ca15d9de0be3dfe45c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879389"
---
# <a name="capicom_certificate_include_option-enumeration"></a>Le certificat CAPICOM \_ \_ inclut l' \_ énumération des options

Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** définit les certificats d’une chaîne qui sont enregistrés. Ce type d’énumération a été introduit dans CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                                 | Description                                                                           | Valeur |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine** | Enregistre tous les certificats de la chaîne à l’exception de l’entité racine.<br/> | 0     |
| **le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**        | Enregistre la totalité de la chaîne de certificats.<br/>                                      | 1     |
| **le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**   | Enregistre uniquement le certificat d’entité finale.<br/>                                     | 2     |



## <a name="remarks"></a>Remarques

Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** est utilisé par la méthode [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




