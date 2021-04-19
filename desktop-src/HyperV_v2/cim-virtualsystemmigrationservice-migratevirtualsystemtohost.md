---
description: Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Méthode MigrateVirtualSystemToHost de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525026"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>Méthode MigrateVirtualSystemToHost de la \_ classe CIM VirtualSystemMigrationService

Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.

> [!Note]  
> Cette méthode est destinée à une solution transitoire uniquement jusqu’à ce que la modélisation de la prise en charge des clusters soit disponible.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Système d’ordinateur virtuel source à migrer.

</dd> <dt>

*DestinationHost* \[ dans\]
</dt> <dd>

Système hôte cible pour la migration.

Les formats acceptables pour ce paramètre sont transmis via les valeurs des éléments de la propriété de tableau **DestinationHostFormatsSupported** \[ \] dans l’instance du [**\_ VirtualSystemMigrationCapabilities CIM**](cim-virtualsystemmigrationcapabilities.md) qui est associée par le biais de l’Association [**CIM \_ ElementCapabilities**](cim-elementcapabilities.md) .

</dd> <dt>

*MigrationSettingData* \[ dans\]
</dt> <dd>

Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) représentant les paramètres de migration applicables à l’opération de migration.

</dd> <dt>

*NewSystemSettingData* \[ dans\]
</dt> <dd>

Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant les nouvelles propriétés applicables au système virtuel après sa migration.

</dd> <dt>

*NewResourceSettingData* \[ dans\]
</dt> <dd>

Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les nouvelles propriétés applicables aux ressources virtuelles dans l’étendue du système virtuel après la migration.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.



| Code/valeur de retour                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                    | Le système virtuel a été migré.<br/>                                                                                                                                                                                                                                                                  |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>                              | Méthode non prise en charge par l’implémentation.<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Échec**</dt> <dt>2</dt> </dl>                                     | Échec de la migration du système virtuel pour des raisons non spécifiées.<br/>                                                                                                                                                                                                                                      |
| <dl> <dt>**Délai d’expiration**</dt> <dt>3</dt> </dl>                                    | Délai d’expiration de la migration du système virtuel ; l’état du système virtuel est inconnu.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**Paramètre non valide**</dt> <dt>4</dt> </dl>                          | Un ou plusieurs paramètres ne sont pas valides. Par exemple, la valeur du paramètre *DestinationHost* peut avoir été spécifiée dans un format non pris en charge.<br/>                                                                                                                                    |
| <dl> <dt>**État non valide**</dt> <dt>5</dt> </dl>                              | Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.<br/>                                                                                           |
| <dl> <dt>**Paramètres incompatibles**</dt> <dt>6</dt> </dl>                    | Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible. Par exemple, la valeur du paramètre *MigrationNewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationHost* .<br/> |
| <dl> <dt>**DMTF réservé**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




