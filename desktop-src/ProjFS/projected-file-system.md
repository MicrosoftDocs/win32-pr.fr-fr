---
title: Windows Système de fichiers projeté
description: vue d’ensemble du système de fichiers Windows projeté (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 68f121162efdf75fb9226b41f9b3a1121bef6480
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413641"
---
# <a name="windows-projected-file-system-projfs"></a>Windows Système de fichiers projeté (ProjFS)

le système de fichiers Windows ProjFS permet à une application en mode utilisateur appelée « fournisseur » de projeter des données hiérarchiques à partir d’une banque de données de stockage dans le système de fichiers, en la faisant apparaître en tant que fichiers et répertoires dans le système de fichiers. par exemple, un fournisseur simple peut projeter le registre de Windows dans le système de fichiers, en faisant en sorte que les clés et les valeurs de registre apparaissent en tant que fichiers et répertoires, respectivement. Un exemple de fournisseur plus complexe est [VFS pour git](https://github.com/Microsoft/VFSForGit), qui est utilisé pour virtualiser des dépôts Git très volumineux.

> [!NOTE]
> ProjFS est conçu pour être utilisé avec les magasins de données de sauvegarde à haut débit. L’un de ses objectifs de conception est de faire en sorte que les données projetées apparaissent comme si elles étaient présentes localement, masquant ainsi le fait que les données peuvent être distantes. Par conséquent, ProjFS ne fournit pas les mécanismes permettant de signaler la progression du rappel des données ; indication de l’État en ligne et hors connexion d’un fichier ; et d’autres fonctionnalités qui peuvent être souhaitables lorsque vous travaillez avec des magasins de données lents. Pour de tels scénarios, utilisez plutôt l' [API de fichiers Cloud](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                                                       | Description |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Guide de programmation du système de fichiers projeté](projfs-programming-guide.md)                              | Informations conceptuelles sur l’implémentation d’une application de fournisseur ProjFS.
| [Windows Informations de référence sur l’API du système de fichiers projeté](projfs-reference.md)                                          | Informations de référence pour l’interface de programmation ProjFS.
| [Windows Glossaire du système de fichiers projeté](projfs-glossary.md)                                                | Termes spéciaux utilisés dans ProjFS.

## <a name="additional-resources"></a>Ressources supplémentaires

| Rubrique                                                                                                             | Description                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemple RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | exemple de fournisseur ProjFS qui projette le registre Windows dans le système de fichiers. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->