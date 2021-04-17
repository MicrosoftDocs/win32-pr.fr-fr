---
description: Indique une erreur MCA (machine Check architecture) spécifique à la plateforme. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: Classe MSMCAEvent_PlatformSpecificError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484912"
---
# <a name="msmcaevent_platformspecificerror-class"></a>MSMCAEvent \_ PlatformSpecificError, classe

La classe **MSMCAEvent \_ PlatformSpecificError** indique une erreur MCA (machine Check architecture) spécifique à la plateforme. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ PlatformSpecificError** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ PlatformSpecificError** possède les propriétés suivantes.

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

Nombre d’erreurs supplémentaires dans l’enregistrement.

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
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Récupérable<br/> |
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

Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.

</dd> <dt>

**\_ID du composant OEM \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique du composant qui signale l’erreur.

</dd> <dt>

**\_ \_ données spécifiques au bus de plateforme \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données propres au bus et spécifiques à l’OEM.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_État d’erreur de la plateforme \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État d’erreur de plateforme générique.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID du demandeur de la plateforme \_ \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du demandeur au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID de répondeur de plateforme \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du répondeur au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID cible de la plateforme \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur cible au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL). Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .

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

**Taille**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de l’enregistrement d’erreur brut.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de message du journal des événements. Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.

</dd> <dt>

**BITS de VALIDATION \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bits de validation utilisés pour indiquer la validité des champs suivants.



| Valeur                                                                                                                                         | Signification                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>          | **Plateforme \_ L' \_ État** de l’erreur est valide.<br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0X2**</dt> </dl>          | **Plateforme \_ L' \_ \_ ID du demandeur d’erreur** est valide.<br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>          | **Plateforme \_ L' \_ \_ ID du répondeur d’erreur** est valide.<br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>          | **Plateforme \_ L' \_ \_ ID cible** de l’erreur est valide.<br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>    | **Plateforme \_ Les \_ \_ données spécifiques** à l’erreur sont valides.<br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>    | **Plateforme \_ L' \_ \_ ID OEM d’erreur** est valide.<br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>    | **Plateforme \_ ERREUR \_ le \_ \_ struct de données OEM** est valide.<br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl> | **Plateforme \_ ERREUR : le \_ \_ \_ chemin d’accès de l’appareil OEM** est valide.<br/> |



 

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAEvent \_ PlatformSpecificError** est dérivée de [**WmiEvent**](wmievent.md).

## <a name="requirements"></a>Configuration requise



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

 

