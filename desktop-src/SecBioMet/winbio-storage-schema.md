---
title: Structure WINBIO_STORAGE_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’un adaptateur de stockage biométrique.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API de Windows Biometric Framework de structure de WINBIO_STORAGE_SCHEMA
- API du pointeur de structure PWINBIO_STORAGE_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510364"
---
# <a name="winbio_storage_schema-structure"></a>Structure du schéma de \_ stockage WINBIO \_

La structure du **\_ \_ schéma de stockage WINBIO** décrit les fonctionnalités d’un adaptateur de stockage biométrique. Cette structure est utilisée par la fonction [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Membres

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Type de mesure biométrique enregistrée dans la base de données.

</dd> <dt>

**DatabaseId**
</dt> <dd>

GUID qui identifie la base de données.

</dd> <dt>

**DataFormat**
</dt> <dd>

GUID qui identifie le format des modèles dans la base de données.

</dd> <dt>

**Attributs**
</dt> <dd>

Informations sur les caractéristiques de la base de données. Il peut s’agir d’une **opération or au niveau du** bit des constantes suivantes.



| Valeur                                                                                                                                                                                                                                                                              | Signification                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Masque d’indicateur de base de données**</dt> <dt>0xFFFF0000</dt> </dl>                | Représente un masque pour les bits d’indicateur.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ Indicateur de base de données 0x00020000 \_ \_ à distance**</dt> <dt></dt> </dl>          | La base de données se trouve sur un ordinateur distant.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ Indicateur de base de données 0x00010000 \_ \_ amovible**</dt> <dt></dt> </dl> | La base de données réside sur un lecteur amovible.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ SGBD**</dt> <dt>0x00000002</dt> </dl>                | La base de données est gérée par un système de gestion de base de données.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Fichier de type base de données**</dt> <dt>0x00000001</dt> </dl>                | La base de données est contenue dans un fichier.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Masque de type de base de données**</dt> <dt>0x0000FFFF</dt> </dl>                | Représente un masque pour le type bits.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | La base de données réside sur le capteur biométrique.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ Smartcard**</dt> <dt>0x00000004</dt> </dl> | La base de données réside sur une carte à puce.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

Le chemin d’accès et le nom de fichier de la base de données si elle réside sur le disque de l’ordinateur.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Valeur de chaîne qui peut être envoyée à un serveur de base de données pour identifier la base de données.

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

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





