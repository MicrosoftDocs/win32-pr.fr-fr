---
title: Fichiers d’en-tête
description: Le fichier d’en-tête d’interface (Name. h) contient des définitions de type et des déclarations de fonction basées sur la définition d’interface dans le fichier IDL actuel, ainsi que sur tous les types de données et opérations déclarés dans les fichiers inclus avec la directive \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- fichiers d’en-tête MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543405"
---
# <a name="the-header-files"></a>Fichiers d’en-tête

Le fichier d’en-tête d’interface (Name. h) contient des définitions de type et des déclarations de fonction basées sur la définition d’interface dans le fichier IDL actuel, ainsi que sur tous les types de données et opérations déclarés dans les fichiers inclus avec la \# directive include. Les types de données des fichiers importés avec la directive import ne sont pas répliqués dans le fichier d’en-tête. au lieu de cela, le fichier d’en-tête généré contient une ligne include dans le fichier H généré à partir du fichier importé.

Incluez ce fichier dans les fichiers sources de la DLL du proxy et pour les applications clientes qui utilisent l’interface.

Le nom par défaut d’un fichier d’en-tête généré à partir d’un fichier. idl est file. h. Le commutateur du compilateur [**/header**](-header.md) MIDL remplace le nom par défaut du fichier d’en-tête d’interface.

 

 




