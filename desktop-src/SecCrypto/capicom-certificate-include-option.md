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
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534766"
---
# <a name="capicom_certificate_include_option-enumeration"></a>Le certificat CAPICOM \_ \_ inclut l' \_ énumération des options

Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** définit les certificats d’une chaîne qui sont enregistrés. Ce type d’énumération a été introduit dans CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                                 | Description                                                                           | Valeur |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine** | Enregistre tous les certificats de la chaîne à l’exception de l’entité racine.<br/> | 0     |
| **le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**        | Enregistre la totalité de la chaîne de certificats.<br/>                                      | 1     |
| **le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**   | Enregistre uniquement le certificat d’entité finale.<br/>                                     | 2     |



## <a name="remarks"></a>Notes

Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** est utilisé par la méthode [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




