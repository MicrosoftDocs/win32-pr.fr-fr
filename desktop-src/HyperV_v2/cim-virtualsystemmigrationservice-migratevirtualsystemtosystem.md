---
description: Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un système cible.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Méthode MigrateVirtualSystemToSystem de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864574"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Méthode MigrateVirtualSystemToSystem de la \_ classe CIM VirtualSystemMigrationService

Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un système cible.

Description du code de retour :

## <a name="syntax"></a>Syntaxe


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Système d’ordinateur virtuel source à migrer.

</dd> <dt>

*DestinationSystem* \[ dans\]
</dt> <dd>

Le système hôte de destination whereto migrer le système virtuel.

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

*NewComputerSystem* \[ à\]
</dt> <dd>

Référence à une instance de la [**classe \_ CIM CIM**](cim-computersystem.md) représentant le système d’ordinateur virtuel après sa migration.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.



| Code/valeur de retour                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                    | Le système virtuel a été migré.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>                              | Méthode non prise en charge par l’implémentation.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Échec**</dt> <dt>2</dt> </dl>                                     | Échec de la migration du système virtuel pour des raisons non spécifiées.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Délai d’expiration**</dt> <dt>3</dt> </dl>                                    | Délai d’expiration de la migration du système virtuel ; l’état du système virtuel est inconnu.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Paramètre non valide**</dt> <dt>4</dt> </dl>                          | Un ou plusieurs paramètres ne sont pas valides, par exemple, la valeur du paramètre système de destination ne contient pas de chemin d’accès d’objet valide.<br/>                                                                                                                                                    |
| <dl> <dt>**État non valide**</dt> <dt>5</dt> </dl>                              | Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.<br/>                                                                                             |
| <dl> <dt>**Paramètres incompatibles**</dt> <dt>6</dt> </dl>                    | Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible. Par exemple, la valeur du paramètre *MigrationNewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationSystem* .<br/> |
| <dl> <dt>**DMTF réservé**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

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

 

 




