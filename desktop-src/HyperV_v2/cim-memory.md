---
description: Représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cdf896f03979770d31cdfcc5da7a2b324caf9936bb96114a2d1657e4b5a47e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695299"
---
# <a name="cim_memory-class-hyper-v-management"></a>Classe CIM_Memory (gestion Hyper-V)

Représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>Membres

La classe de **\_ mémoire CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ mémoire CIM** possède ces propriétés.

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,18 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,13 ")
</dt> </dl>

Tableau d’octets qui contient des informations supplémentaires sur l’erreur. Par exemple, le syndrome ECC ou le retour des bits de vérification si une méthodologie d’erreur basée sur CRC est utilisée. Dans ce dernier cas, si une erreur de bit unique est reconnue et que l’algorithme CRC est connu, il est possible de déterminer le bit exact qui a échoué.

Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,8 ")
</dt> </dl>

**true** si l’erreur la plus récente est correcte ; Sinon, **false**. Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,4 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,5 "), **punitif** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Adresse de fin référencée par une application ou un système d’exploitation, et mappée par un contrôleur de mémoire pour l’objet mémoire. L’adresse de fin est spécifiée en kilo-octets.

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,10 ")
</dt> </dl>

Opération d’accès mémoire qui a provoqué la dernière erreur. Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lecture** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Écriture** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Écriture partielle** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. de l’unités de"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,19 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,14 ")
</dt> </dl>

Adresse de la dernière erreur de mémoire. Le type d’erreur est décrit par la propriété **errorInfo** . Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**Partagefichiers**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,12 ")
</dt> </dl>

Tableau qui contient les données capturées au cours du dernier accès mémoire erroné. Les données occupent les n premiers octets du tableau nécessaire pour contenir le nombre de bits spécifié par la propriété **ErrorTransferSize** .

Si la propriété **ErrorTransferSize** contient « 0 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")
</dt> </dl>

Classement des données stockées dans la propriété **ErrorData** . Vous pouvez spécifier « octet le moins significatif en premier » (valeur = 1) ou « octet le plus significatif en premier » (2). Si la propriété **ErrorTransferSize** contient « 0 » (OK), cette propriété n’est pas utilisée.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Octet le moins significatif en premier** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Octet le plus significatif en premier** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,12 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ mémoire CIM**.**OtherErrorDescription**")
</dt> </dl>

Type de la dernière erreur à se produire.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Lecture incorrecte** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Erreur de parité** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Erreur de bit unique** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Erreur double bit** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Erreur multibits** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Erreur de grignotage** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Erreur de somme de contrôle** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Erreur CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Non défini** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Non défini** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Non défini** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,7 ")
</dt> </dl>

Indique si les algorithmes de parité, les algorithmes CRC, l’ECC ou d’autres mécanismes sont utilisés par l’objet mémoire. Vous pouvez également fournir des détails sur l’algorithme.

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphérique de mémoire DMTF \| 005,21 "," MIF. \|Groupe de mémoires physiques DMTF \| 001,15 "), **punitif** (" Byte ")
</dt> </dl>

Plage, en octets, dans laquelle la dernière erreur peut être résolue. Par exemple, si les adresses d’erreur sont résolues en bit 11, par exemple sur une base de page par défaut ; Ensuite, les erreurs peuvent être résolues en limites de 4 Ko, et cette propriété est définie sur « 4000 ». Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")
</dt> </dl>

Heure à laquelle la dernière erreur de mémoire s’est produite. Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de mémoires physiques DMTF \| 001,11 "), **punitif** (" bit ")
</dt> </dl>

Taille du transfert de données, en bits, à l’origine de la dernière erreur. « 0 » n’indique aucune erreur. Si la propriété **errorInfo** contient « 3 » (OK), cette propriété n’est pas utilisée.

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ mémoire CIM**.**ErrorInfo**»)
</dt> </dl>

Description du type d’erreur, lorsque la propriété **ErrorType** est définie sur « 1 » (other).

</dd> <dt>

**De la**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilo-octets"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Le \| groupe de mémoires DMTF mappe \| des adresses 001,3 "," MIF. \|Adresses mappées du périphérique de mémoire DMTF \| 001,4 "), **punitif** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Adresse de départ référencée par une application ou un système d’exploitation, et mappée par un contrôleur de mémoire pour l’objet mémoire. L’adresse de départ est spécifiée en kilo-octets.

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")
</dt> </dl>

**true** si les informations d’adresse dans la propriété **ErrorAddress** sont une adresse de niveau système, **false** s’il s’agit d’une adresse physique.

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si la mémoire est volatile ; Sinon, **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> </dl>

 

