---
description: Contrôle de l’instance du collecteur. Requiert les privilèges d’administrateur (BA).
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 2681af7425fd5cacf88375e11e4658e5d4b1a2c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522911"
---
# <a name="control-class"></a>Control (classe)

Contrôle de l’instance du collecteur. Requiert les privilèges d’administrateur (BA).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Membres

La classe **Control** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Control** possède ces méthodes.



| Méthode                                                         | Description                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Contrôler**](control-checkpoint.md)                       | Si la configuration actuelle est un résultat de l’opération d’annulation/de rétablissement/restauration, le marque comme s’il avait été défini explicitement, afin que l’historique conserve l’heure à laquelle il a été défini, et un fichier de sauvegarde sera créé pour celui-ci lors de la prochaine modification de configuration. Si la configuration actuelle a déjà été définie explicitement, n’a aucun effet. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Videz les informations de diagnostic dans le journal.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Arrêtez rapidement le collecteur, en ignorant toutes les données mises en file d’attente.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Purge**](control-flush.md)                                 | Videz les mémoires tampons du redirecteur.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Lire la configuration active du collecteur.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Comparez l’argument à la configuration active du collecteur. Retourne 1 s’ils correspondent, 0 dans le cas contraire.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Retourne la liste des fichiers de configuration de sauvegarde enregistrés qui peuvent être restaurés.<br/>                                                                                                                                                                                                                                                                                  |
| [**Rétablir**](control-redo.md)                                   | Réinitialiser la configuration active du collecteur à partir du fichier de sauvegarde ultérieur (déterminé par la progression à partir de l’horodatage d’origine actuel). Si la configuration a été annulée, cela signifie que la modification n’a pas été effectuée. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde, sélectionné par un horodateur. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Définissez la nouvelle configuration active du collecteur. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                                                                                                                                                                                                                                                                           |
| [**Correct**](control-shutdown.md)                           | Arrêtez le collecteur. Si le collecteur s’exécute en tant que service, l’arrêt du service est la meilleure approche.<br/>                                                                                                                                                                                                                                                     |
| [**Annuler**](control-undo.md)                                   | Restaure la configuration active du collecteur à partir du fichier de sauvegarde précédent (déterminé par le retour à partir de l’horodateur d’origine actuel). Si la configuration a été définie, cela signifie que vous annulez cette modification. Les appels consécutifs sont annulés à la configuration antérieure et antérieure. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Validez un texte de configuration pour l’exactitude sans le définir comme actif. Retourne 1 en cas de réussite, 0 en cas d’erreur.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




