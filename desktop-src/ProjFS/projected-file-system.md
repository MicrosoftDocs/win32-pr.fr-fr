---
title: Système de fichiers projeté de Windows
description: Vue d’ensemble du système de fichiers projetés (ProjFS) Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 68f121162efdf75fb9226b41f9b3a1121bef6480
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120584"
---
# <a name="windows-projected-file-system-projfs"></a>Système de fichiers projetés (ProjFS) Windows

Le système de fichiers projeté Windows (ProjFS) permet à une application en mode utilisateur appelée « fournisseur » de projeter des données hiérarchiques à partir d’une banque de données de stockage dans le système de fichiers, en la faisant apparaître en tant que fichiers et répertoires dans le système de fichiers. Par exemple, un fournisseur simple peut projeter le Registre Windows dans le système de fichiers, en faisant en sorte que les clés et les valeurs de Registre apparaissent sous la forme de fichiers et de répertoires, respectivement. Un exemple de fournisseur plus complexe est [VFS pour git](https://github.com/Microsoft/VFSForGit), qui est utilisé pour virtualiser des dépôts Git très volumineux.

> [!NOTE]
> ProjFS est conçu pour être utilisé avec les magasins de données de sauvegarde à haut débit. L’un de ses objectifs de conception est de faire en sorte que les données projetées apparaissent comme si elles étaient présentes localement, masquant ainsi le fait que les données peuvent être distantes. Par conséquent, ProjFS ne fournit pas les mécanismes permettant de signaler la progression du rappel des données ; indication de l’État en ligne et hors connexion d’un fichier ; et d’autres fonctionnalités qui peuvent être souhaitables lorsque vous travaillez avec des magasins de données lents. Pour de tels scénarios, utilisez plutôt l' [API de fichiers Cloud](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                                                       | Description |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Guide de programmation du système de fichiers projetée Windows](projfs-programming-guide.md)                              | Informations conceptuelles sur l’implémentation d’une application de fournisseur ProjFS.
| [Informations de référence sur l’API du système de fichiers projeté Windows](projfs-reference.md)                                          | Informations de référence pour l’interface de programmation ProjFS.
| [Glossaire du système de fichiers projeté de Windows](projfs-glossary.md)                                                | Termes spéciaux utilisés dans ProjFS.

## <a name="additional-resources"></a>Ressources supplémentaires

| Rubrique                                                                                                             | Description                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemple RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Exemple de fournisseur ProjFS qui projette le Registre Windows dans le système de fichiers. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->