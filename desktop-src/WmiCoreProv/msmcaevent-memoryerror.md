---
description: Représente un événement d’erreur de mémoire MCA (machine Check architecture). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: Classe MSMCAEvent_MemoryError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192211"
---
# <a name="msmcaevent_memoryerror-class"></a>MSMCAEvent \_ MemoryError, classe

La classe **MSMCAEvent \_ MemoryError** représente un événement d’erreur de mémoire MCA (machine Check architecture). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ MemoryError** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ MemoryError** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance de la classe est active ; Sinon, **false**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’erreurs supplémentaires dans l’enregistrement MCA.

</dd> <dt>

**\_données spécifiques au bus \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données propres au bus et spécifiques à l’OEM.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Pourcentage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

UC qui a signalé l’erreur. Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Niveau de gravité de l’erreur signalée.



| Valeur                                                                                                | Signification                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Récupérable<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erreur irrécupérable<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Corrigible<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificateur unique de cette instance de la classe.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la valeur est égale à zéro, cet événement n’est pas consigné dans le journal des événements système.

</dd> <dt>

**Banque de MEM \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Module ou numéro de rang de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**\_position du bit de mémoire \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Position de bit dans le mot de mémoire qui contient l’erreur.

</dd> <dt>

**\_carte mémoire**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de carte de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**MEM ( \_ colonne)**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de colonne de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**\_appareil MEM**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro d’unité de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**État de l’erreur de mémoire \_ \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de l’erreur de mémoire.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_module MEM**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Module ou numéro de classement de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**nœud de MEM \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nœud contenant l’erreur de mémoire. Cette propriété s’applique uniquement à un système à plusieurs nœuds. Cette propriété est spécifique au fournisseur.

</dd> <dt>

**\_ADR physique de mem \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse physique de l’erreur de mémoire.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_masque physique de mémoire \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bits d’adresse valides dans l’adresse physique 64 bits de l’erreur de mémoire.

> [!Note]  
> Le masque physique spécifie la granularité de l’adresse physique. L’adresse physique de l’erreur de mémoire dépend des facteurs d’implémentation matérielle.

 

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**rangée de mém. \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de ligne de l’emplacement de l’erreur de mémoire.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL). Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID du demandeur \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse matérielle de l’appareil ou du composant qui initie la transaction.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID du RÉPONDeur \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse matérielle du répondeur à la transaction.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Taille**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de l’enregistrement d’erreur brut en octets.

</dd> <dt>

**\_ID cible**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse matérielle de la cible prévue de la transaction.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de message du journal des événements. ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.

</dd> <dt>

**BITS de VALIDATION \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bits de validation utilisés pour indiquer la validité des champs suivants.



| Valeurs                                                                                     | Signification                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>         | L’état de l’erreur de mémoire \_ \_ est valide.<br/>                 |
| <dl> <dt>2 (0X2)</dt> </dl>         | L' \_ adresse physique de mem \_ est valide.<br/>                |
| <dl> <dt>4 (0x4)</dt> </dl>         | Le \_ masque d’ADR MEM \_ est valide.<br/>                    |
| <dl> <dt>8 (0x8)</dt> </dl>         | Le \_ nœud de MEM est valide.<br/>                          |
| <dl> <dt>16 (0x10)</dt> </dl>       | La \_ carte mémoire est valide.<br/>                          |
| <dl> <dt>32 (0x20)</dt> </dl>       | Le \_ module MEM est valide.<br/>                        |
| <dl> <dt>64 (0x40)</dt> </dl>       | La \_ Banque de MEM est valide.<br/>                          |
| <dl> <dt>128 (0x80)</dt> </dl>      | L' \_ appareil MEM est valide.<br/>                        |
| <dl> <dt>256 (0x100)</dt> </dl>     | La \_ ligne MEM est valide.<br/>                           |
| <dl> <dt>512 (0x200)</dt> </dl>     | La \_ colonne MEM est valide.<br/>                        |
| <dl> <dt>1024 (0x400)</dt> </dl>    | La \_ position du bit de mémoire \_ est valide.<br/>                 |
| <dl> <dt>2048 (0x800)</dt> </dl>    | L' \_ ID de demande de la plateforme MEM \_ \_ est valide.<br/>       |
| <dl> <dt>4096 (0x1000)</dt> </dl>   | L' \_ ID du répondeur de la plateforme MEM \_ \_ est valide.<br/>       |
| <dl> <dt>8192 (0x2000)</dt> </dl>   | La \_ plateforme \_ cible MEM est valide.<br/>              |
| <dl> <dt>16384 (0x4000)</dt> </dl>  | Les \_ données spécifiques au bus de plateforme mém \_ \_ \_ sont valides.<br/> |
| <dl> <dt>32768 (0x8000)</dt> </dl>  | L' \_ ID OEM de la plateforme MEM \_ \_ est valide.<br/>             |
| <dl> <dt>65536 (0x10000)</dt> </dl> | La \_ structure de données OEM de la plateforme MEM \_ \_ \_ est valide.<br/>   |



 

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAEvent \_ MemoryError** est dérivée de [**WmiEvent**](wmievent.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

