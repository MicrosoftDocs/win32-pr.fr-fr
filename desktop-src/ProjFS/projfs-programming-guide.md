---
title: Guide de programmation du système de fichiers projeté
description: Informations conceptuelles sur l’implémentation d’une application de fournisseur ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031557"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Guide de programmation du système de fichiers projeté (ProjFS)

Le système de fichiers projeté Windows (ProjFS) permet à une application en mode utilisateur appelée « fournisseur » de projeter des données hiérarchiques dans le système de fichiers, en la faisant apparaître en tant que fichiers et répertoires dans le système de fichiers.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                                                                       | Description |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Vue d’ensemble du fournisseur](provider-overview.md)                                                                   | Vue d’ensemble conceptuelle d’une application de fournisseur.
| [État du cache dans la racine de virtualisation](cache-state.md)                                                    | Décrit les différents États de cache qu’un fichier ou un répertoire géré par le fournisseur peut avoir. 
| [Activation du système de fichiers projetés Windows](enabling-windows-projected-file-system.md)                         | Décrit comment activer le composant facultatif ProjFS.
| [Cycle de vie des instances de virtualisation](virtualization-instance-lifecycle.md)                                   | Vue d’ensemble du cycle de vie d’une instance de virtualisation ProjFS.
| [Énumération de fichiers et de répertoires](enumerating-files-and-directories.md)                                   | Décrit comment un fournisseur ProjFS participe à l’énumération de répertoires.
| [Envoi de données de fichier](providing-file-data.md)                                                               | Décrit comment un fournisseur fournit des informations d’espace réservé et des données de fichier.
| [Notifications d’opérations du système de fichiers](file-system-operation-notifications.md)                               | Décrit comment un fournisseur peut recevoir des notifications d’opérations du système de fichiers.
| [Gestion des modifications d’affichage](handling-view-changes.md)                                                           | Décrit comment mettre à jour la vue client du magasin de stockage d’un fournisseur.
| [Gestion asynchrone des rappels](asynchronous-callback-handling.md)                                         | Décrit comment le fournisseur peut les rappels de service asynchrones.
| [Informations de référence sur l’API du système de fichiers projeté Windows](/windows/desktop/api/_projfs) | Informations de référence pour l’interface de programmation ProjFS.

## <a name="additional-resources"></a>Ressources supplémentaires

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemple RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Exemple de fournisseur ProjFS qui projette le Registre Windows dans le système de fichiers. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->