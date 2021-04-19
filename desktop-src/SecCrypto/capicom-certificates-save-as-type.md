---
description: Définit le format d’un fichier contenant des informations sur les certificats.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Énumération CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520924"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>L' \_ énumération des certificats CAPICOM \_ \_ en tant que \_ type

Le type d’énumération des **\_ certificats CAPICOM \_ \_ en tant que \_** type définit le format d’un fichier contenant des informations sur les certificats. Ce type d’énumération a été introduit par CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                          | Description                                          | Valeur |
|-------------------------------------------------|------------------------------------------------------|-------|
| **\_certificats CAPICOM \_ enregistrés \_ sous forme \_ sérialisée** | Les certificats enregistrés sont sérialisés.<br/>    | 0     |
| **\_Certificats CAPICOM \_ enregistrés \_ en tant que \_ PKCS7**      | Les certificats sont enregistrés sous la forme d’un fichier PKCS \# 7.<br/> | 1     |
| **\_certificats CAPICOM \_ Enregistrer \_ comme \_ pfx**        | Les certificats sont enregistrés en tant que PFX.<br/>      | 2     |



## <a name="remarks"></a>Notes

Le \_ \_ \_ \_ type d’énumération certificats Save As type est utilisé par la méthode [**Certificates. Save**](certificates-save.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




