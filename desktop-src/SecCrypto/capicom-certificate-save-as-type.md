---
description: Définit le format d’un fichier contenant des informations de certificat.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Énumération CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526090"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_Énumération du certificat \_ CAPICOM \_ en tant que \_ type

Le type d’énumération du **\_ certificat CAPICOM \_ \_ en tant que \_** type définit le format d’un fichier contenant les informations de certificat. Ce type d’énumération a été introduit par CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                  | Description                                                                                                                                   | Valeur |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_certificat CAPICOM \_ enregistré \_ en tant que \_ pfx** | Le fichier de sortie sera formaté en tant que fichier PFX (PKCS 12) et toutes les clés privées associées qui peuvent être exportées seront également enregistrées.<br/> | 0     |
| **\_certificat CAPICOM \_ enregistré \_ comme \_ CER** | Le fichier de sortie sera formaté en tant que fichier CER sans clé privée enregistrée.<br/>                                                        | 1     |



## <a name="remarks"></a>Notes

Le type d’énumération du **\_ certificat CAPICOM \_ \_ en tant que \_** type est utilisé par la méthode [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




