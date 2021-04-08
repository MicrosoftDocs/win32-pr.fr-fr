---
description: Représente une erreur de bus PCI MCA (machine Check architecture). Cette classe est disponible uniquement pour les ordinateurs qui exécutent un système d’exploitation Windows 64 bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751381"
---
# <a name="msmcaevent_pcibuserror-class"></a>MSMCAEvent \_ PCIBusError, classe

La classe **MSMCAEvent \_ PCIBusError** représente une erreur de bus PCI MCA (machine Check architecture). Cette classe est disponible uniquement pour les ordinateurs qui exécutent un système d’exploitation Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ PCIBusError** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ PCIBusError** possède les propriétés suivantes.

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

**\_adresse du bus PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mémoire ou adresse d’e/s sur le bus PCI au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_cmd bus \_ PCI**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Commande ou opération de bus au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_données de bus PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données sur le bus PCI au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_État d' \_ Erreur du bus PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État du bus au moment de l’erreur.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_type d' \_ erreur de bus PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’erreur de bus PCI.



| Valeur                                                                                                | Signification                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Erreur système inconnue ou spécifique au système OEM.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erreur de parité de données.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Erreur système.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Abandon maître.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Le délai d’expiration du bus ou aucun appareil n’est présent (pas de DEVSEL \# ).<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Erreur de parité des données de référence.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Erreur de parité d’adresse.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Erreur de parité de commande.<br/>                            |



 

</dd> <dt>

**\_ID de bus PCI \_ \_ BusNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur désigné pour le bus PCI qui a rencontré l’erreur.

</dd> <dt>

**\_ID de bus PCI \_ \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de segment désigné pour le bus PCI qui a rencontré l’erreur.

</dd> <dt>

**\_ID du \_ demandeur de bus PCI \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du demandeur de bus PCI au moment de l’événement.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID du \_ répondeur PCI bus \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du répondeur du bus PCI au moment de l’événement.

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



| Valeurs                                                                                  | Signification                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | L' \_ État de l’erreur de bus PCI \_ \_ est valide.<br/>     |
| <dl> <dt>2 (0X2)</dt> </dl>      | Le \_ type d’erreur de bus PCI \_ \_ est valide.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | L' \_ ID de bus PCI \_ est valide.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | L' \_ adresse du bus PCI \_ est valide.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | Les \_ données de bus PCI \_ sont valides.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | La \_ commande de bus PCI \_ est valide.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | L' \_ ID du demandeur de bus PCI \_ \_ est valide.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | L' \_ \_ ID du répondeur PCI bus \_ est valide.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | L' \_ ID cible du bus PCI \_ \_ est valide.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | L' \_ ID OEM du bus PCI \_ \_ est valide.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | Le \_ struct de données OEM du bus PCI \_ \_ \_ est valide.<br/> |



 

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAEvent \_ PCIBusError** est dérivée de [**WmiEvent**](wmievent.md).

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

 

