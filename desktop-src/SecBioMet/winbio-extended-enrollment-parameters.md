---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS structure (WinBio \_ adapter. h)
description: Contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
- API du pointeur de structure PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095953"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>\_Structure des \_ paramètres d’inscription étendue WINBIO \_

La structure des **\_ \_ \_ paramètres d’inscription étendue WINBIO** contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Taille (en octets) de la structure **des \_ \_ \_ paramètres d’inscription étendue WINBIO** .

</dd> <dt>

**Sous-fait**
</dt> <dd>

L’une des [**\_ \_ constantes de sous-type biométrique WINBIO**](winbio-biometric-subtype-constants.md) qui fournit des informations supplémentaires sur l’inscription.

</dd> </dl>

## <a name="remarks"></a>Notes

le Windows Biometric Framework passe cette structure à la méthode [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) lors d’une opération d’inscription.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ adaptateur. h (include WinBio \_ adapter. h)</dt> </dl> |



 

 





