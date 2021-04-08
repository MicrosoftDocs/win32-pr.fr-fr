---
description: Spécifie la taille de bloc d’octets Clear (non chiffrée) pour le chiffrement de modèle basé sur un échantillon.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Attribut MFSampleExtension_Encryption_SkipByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863970"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>\_Attribut SkipByteBlock de chiffrement MFSampleExtension \_

Spécifie la taille de bloc d’octets Clear (non chiffrée) pour le chiffrement de modèle basé sur un échantillon.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Le nombre d’octets chiffrés dans le bloc de mappage de sous-échantillon est spécifié dans l’attribut [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) . Si l’un de ces attributs n’est pas présent ou a la valeur 0, cela signifie que les exemples de données ne sont pas chiffrés. L’une ou l’autre des deux valeurs doit être différente de zéro, des valeurs positives ou les deux doivent avoir une valeur égale à zéro.

Dans les cas où la source est MP4, la valeur est définie en fonction des valeurs de bloc d' \_ octets ignorés par défaut \_ \_ dans la zone suivre le chiffrement (« tenc ») dans l’en-tête MP4. Pour plus d’informations, consultez [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




