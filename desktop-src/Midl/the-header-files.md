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
# <a name="the-header-files"></a><span data-ttu-id="7b53d-104">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7b53d-104">The Header Files</span></span>

<span data-ttu-id="7b53d-105">Le fichier d’en-tête d’interface (Name. h) contient des définitions de type et des déclarations de fonction basées sur la définition d’interface dans le fichier IDL actuel, ainsi que sur tous les types de données et opérations déclarés dans les fichiers inclus avec la \# directive include.</span><span class="sxs-lookup"><span data-stu-id="7b53d-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="7b53d-106">Les types de données des fichiers importés avec la directive import ne sont pas répliqués dans le fichier d’en-tête. au lieu de cela, le fichier d’en-tête généré contient une ligne include dans le fichier H généré à partir du fichier importé.</span><span class="sxs-lookup"><span data-stu-id="7b53d-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="7b53d-107">Incluez ce fichier dans les fichiers sources de la DLL du proxy et pour les applications clientes qui utilisent l’interface.</span><span class="sxs-lookup"><span data-stu-id="7b53d-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="7b53d-108">Le nom par défaut d’un fichier d’en-tête généré à partir d’un fichier. idl est file. h.</span><span class="sxs-lookup"><span data-stu-id="7b53d-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="7b53d-109">Le commutateur du compilateur [**/header**](-header.md) MIDL remplace le nom par défaut du fichier d’en-tête d’interface.</span><span class="sxs-lookup"><span data-stu-id="7b53d-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




