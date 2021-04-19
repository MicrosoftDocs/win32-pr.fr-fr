---
description: Indique une erreur de composant PCI MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Classe MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529201"
---
# <a name="msmcaevent_pcicomponenterror-class"></a>MSMCAEvent \_ PCIComponentError, classe

La classe **MSMCAEvent \_ PCIComponentError** indique une erreur de composant PCI MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ PCIComponentError** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ PCIComponentError** possède les propriétés suivantes.

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

**\_État d' \_ Erreur du COMP PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code d’erreur interne.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_BusNumber d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de bus du composant PCI.

</dd> <dt>

**\_ClassCodeBaseClass d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code de classe de la classe de base du composant PCI.

</dd> <dt>

**\_ClassCodeInterface d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Interface de code de classe du composant PCI.

</dd> <dt>

**\_ClassCodeSubClass d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Classe de code de classe du composant PCI.

</dd> <dt>

**\_ID d' \_ information \_ COMP PCI**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur d’appareil du composant PCI.

</dd> <dt>

**\_DeviceNumber d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro d’appareil du composant PCI.

</dd> <dt>

**\_FunctionNumber d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de fonction du composant PCI.

</dd> <dt>

**\_SegmentNumber d' \_ informations sur la composition PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de segment du composant PCI.

</dd> <dt>

**ID de la \_ COMP PCI \_ \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du fournisseur du composant PCI.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’octets qui contient l’enregistrement d’erreur brut. Nombre d’éléments dans le tableau que spécifie la propriété **Size** .

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



| Valeurs                                                                               | Signification                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>   | L' \_ État d’erreur du COMP PCI \_ \_ est valide.<br/>    |
| <dl> <dt>2 (0X2)</dt> </dl>   | Les \_ informations sur la composition PCI \_ sont valides.<br/>             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Le \_ \_ nombre de mém. PCI COMP \_ est valide.<br/>         |
| <dl> <dt>8 (0x8)</dt> </dl>   | Le \_ \_ nombre d’e/s comp PCI \_ est valide.<br/>          |
| <dl> <dt>16 (0x10)</dt> </dl> | La \_ paire de données regs de la composition PCI \_ \_ \_ est valide.<br/> |



 

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAEvent \_ PCIComponentError** est dérivée de [**WmiEvent**](wmievent.md).

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

 

