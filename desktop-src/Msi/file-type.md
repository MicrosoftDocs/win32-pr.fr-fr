---
description: Le type de fichier de type sémantique est l’un des types de format de clé. Ce type se compose d’une clé étrangère dans la table de fichiers fournie par l’utilisateur.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543519"
---
# <a name="file-type"></a>Type de fichier

Le type de fichier de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md). Ce type se compose d’une clé étrangère dans la [table de fichiers](file-table.md) fournie par l’utilisateur.

Le type de fichier peut être utilisé avec les types de ContextData suivants.

**AssemblyContext ContextData**

Ce type peut être utilisé pour permettre aux utilisateurs de configurer des clés étrangères sur des assemblys Win32 ou common language runtime. L’outil de fusion doit substituer un [identificateur](identifier.md) Windows Installer pour les éléments de ce type dans le modèle dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll ne l’applique pas et il revient à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de fichiers.

NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).

 

 



