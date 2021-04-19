---
description: Définit les informations à interroger à partir d’un certificat.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Énumération CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528503"
---
# <a name="capicom_cert_info_type-enumeration"></a>\_ \_ Énumération du type d’informations de certificat CAPICOM \_

Le type d’énumération de **\_ \_ \_ type** d’informations de certificat CAPICOM définit les informations qui doivent être interrogées à partir d’un certificat.

## <a name="members"></a>Membres



| Membre                                         | Description                                                                                  | Valeur |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **\_ \_ \_ \_ \_ nom simple de l’objet du certificat CAPICOM** | Retourne le nom complet de l’objet du certificat.<br/>                              | 0     |
| **\_ \_ \_ \_ \_ nom simple de l’émetteur d’informations de certificat CAPICOM**  | Retourne le nom complet de l’émetteur du certificat.<br/>                        | 1     |
| **nom du message de l’objet de l' \_ information du certificat CAPICOM \_ \_ \_ \_**  | Retourne l’adresse de messagerie de l’objet du certificat.<br/>                             | 2     |
| **nom de messagerie de l' \_ émetteur du certificat CAPICOM \_ info \_ \_ \_**   | Retourne l’adresse de messagerie de l’émetteur du certificat.<br/>                       | 3     |
| **UPN de l' \_ \_ objet d’informations de certificat CAPICOM \_ \_**          | Retourne l’UPN de l’objet du certificat. Introduit dans CAPICOM 2,0.<br/>            | 4     |
| **UPN de l' \_ \_ émetteur des informations de certificat CAPICOM \_ \_**           | Retourne l’UPN de l’émetteur du certificat. Introduit dans CAPICOM 2,0.<br/>      | 5     |
| **\_ \_ \_ \_ \_ nom DNS de l’objet du certificat CAPICOM**    | Retourne le nom DNS de l’objet du certificat. Introduit dans CAPICOM 2,0.<br/>       | 6     |
| **\_ \_ \_ \_ nom DNS de l’émetteur CAPICOM informations CERT \_**     | Retourne le nom DNS de l’émetteur du certificat. Introduit dans CAPICOM 2,0.<br/> | 7     |



## <a name="remarks"></a>Notes

Le type d’énumération de **\_ type d' \_ informations \_ de certificat CAPICOM** est utilisé par la méthode [**Certificate. GetInfo**](certificate-getinfo.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




