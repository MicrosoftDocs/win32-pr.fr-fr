---
description: La table ServiceControl est utilisée pour contrôler les services installés ou désinstallés. Notez que les services qui s’appuient sur la présence d’un assembly dans le global assembly cache (GAC) ne peuvent pas être installés ou démarrés à l’aide des tables ServiceInstall et ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Table ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0c360991ce4a72698ac1b667d82a98ba64b7a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885690"
---
# <a name="servicecontrol-table"></a>Table ServiceControl

La table ServiceControl est utilisée pour contrôler les services installés ou désinstallés.

> [!Note]  
> Les services qui s’appuient sur la présence d’un [assembly](assemblies.md) dans le global assembly cache (GAC) ne peuvent pas être installés ou démarrés à l’aide des tables [ServiceInstall](serviceinstall-table.md) et ServiceControl. Si vous avez besoin de démarrer un service qui dépend d’un assembly dans le GAC, vous devez utiliser une séquence d’action personnalisée après l' [action InstallFinalize](installfinalize-action.md) ou une [action personnalisée de validation](commit-custom-actions.md). Pour plus d’informations sur l’installation d’assemblys dans le GAC, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md).

 

La table ServiceControl contient les colonnes suivantes.



| Colonne         | Type                         | Clé : | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identificateur](identifier.md) | O   | N        |
| Nom           | [Correct](formatted.md)   | N   | N        |
| Événement          | [Integer](integer.md)       | N   | N        |
| Arguments      | [Correct](formatted.md)   | N   | O        |
| Wait           | [Integer](integer.md)       | N   | O        |
| Composant\_    | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Il s’agit de la clé primaire de cette table.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Cette colonne est la chaîne qui nomme le service. Cette colonne peut être utilisée pour contrôler un service qui n’est pas installé.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement
</dt> <dd>

Cette colonne contient les opérations à effectuer sur le service nommé. Notez que lors de l’arrêt d’un service, tous les services qui dépendent de ce service sont également arrêtés. Lors de la suppression d’un service en cours d’exécution, le programme d’installation arrête le service.

Les valeurs de ce champ sont des champs de bits qui peuvent être combinés en une valeur unique qui représente plusieurs opérations.

Les valeurs suivantes sont utilisées uniquement durant une installation.



| Constante                           | Valeur hexadécimale | Decimal | Description                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Démarre le service pendant l' [action StartServices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Arrête le service pendant l' [action StopServices](stopservices-action.md).       |
| (aucun)                             | 0x004       | 4       | &lt;réservé&gt;                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Supprime le service pendant l' [action DeleteServices](deleteservices-action.md). |



 

Les valeurs suivantes sont utilisées uniquement pendant une désinstallation.



| Constante                                    | Valeur hexadécimale | Decimal | Description                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Démarre le service pendant l' [action StartServices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Arrête le service pendant l' [action StopServices](stopservices-action.md).       |
| (aucun)                                      | 0x040       | 64      | &lt;réservé&gt;                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Supprime le service pendant l' [action DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments
</dt> <dd>

Liste d’arguments pour démarrer les services. Les arguments sont séparés par des caractères null \[ ~ \] . Par exemple, la liste des arguments un, deux et trois sont répertoriées comme suit : un \[ ~ \] deux \[ ~ \] trois.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Qu'
</dt> <dd>

Si vous laissez ce champ null ou si vous entrez une valeur de 1, le programme d’installation attend un maximum de 30 secondes avant que le service ne se termine. L’attente peut être utilisée pour permettre à un événement critique de renvoyer une erreur d’échec. La valeur 0 dans ce champ signifie d’attendre uniquement jusqu’à ce que le gestionnaire de contrôle des services (SCM) signale que ce service est en état d’attente avant de poursuivre l’installation.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe vers la colonne de l’une des [tables de composants](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Les actions [StartServices](startservices-action.md), [StopServices](stopservices-action.md)et [DeleteServices](deleteservices-action.md) dans les [*tables de séquences*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

Utilisez la colonne nom pour démarrer, arrêter ou supprimer des services qui sont remplacés par l’installation ou qui dépendent d’un nouveau service en cours d’installation. Par exemple, l’entrée de MyService dans la colonne ServiceControl peut lier ce service à MyComponent dans la \_ colonne Component. Si le champ de bits de la colonne d’événement est défini pour démarrer lors de l’installation de, le programme d’installation démarre MyService lors de l’installation de MonComposant.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



