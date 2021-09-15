---
description: Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions SelfRegModules et SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Spécification de l’ordre d’inscription automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413926"
---
# <a name="specifying-the-order-of-self-registration"></a>Spécification de l’ordre d’inscription automatique

Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions [SelfRegModules](selfregmodules-action.md) et [SelfUnRegModules](selfunregmodules-action.md) . Ces actions inscrivent tous les modules listés dans la [table Selfreg](selfreg-table.md). Le programme d’installation ne s’inscrit pas automatiquement .exe fichiers.

Pour spécifier l’ordre dans lequel le programme d’installation inscrit ou désinscrit des modules, vous devez utiliser deux [actions personnalisées](custom-actions.md) pour chaque module. Une action personnalisée pour DllRegisterServer et une seconde pour DllUnregisterServer. Ces actions personnalisées doivent ensuite être créées dans la [table InstallExecuteSequence](installexecutesequence-table.md) au point de l’ordre où la dll doit être inscrite ou désinscrite.

L’exemple suivant montre comment créer la base de données pour planifier l’inscription automatique d’une DLL à un point particulier dans la séquence d’action.

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ | FileName  | Séquence |
|-------|-------------|-----------|----------|
| mydll | myComponent | Mydll.dll | 13       |



 

[Table des composants](component-table.md) (partielle)



| Composant   | ComponentId | Répertoire\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*GUID*}  | mondossier    | mydll   |



 

[Table de répertoire](directory-table.md)



| Répertoire | Répertoire \_ parent | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| mondossier  | TARGETDIR         | mondossier \| mon dossier |



 

[Table CustomAction](customaction-table.md)



| Action     | Type | Source   | Cible                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | mondossier | « \[ SystemFolder \] msiexec »/y « \[ \# mydll \] » |
| mydllUNREG | 3170 | mondossier | « \[ SystemFolder \] msiexec "/z" \[ \# mydll \] " |



 

[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)



| Action           | Condition         | Séquence |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2 200     |
| mydllUNREG       | $myComponent = 2    | 2201     |
| RemoveFiles      |                   | 3 500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



