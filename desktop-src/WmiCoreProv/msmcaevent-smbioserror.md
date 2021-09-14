---
description: Indique une erreur BIOS du système MCA (machine Check architecture). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855610"
---
# <a name="msmcaevent_smbioserror-class"></a>MSMCAEvent \_ SMBIOSError, classe

La classe **MSMCAEvent \_ SMBIOSError** indique une erreur BIOS du système MCA (machine Check architecture). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ SMBIOSError** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ SMBIOSError** possède les propriétés suivantes.

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

Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.

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

**\_type d’événement SMBIOS \_**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d'événement.



| Valeur                                                                                                  | Signification                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl>   | Réservé.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Erreur de mémoire ECC sur un bit.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Erreur de mémoire ECC sur plusieurs bits.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Erreur de mémoire avec parité.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Délai d’expiration du bus.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | Vérification du canal d’e/s.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | Logiciel NMI.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Redimensionnement de la mémoire.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | Erreur de publication.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | Erreur de parité PCI.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | Erreur du système PCI.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | Défaillance du processeur.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | Délai d’expiration du minuteur de basculement EISA.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Journal de mémoire à corriger désactivé.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Journalisation désactivée pour un type d’événement spécifique. Trop d’erreurs du même type reçues dans un laps de temps réduit.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Réservé.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | Limite du système dépassée (par exemple, le seuil de tension ou de température est dépassé).<br/>                                  |
| <span id="17"></span><dl> <dt>**17**</dt> </dl> | La minuterie matérielle asynchrone a expiré et a émis une réinitialisation du système.<br/>                                                   |
| <span id="18"></span><dl> <dt>**19**</dt> </dl> | Informations de configuration du système.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19**</dt> </dl> | Informations sur le disque dur.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | Système reconfiguré.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Erreur de complexité de l’UC non corrigeable.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Réinitialisation ou effacement de la zone de journal.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23/07/03**</dt> </dl> | Démarrage du système. Si elle est implémentée, il est garanti que cette entrée de journal est la première écrite au démarrage du système.<br/>        |



 

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

Bits de validation utilisés pour indiquer la validité des champs suivants. La valeur 1 (0x1) signifie que l' **\_ événement SMBIOS** est valide.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAEvent \_ SMBIOSError** est dérivée de [**WmiEvent**](wmievent.md).

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

 

