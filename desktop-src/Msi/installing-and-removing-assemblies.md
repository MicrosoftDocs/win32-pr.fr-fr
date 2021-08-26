---
description: Lors de l’installation d’un assembly dans un emplacement isolé pour une application spécifique, l’application doit être spécifiée dans la \_ colonne application de fichier de la table MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installation et suppression d’assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043429"
---
# <a name="installing-and-removing-assemblies"></a>Installation et suppression d’assemblys

Lors de l’installation d’un assembly dans un emplacement isolé pour une application spécifique, l’application doit être spécifiée dans la \_ colonne application de fichier de la [table MsiAssembly](msiassembly-table.md). Ce champ est une clé de la [table de fichiers](file-table.md). Le programme d’installation utilise la structure de répertoires spécifiée dans la [table de répertoires](directory-table.md) pour installer l’assembly dans le même répertoire que le composant qui contient ce fichier.

Lors de l’installation d’un assembly dans le Global Assembly Cache, la valeur dans la \_ colonne application de fichier de la [table MsiAssembly](msiassembly-table.md) doit être null.

Les sections suivantes décrivent l’installation des assemblys Win32 et common language runtime :

-   [Installation d’assemblys Win32](installation-of-win32-assemblies.md)
-   [Installation d’assemblys Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



