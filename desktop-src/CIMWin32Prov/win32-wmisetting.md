---
description: La \_ classe WMI singleton de WMISetting Win32 contient les paramètres opérationnels du service WMI. cette classe ne peut avoir qu’une seule instance, qui existe toujours pour chaque système Windows et ne peut pas être supprimée. Impossible de créer des instances supplémentaires.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920427"
---
# <a name="win32_wmisetting-class"></a>\_Classe WMISetting Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) singleton de **\_ WMISetting Win32** contient les paramètres opérationnels du service WMI. cette classe ne peut avoir qu’une seule instance, qui existe toujours pour chaque système Windows et ne peut pas être supprimée. Impossible de créer des instances supplémentaires.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ WMISetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ WMISetting** a ces propriétés.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| default namespace »)
</dt> </dl>

Espace de noms de script par défaut. Cette propriété contient l’espace de noms utilisé par les appels de l’API de script pour WMI si aucun n’est spécifié par l’appelant.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** espace de \\  \\  \\  \\ **\| noms par défaut de script** WBEM Microsoft    

Exemple : root \\ cimv2

Pour obtenir un exemple de script qui utilise cette propriété, consultez la section Notes.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| Enable for ASP »)
</dt> </dl>

Si la **valeur est true**, les scripts WMI peuvent être utilisés sur des Pages de Active Server (ASP). cette propriété est valide sur les systèmes qui exécutent des versions non prises en charge de Windows uniquement. pour les systèmes Windows pris en charge, les scripts WMI sont toujours autorisés sur ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM Microsoft WBEM \\ \\ \| AutoRecover" MOF ")
</dt> </dl>

Liste des noms de fichiers MOF complets utilisés pour initialiser ou récupérer l’espace de stockage WMI. La liste détermine l’ordre dans lequel les fichiers MOF sont compilés.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM- \| récupération automatique (MOF** )    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X »)
</dt> </dl>

Non pris en charge.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Ne pas démarrer** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Démarrage automatique** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Démarrer lors du redémarrage** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Sauvegarde voulu**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup intervalle Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Non pris en charge. Au lieu de cela, sauvegardez manuellement le référentiel WMI.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Date et heure de la dernière sauvegarde.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build »)
</dt> </dl>

Informations de version pour le service WMI actuellement installé.

Durée écoulée entre les sauvegardes de la base de données WMI.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ \_** \\  \\  \\ **\| Build WBEM** du logiciel de l’ordinateur local

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Courte description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM le \\ \\ \| Répertoire de référentiel CIMOM »)
</dt> </dl>

Chemin d’accès au répertoire qui contient l’espace de stockage WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| maximum DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")
</dt> </dl>

Taille maximale de l’espace de stockage WMI.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet actuel.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections »)
</dt> </dl>

Non pris en charge.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| « EnableEvents »)
</dt> </dl>

Si la **valeur est true**, le sous-système d’événements WMI doit être activé.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation »)
</dt> </dl>

Si la valeur est **true**, WMI crée un segment de mémoire pré-alloué avec la taille de la valeur **LastStartupHeapPreallocation** lors de l’initialisation de WMI.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Highst Threshold on client Objects »), [**Units**](../wmisdk/standard-qualifiers.md) (« Objects per second »)
</dt> </dl>

Vitesse maximale à laquelle les objets créés par le fournisseur peuvent être remis aux clients. Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI conserve les objets dans les files d’attente avant de les transmettre aux consommateurs. Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur. Si la mémoire détenue par les objets non collectés atteint **LowThresholdOnObjects**, WMI ralentit l’ajout de nouveaux objets dans la file d’attente. Si les événements non collectés continuent à s’accumuler et que la durée maximale de remise des événements dans **MaxWaitOnClientObjects** est atteinte alors que la mémoire utilisée est à la valeur dans **HighThresholdOnClientObjects**, WMI n’accepte aucun autre objet des fournisseurs et retourne la **mémoire WBEM E à la \_ \_ \_ \_ mémoire des** clients.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("Events per sec")
</dt> </dl>

Vitesse maximale à laquelle les événements doivent être remis aux clients. Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI met en file d’attente les événements avant de les transmettre aux consommateurs. Pour plus d’efficacité, les consommateurs doivent collecter les événements à un rythme qui correspond au fournisseur. Si la mémoire détenue par les événements non collectés atteint **LowThresholdOnObjects**, WMI ralentit l’ajout de nouveaux événements dans la file d’attente. Si les événements non collectés continuent à s’accumuler et que la durée maximale de remise des événements dans **MaxWaitOnEvents** est atteinte alors que la mémoire utilisée est à la valeur de **HighThresholdOnEvents**, WMI n’accepte plus d’événements des fournisseurs et retourne la **mémoire WBEM E à la \_ \_ \_ \_ mémoire des** clients.

> [!Note]  
> La limitation est effectuée uniquement pour les consommateurs d’événements permanents, de sorte que les consommateurs temporaires ne doivent pas s’attendre à une limitation lorsque les événements sont sauvegardés dans la file d’attente d’événements internes WMI.

 

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| installation Directory »)
</dt> </dl>

Chemin d’accès au répertoire où le logiciel WMI a été installé. L’emplacement par défaut est \\ system32 \\ WBEM.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ \_** Répertoire d' \\  \\  \\ **\| installation WBEM** du logiciel de l’ordinateur local

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Taille du tas pré-alloué créé par WMI pendant l’initialisation.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory »)
</dt> </dl>

Chemin d’accès au répertoire qui contient l’emplacement des fichiers journaux système WMI.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** répertoire de \\  \\  \\ **\| \| journalisation CIMOM Microsoft WBEM**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging »)
</dt> </dl>

L’activation de la journalisation des événements et le niveau de détail de la journalisation utilisé.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ **\| \| journalisation CIMOM Microsoft WBEM**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Journalisation des erreurs** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Journalisation des erreurs détaillées** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per sec")
</dt> </dl>

Vitesse à laquelle WMI commence à ralentir la création de nouveaux objets créés pour les clients. Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI conserve les objets dans les files d’attente avant de les transmettre aux consommateurs. Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur. Si le taux de demandes d’objets atteint **LowThresholdOnClientObjects**, WMI ralentit progressivement la création de nouveaux objets pour correspondre au taux d’utilisation du client. Ce ralentissement démarre lorsque la vitesse à laquelle les objets sont créés est supérieure à la valeur de cette propriété. Consultez **HighThresholdOnClientObjects**.

Cette propriété reflète la valeur de registre.

**Clé \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("Events per sec")
</dt> </dl>

Vitesse à laquelle WMI commence à ralentir la remise de nouveaux événements. Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI met en file d’attente les événements avant de les transmettre aux consommateurs. Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur. Si la file d’attente augmente le contrôle, les limitations WMI sont ralenties : la remise des événements progressivement pour s’aligner sur le taux du client. Ce ralentissement démarre lorsque la vitesse à laquelle les événements sont générés dépasse la valeur de cette propriété. Consultez **HighThresholdOnEvents**.

> [!Note]  
> La limitation est effectuée uniquement pour les consommateurs d’événements permanents, de sorte que les consommateurs temporaires ne doivent pas s’attendre à une limitation lorsque les événements sont sauvegardés dans la file d’attente d’événements internes WMI.

 

Cette propriété reflète la valeur de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local**- \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file Max size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Taille maximale des fichiers journaux générés par le service WMI.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ \_** \\  \\  \\ **\| \| Taille maximale du fichier journal CIMOM Microsoft WBEM** de l’ordinateur local

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Durée pendant laquelle un objet nouvellement créé attend d’être utilisé par le client avant d’être supprimé et une valeur d’erreur est retournée. Cette propriété interagit avec les propriétés **LowThresholdOnClientObjects** et **HighThresholdOnClientObjects** pour limiter, ralentir, la remise d’objets aux consommateurs lorsque le consommateur reçoit les objets trop lentement.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Durée pendant laquelle un événement envoyé à un client est mis en file d’attente avant d’être supprimé. Cette propriété interacts0 avec **LowThresholdOnEvents** et **HighThresholdOnEvents** pour limiter, ralentir, la remise d’objets aux consommateurs lorsque le consommateur reçoit les objets trop lentement.

Cette propriété reflète la valeur de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait sur événements (MS)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory »)
</dt> </dl>

Chemin d’accès au répertoire des applications qui installent les fichiers MOF dans le référentiel WMI. WMI compile automatiquement tous les fichiers MOF placés dans ce répertoire et, en fonction de sa réussite, déplace le fichier MOF vers un sous-répertoire intitulé Good ou Bad. Si la \# commande [pragma autoautorecover](../wmisdk/pragma-autorecover.md) est incluse, le nom de fichier complet est ajouté à la liste **AutorecoverMofs** utilisée lors de l’initialisation ou de la récupération du référentiel par WMI. La liste détermine l’ordre dans lequel les MOF sont compilés.

Cette propriété reflète la valeur dans la clé de registre.

**HKEY \_ \_Ordinateur local** \\ **logiciel** \\ **Microsoft** \\ **WBEM \| CIMOM \| fichier MOF-répertoire d’installation**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificateur par lequel l’objet actuel est connu.

Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ WMISetting** est dérivée [**du \_ paramètre CIM**](cim-setting.md). Une seule instance de cette classe peut exister sur un ordinateur.

Il peut être très utile de savoir comment WMI est configuré sur un ordinateur pour déboguer des scripts ou résoudre des problèmes liés au service WMI lui-même. Par exemple, de nombreux scripts WMI sont écrits en supposant que \\ la racine cimv2 est l’espace de noms par défaut sur l’ordinateur cible. Par conséquent, les writers de script qui ont besoin d’accéder à une classe dans « root \\ cimv2 » ne parviennent souvent pas à inclure l’espace de noms dans le moniker GetObject, comme illustré dans l’exemple de code suivant :

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Si la racine \\ cimv2 n’est pas l’espace de noms par défaut sur l’ordinateur cible, ce script échouera. Pour éviter ce problème, l’espace de noms racine \\ cimv2 doit être inclus dans le moniker, comme illustré dans l’exemple de code suivant :

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Si l’espace de noms par défaut sur l’ordinateur cible est différent de l’espace de noms utilisé par un script, le script échoue. En plus de cela, l’utilisateur recevra le message d’erreur de type « classe non valide ». En vérité, l’échec n’est pas dû au fait que la classe n’est pas valide mais que la classe est introuvable dans l’espace de noms par défaut. Il s’agit d’un problème difficile à résoudre, car vous devrez peut-être examiner les problèmes potentiels de la classe plutôt que des problèmes avec l’espace de noms (ou, dans le cas contraire, was) spécifié.

Vous pouvez utiliser la classe **Win32 \_ WMISetting** pour déterminer le mode de configuration de WMI sur un ordinateur. Des détails de configuration tels que l’espace de noms par défaut ou le numéro de build WMI peuvent être utiles pour résoudre les problèmes de script. Ces paramètres fournissent également des informations d’administration importantes, telles que la façon dont les erreurs WMI sont journalisées ou même si elles sont enregistrées sur un ordinateur et les fournisseurs WMI qui seront rechargés automatiquement si vous devez reconstruire le référentiel WMI.

## <a name="examples"></a>Exemples

l’exemple de code [Modify WMI Paramètres](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript de la galerie TechNet utilise la classe **Win32 \_ WMISetting** pour configurer l’intervalle de sauvegarde et le niveau de journalisation WMI.

La liste de l’exemple de code VBScript de l' [espace de noms par défaut](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) sur la Galerie TechNet utilise la classe **Win32 \_ WMISetting** pour récupérer et afficher le paramètre WMI « espace de noms par défaut pour les scripts » WMI actuel.

La modification de l’exemple de code VBScript de l' [espace de noms WMI par défaut](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) dans la Galerie TechNet utilise la propriété **ASPScriptDefaultNamespace** pour définir le paramètre WMI « espace de noms par défaut pour les scripts » sur « root \\ cimv2 ».

la [liste de tous les](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) exemples de code wmi Paramètres VBSCript utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste de paramètres WMI configurés sur un ordinateur.

L’exemple de code JavaScript liste des informations sur les [paramètres WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.

L’exemple de code de la [liste des informations de paramètres WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.

L’exemple de code de l’objet de liste de paramètres [WMI](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) REXX utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.

L’exemple de code VBScript suivant montre comment obtenir la version de WMI en cours d’exécution sur l’ordinateur local. « Win32 \_ WMISetting = @ » indique l’instance unique de la classe. Pour plus d’informations, consultez versions de WMI.


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dt>

[Classes de gestion des services WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
