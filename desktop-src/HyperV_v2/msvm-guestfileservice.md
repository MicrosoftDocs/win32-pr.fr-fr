---
description: MSVM \_ GuestFileService contient une méthode qui peut être utilisée pour copier un fichier sur un ordinateur virtuel à partir de l’hôte Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Classe Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa307a55963f6773682e81a08bf7d45e064c9a5bd7213f5d2d426a8d44be70b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789889"
---
# <a name="msvm_guestfileservice-class"></a>MSVM \_ GuestFileService, classe

**MSVM \_ GuestFileService** contient une méthode qui peut être utilisée pour copier un fichier sur un ordinateur virtuel à partir de l’hôte Hyper-V. Cette classe dérive de [**MSVM \_ GuestService**](msvm-guestservice.md).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestFileService** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ GuestFileService** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md) | Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.<br/> **Windows 8.1 :** cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.<br/> |
| **StartService**                                                   | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                     |
| **StopService**                                                    | Cette méthode n'est pas prise en charge.<br/>                                                                                                                                     |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestFileService** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Courte description textuelle de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe ou de la sous-classe utilisée dans la création d’une instance. Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique du service qui fournit également une indication de la fonctionnalité gérée. Pour plus d’informations sur les fonctionnalités, consultez la propriété **Description** de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Démarré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, le service a démarré.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.

Les valeurs sont notamment les suivantes :

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**Automatique**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**Opération**
</dt> </dl>

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État actuel de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Les valeurs sont notamment les suivantes :

<dl><span id="OK"></span><span id="ok"></span><dt>

**OK**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Erreurs**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Détérioré**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Connue**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**« Échec prévu »**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Démarr**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Arrêt**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Services**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Trop sollicité**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**« Non récupéré »**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**« Aucun contact »**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**« Comm. perdue »**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe de création du système d’étendue.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du système qui héberge le service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

