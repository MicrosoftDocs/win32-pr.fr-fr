---
description: La table MsiServiceConfigFailureActions répertorie les opérations à exécuter après l’échec d’un service. Les opérations spécifiées dans ce tableau s’exécutent lors du prochain démarrage du système.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Table MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907c0feb2e331c1e19ff4292d11cc58b65340a7543d9af5d0a1ccf23d2e80a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944416"
---
# <a name="msiserviceconfigfailureactions-table"></a>Table MsiServiceConfigFailureActions

La table MsiServiceConfigFailureActions répertorie les opérations à exécuter après l’échec d’un service. Les opérations spécifiées dans ce tableau s’exécutent lors du prochain démarrage du système.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 5,0.

La table MsiServiceConfigFailureActions contient les colonnes suivantes.



| Colonne                         | Type                         | Clé | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificateur](identifier.md) | O   | N        |
| Nom                           | [Correct](formatted.md)   | N   | N        |
| Événement                          | [Integer](integer.md)       | N   | N        |
| ResetPeriod                    | [Integer](integer.md)       | N   | O        |
| RebootMessage                  | [Correct](formatted.md)   | N   | Y        |
| Commande                        | [Correct](formatted.md)   | N   | O        |
| Actions                        | [Text](text.md)             | N   | O        |
| DelayActions                   | [Text](text.md)             | N   | O        |
| Composant\_                    | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Il s’agit de la clé primaire de cette table qui identifie une action d’échec.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne contient le nom d’un service qui fait partie de ce package ou qui est déjà installé.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement
</dt> <dd>

Cette colonne spécifie quand modifier la configuration du service. Les valeurs suivantes sont des champs de bits qui peuvent être combinés pour représenter plusieurs opérations. Toutes les autres valeurs de champ de bits sont ignorées.



| Constante                                         | Description                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Modification au cours de l’installation du composant.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Modification au cours de la désinstallation du composant.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Modification lors de la réinstallation du composant. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

Période de réinitialisation en secondes du nombre d’échecs du service. Le [Gestionnaire de contrôle des services](../services/service-control-manager.md) (SCM) compte le nombre de fois où chaque service a échoué depuis le dernier redémarrage du système. Le nombre est réinitialisé à zéro si le service n’échoue pas pendant la période de réinitialisation. Lorsque le service échoue pour la nième fois, le système effectue l’action spécifiée dans l’élément \[ N-1 \] du tableau spécifié dans le champ actions.

Laissez le champ ResetPeriod vide pour indiquer que le nombre d’échecs ne doit jamais être réinitialisé.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

Message envoyé aux utilisateurs avant le redémarrage de l’ordinateur en réponse à une action de **\_ \_ redémarrage de l’action SC** spécifiée dans la colonne actions. Vous pouvez utiliser une chaîne vide, "", pour envoyer le message actuel inchangé. Vous pouvez utiliser \[ ~ \] la syntaxe du type de données [mis en forme](formatted.md) pour supprimer le message en cours et envoyer aucun message.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Commande
</dt> <dd>

La ligne de commande exécutée par le processus créé par la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en réponse à une action de **\_ commande sc action \_ Run \_** spécifiée dans la colonne actions. Le nouveau processus s’exécute sous le même compte que le service et uniquement si le champ d’action est **\_ \_ \_ commande sc action Run**. Vous pouvez utiliser une chaîne vide, "", pour utiliser la ligne de commande actuelle inchangée. Vous pouvez utiliser \[ ~ \] la syntaxe du type de données [mis en forme](formatted.md) pour supprimer la ligne de commande actuelle et ne pas exécuter d’opération en cas d’échec du service.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Interventions
</dt> <dd>

Ce champ contient un tableau de valeurs entières qui spécifient les actions effectuées par le SCM en cas d’échec du service. Séparez les valeurs dans le tableau par \[ ~ \] . La valeur entière dans le nième élément du tableau spécifie l’action exécutée lorsque le service échoue pour la nième heure. Chaque membre du tableau est l’une des valeurs entières suivantes.



| Constante                                 | Description           |
|------------------------------------------|-----------------------|
| **SC \_ ACTION \_ None** 0<br/>         | Aucune action.            |
| **SC \_ ACTION de \_ redémarrage** 2<br/>       | Redémarrez l'ordinateur. |
| **SC \_ ACTION \_ restart** 1<br/>      | Redémarrez le service.  |
| **SC \_ ACTION \_ exécuter la \_ commande** 3<br/> | Exécutez une commande.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Ce champ contient un tableau de valeurs entières qui spécifient le délai d’attente, en millisecondes, avant l’exécution de l’action spécifiée dans la colonne action. Séparez les valeurs dans le tableau par \[ ~ \] . Le nombre d’éléments dans le tableau DelayActions doit être égal au nombre d’éléments dans le tableau d’actions. Le nième élément du tableau DelayActions spécifie le délai d’exécution du nième élément du tableau d’actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe vers la colonne de l’une des [tables de composants](component-table.md).

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

 

 
