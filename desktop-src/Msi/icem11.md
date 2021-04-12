---
description: ICEM11 vérifie qu’un module de fusion configurable répertorie la table ModuleConfiguration et la table ModuleSubstitution dans la table ModuleIgnoreTable du module.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203778"
---
# <a name="icem11"></a>ICEM11

ICEM11 vérifie qu’un module de fusion configurable répertorie la [table ModuleConfiguration](moduleconfiguration-table.md) et la [table ModuleSubstitution](modulesubstitution-table.md) dans la [table ModuleIgnoreTable](moduleignoretable-table.md) du module. Cela permet de s’assurer que les outils de fusion qui ne reconnaissent pas les modules de fusion configurables (inférieurs à la version 2,0) ne copient pas ces tables dans la base de données cible.

Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures. Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Résultats

ICEM11 publie une erreur si le module contient une table ModuleConfiguration ou ModuleSubstitution non listée dans le tableau ModuleIgnoreTable.

## <a name="example"></a>Exemple

ICEM11 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (partiel)



| Nom     | Format | Type   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | Icône        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| Table de charge de travail   | Ligne              | Colonne | Valeur        |
|---------|------------------|--------|--------------|
| Contrôler | Dialog1; Control1 | Texte   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Table de charge de travail               |
|---------------------|
| ModuleConfiguration |



 

Pour corriger cette erreur, vous pouvez inclure les tables ModuleSubstitution et ModuleConfiguration dans la table ModuleIgnoreTable.

## <a name="table-used-during-execution"></a>Table utilisée pendant l’exécution

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



