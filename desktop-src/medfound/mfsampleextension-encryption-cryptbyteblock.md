---
description: Spécifie la taille de bloc d’octets chiffrés pour le chiffrement de modèle basé sur l’exemple.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Attribut MFSampleExtension_Encryption_CryptByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525705"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>\_Attribut CryptByteBlock de chiffrement MFSampleExtension \_

Spécifie la taille de bloc d’octets chiffrés pour le chiffrement de modèle basé sur l’exemple.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Le nombre d’octets clairs (non chiffrés) dans le bloc de mappage de sous-échantillon est spécifié dans l’attribut [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) . Si l’un de ces attributs n’est pas présent ou a la valeur 0, cela signifie que les exemples de données ne sont pas chiffrés. L’une ou l’autre des deux valeurs doit être différente de zéro, des valeurs positives ou les deux doivent avoir une valeur égale à zéro.

Dans les cas où la source est MP4, la valeur est définie en fonction des valeurs du bloc d' \_ \_ octet de \_ chiffrement par défaut dans la zone suivre le chiffrement (« tenc ») dans l’en-tête MP4. Pour plus d’informations, consultez [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




