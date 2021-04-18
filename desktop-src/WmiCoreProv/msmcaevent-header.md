---
description: Représente l’en-tête commun utilisé par toutes les classes MSMCAEvent. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536538"
---
# <a name="msmcaevent_header-class"></a>\_Classe d’en-tête MSMCAEvent

La classe d' **\_ en-tête MSMCAEvent** représente l’en-tête commun utilisé par toutes les [classes MSMCA](msmca-classes.md) . Les fichiers d’en-tête sont utilisés afin que le code C et C++ puisse avoir une structure de données qui décrit l’en-tête commun pour tous les événements. Cette classe est réservée à un usage interne. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a>Membres

La classe d' **\_ en-tête MSMCAEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ en-tête MSMCAEvent** a ces propriétés.

<dl> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’erreurs supplémentaires dans l’enregistrement MCA.

</dd> <dt>

**Pourcentage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

UC qui signale l’erreur. Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.

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

**LogToEventlog**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.

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

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de message du journal des événements. Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.

</dd> </dl>

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

[Classes WMI C++](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

