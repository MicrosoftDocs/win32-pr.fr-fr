---
description: La table MsiServiceConfig configure un service qui est installé ou en cours d’installation par le package actuel.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Table MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119682"
---
# <a name="msiserviceconfig-table"></a>Table MsiServiceConfig

La table MsiServiceConfig configure un service qui est installé ou en cours d’installation par le package actuel.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 5,0.

La table MsiServiceConfig contient les colonnes suivantes.



| Colonne           | Type                         | Clé | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identificateur](identifier.md) | O   | N        |
| Nom             | [Correct](formatted.md)   | N   | N        |
| Événement            | [Integer](integer.md)       | N   | N        |
| ConfigType       | [Integer](integer.md)       | N   | N        |
| Argument         | [Correct](formatted.md)   | N   | O        |
| Composant\_      | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Il s’agit de la clé primaire de cette table.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne contient le nom d’un service qui fait partie de ce package ou qui est déjà installé.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement
</dt> <dd>

Cette colonne spécifie quand modifier la configuration du service. Les valeurs suivantes peuvent être combinées pour représenter plusieurs opérations. Toutes les valeurs incluses en dehors de celles-ci sont ignorées.



| Constante                                         | Description                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Exécute l’action lors de l’installation du composant.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Exécute l’action pendant la désinstallation du composant. |
| **msidbServiceConfigEventReinstall** 4<br/> | Effectue l’action lors de la réinstallation du composant. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

La valeur de ce champ, associée à la valeur dans le champ arguments, spécifie la modification à apporter à la configuration du service. La modification spécifiée prend effet lors du prochain démarrage du système.



| Config                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Service \_ \_ \_ \_ Démarrage automatique différé** de la configuration 3<br/>       | Configurez le délai d’un [service à démarrage automatique](../services/automatically-starting-services.md). <br/> Entrez 1 dans le champ argument pour démarrer le service après d’autres services à démarrage automatique plus un délai. <br/> Entrez 0 dans le champ argument pour désactiver le délai de service de démarrage automatique.<br/> S’applique uniquement aux services ou services à démarrage automatique installés par ce package avec **le \_ \_ démarrage automatique du service** dans le champ StartType de la [table ServiceInstall](serviceinstall-table.md).<br/>                                                                         |
| **Service \_ \_ \_ \_ Informations sur les privilèges requis** pour la configuration 6<br/> | Modifiez la liste des privilèges requis par le service.<br/> Entrez la liste des privilèges demandés dans le champ argument. La valeur de chaîne [mise en forme](formatted.md) dans le champ argument répertorie les [**constantes de privilège**](../secauthz/privilege-constants.md) pour les privilèges demandés. Vous pouvez utiliser la \[ ~ \] syntaxe de la chaîne [mise en forme](formatted.md) pour insérer un caractère null. Séparez les constantes de privilège de la liste par \[ ~ \] .<br/>                                                                                                                              |
| **Service \_ \_ \_ \_ Informations sid** 5 du service de configuration<br/>         | Ajoutez un type de SID de service au jeton de processus contenant ce service.<br/> Entrez dans le champ argument un type de SID de service valide pour la structure d' [**\_ \_ informations SID du service**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : **type de SID de service \_ \_ \_ None** (0x00), type de SID de service (0x03) ou type de **\_ SID de \_ \_ service** **\_ \_ \_ illimité** (0x01). <br/>                                                                                                                                                                                                                                              |
| **Service \_ \_ \_ Informations de préfermeture de configuration** 7<br/>          | Configurez la durée d’attente du [Gestionnaire de contrôle des services](../services/service-control-manager.md) (SCM) avant de procéder à d’autres opérations d’arrêt. Le SCM attend pendant ce laps de temps après l’envoi de la notification de préversion de **\_ \_ contrôle de service** au service. <br/> Entrez la durée, en millisecondes, dans le champ argument. Laissez le champ argument vide pour réinitialiser le délai à la valeur par défaut de 3 minutes. <br/>                                                                                                                               |
| **Service \_ \_Indicateur des \_ actions \_ d’échec** de la configuration 4<br/>     | Configurez à quel moment exécuter les actions d’échec pour ce service. Ce paramètre est ignoré si le service n’a pas d’action d’échec configurée.<br/> Entrez 0 pour exécuter les actions uniquement si le service se termine sans que Reporting **service soit \_ arrêté**.<br/> Entrez 1 pour exécuter les actions si le service arrête le service de création de rapports et que le membre **dwWin32ExitCode** de la structure d' [**\_ État du service**](/windows/win32/api/winsvc/ns-winsvc-service_status) n’est pas une erreur de **\_ réussite**. **\_** Les actions configurées en cas d’échec sont également exécutées si le service se termine sans que Reporting **services soit \_ arrêté**.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

La valeur de ce champ, associée à la valeur dans le champ ConfigType, spécifiez la modification à apporter à la configuration du service. La modification spécifiée prend effet lors du prochain démarrage du système.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe de la colonne de composant de la [table des composants](component-table.md).

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
