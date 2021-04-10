---
title: Structure WINBIO_UNIT_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’une unité biométrique.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- API de Windows Biometric Framework de structure de WINBIO_UNIT_SCHEMA
- API du pointeur de structure PWINBIO_UNIT_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942815"
---
# <a name="winbio_unit_schema-structure"></a>Structure de schéma d' \_ unité WINBIO \_

La structure de **\_ \_ schéma d’unité WINBIO** décrit les fonctionnalités d’une unité biométrique. Elle est utilisée par la fonction [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>Membres

<dl> <dt>

**UnitId**
</dt> <dd>

Valeur qui identifie l’unité biométrique.

</dd> <dt>

**PoolType**
</dt> <dd>

Valeur **ULong** qui spécifie le type de l’unité biométrique. Il peut s’agir de l’une des valeurs suivantes :



| Valeur                                                                                                                                                                            | Signification                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ inconnu**</dt> </dl> | Le type est inconnu.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_système de pool WINBIO \_**</dt> </dl>    | La session se connecte à une collection partagée d’unités biométriques gérée par le fournisseur de services.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**\_pool WINBIO \_ privé**</dt> </dl> | La session se connecte à une collection d’unités biométriques gérées par l’appelant.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Valeur qui spécifie le type de l’unité biométrique. Seule **une \_ \_ empreinte digitale de type WINBIO** est actuellement prise en charge.

</dd> <dt>

**SensorSubType**
</dt> <dd>

Sous-type de capteur défini pour le type biométrique spécifié par le membre **BiometricFactor** . Seuls les types d’empreintes digitales (**\_ \_ empreintes de type WINBIO**) sont actuellement pris en charge. Les sous-types suivants sont actuellement définis pour les empreintes digitales :

-   \_sous-type de capteur WINBIO \_ \_ inconnu
-   \_balayage de \_ sous-type de capteur WINBIO FP \_ \_
-   WINBIO \_ de \_ sous-type de capteur FP \_ \_

</dd> <dt>

**Capabilities**
</dt> <dd>

Masque de réévaluation des fonctionnalités du capteur biométrique. Il peut s’agir d’une **opération or au niveau du** bit des valeurs suivantes :

-   \_capteur de capacité WINBIO \_
-   \_correspondance des fonctionnalités WINBIO \_
-   \_ \_ base de données de capacité WINBIO
-   \_traitement des capacités WINBIO \_
-   \_chiffrement des fonctionnalités WINBIO \_
-   NAVIGATION dans les \_ fonctionnalités WINBIO \_
-   \_indicateur de capacité WINBIO \_
-   \_ \_ capteur virtuel de capacité WINBIO \_
    > [!Note]  
    > La constante de **\_ \_ \_ capteur virtuel de capacité WINBIO** s’applique uniquement à Windows 10 et versions ultérieures.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Valeur de chaîne qui contient l’ID d’appareil. La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.

</dd> <dt>

**Description**
</dt> <dd>

Valeur de chaîne qui contient une description de l’unité biométrique. La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.

</dd> <dt>

**Fabricant**
</dt> <dd>

Valeur de chaîne qui contient le nom du fabricant. La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.

</dd> <dt>

**Modèle**
</dt> <dd>

Valeur de chaîne qui contient le numéro de modèle de l’unité biométrique. La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.

</dd> <dt>

**SerialNumber**
</dt> <dd>

Chaîne Unicode terminée par le caractère **null** qui contient le numéro de série de l’unité biométrique. La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Structure [**de \_ version de WINBIO**](winbio-version.md) qui contient les numéros de version principale et secondaire pour l’unité biométrique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





