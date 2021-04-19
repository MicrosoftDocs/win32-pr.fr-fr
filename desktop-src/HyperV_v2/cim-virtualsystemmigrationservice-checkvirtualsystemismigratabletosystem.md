---
description: 'En savoir plus sur : méthode CheckVirtualSystemIsMigratableToSystem de la classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Méthode CheckVirtualSystemIsMigratableToSystem de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544812"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Méthode CheckVirtualSystemIsMigratableToSystem de la \_ classe CIM VirtualSystemMigrationService

Méthode permettant d’effectuer une vérification préalable pour déterminer si un système virtuel est susceptible d’être migré vers un système cible. Cette méthode ne garantit pas qu’une migration suivante échouera toujours, en raison de la disponibilité dynamique des ressources. Description du code de retour :

## <a name="syntax"></a>Syntaxe


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

[**CIM \_ Instance ComputerSystem**](cim-computersystem.md) référençant le système d’ordinateur virtuel source à migrer.

</dd> <dt>

*DestinationSystem* \[ dans\]
</dt> <dd>

[**CIM \_ Instance système**](cim-system.md) référençant le système de destination sur lequel migrer le système virtuel.

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

*IsMigratable* \[ à\]
</dt> <dd>

Résultat de la vérification de la migration indiquant si la migration du système virtuel est réussie ou non.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.



| Code/valeur de retour                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>    | Vérification effectuée ; résultat signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>              | Méthode non prise en charge par l’implémentation. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Échec**</dt> <dt>2</dt> </dl>                     | Échec de la vérification pour des raisons non spécifiées. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Délai d’expiration**</dt> <dt>3</dt> </dl>                    | Le contrôle a expiré. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Paramètre non valide**</dt> <dt>4</dt> </dl>          | Un ou plusieurs paramètres ne sont pas valides. Par exemple, la valeur du paramètre *DestinationSystem* ne comprend pas de chemin d’accès d’objet valide. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                                                                        |
| <dl> <dt>**État non valide**</dt> <dt>5</dt> </dl>              | Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/>                                                                                    |
| <dl> <dt>**Paramètres incompatibles**</dt> <dt>6</dt> </dl>    | Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible. Par exemple, la valeur du paramètre *NewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationSystem* . Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .<br/> |
| <dl> <dt>**DMTF réservé**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

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

 

 




