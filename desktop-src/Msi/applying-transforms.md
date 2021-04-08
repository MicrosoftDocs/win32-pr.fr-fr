---
description: La propriété transformations contient la liste des transformations d’un package d’installation. Le programme d’installation applique toutes les transformations de la liste des transformations à chaque installation, publication, installation à la demande ou installation de maintenance du package.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Application de transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864477"
---
# <a name="applying-transforms"></a>Application de transformations

La propriété [**TRANSformations**](transforms.md) contient la liste des transformations d’un package d’installation. Le programme d’installation applique toutes les transformations de la liste des transformations à chaque installation, publication, installation à la demande ou installation de maintenance du package.

La propriété [**TRANSformations**](transforms.md) est définie en spécifiant la liste des transformations sur la ligne de commande ; Toutefois, lorsque vous utilisez l' [option de ligne de commande](command-line-options.md)/JM ou/ju, la liste transformations doit être spécifiée à l’aide de l’option/t.

Notez que la liste transformations ne peut pas être modifiée une fois installée et ne peut être supprimée qu’en désinstallant l’application.

> [!Note]  
> Un package de Windows Installer ne peut pas appliquer plus de 255 transformations lors de l’installation d’une application ou d’une mise à jour. Lorsque de nombreuses transformations sont nécessaires, elles doivent être combinées et les transformations obsolètes antérieures doivent être éliminées.

 

Le tableau suivant fournit des exemples de différentes chaînes de transformation qui peuvent être ajoutées à la liste des transformations.



| Transforme la chaîne                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1. MST ;: transform2. MST ;: transform3. MST                                                                                 | Transform2. MST et transform3. MST sont des [transformations incorporées](embedded-transforms.md). transform1. MST est une [transformation sécurisée à la source](secure-at-source-transforms.md) uniquement si la [**propriété TRANSFORMSSECURE**](transformssecure.md) ou la [stratégie TRANSFORMSSECURE](transformssecure-policy.md) est définie, sinon transform1 est une [transformation non sécurisée](unsecured-transforms.md). |
| \\\\\\ \\ chemin d’accès au partage de serveur \\ transform1. MST ;: transform2. MST                                                                        | Transform2. MST est une [transformation incorporée](embedded-transforms.md). transform1. MST est une [transformation de chemin d’accès complet sécurisé](secure-full-path-transforms.md) uniquement si la propriété [**TRANSFORMSSECURE**](transformssecure.md) ou la [stratégie TRANSFORMSSECURE](transformssecure-policy.md) est définie, sinon transform1 est une [transformation non sécurisée](unsecured-transforms.md).                   |
| @ : transform2. MST ; transform1. MST @transform1.mst ;: transform2. MST<br/>                                                     | Transform2. MST est une transformation incorporée. transform1. MST est une [transformations sécurisée à la source](secure-at-source-transforms.md)autonome.                                                                                                                                                                                                                                                |
| \|\\\\\\ \\ chemin d’accès au partage de serveur \\ transform1. MST ;: transform2. MST \| : transform2. MST ; \\ \\ chemin de partage de serveur \\ \\ \\ transform1. MST<br/> | Transform2. MST est une transformation incorporée. transform1. MST est une [transformation autonome sécurisée-chemin d’accès complet](secure-full-path-transforms.md).                                                                                                                                                                                                                                                 |



 

 

 




