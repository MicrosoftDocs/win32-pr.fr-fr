---
title: Fichier d’en-tête
description: Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la directive \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL et RPC MIDL, interfaces, fichier d’en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029545"
---
# <a name="the-header-file"></a><span data-ttu-id="f07b4-104">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f07b4-104">The Header File</span></span>

<span data-ttu-id="f07b4-105">Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL, ainsi que tous les types de données et opérations déclarés dans les fichiers inclus avec la \# directive include.</span><span class="sxs-lookup"><span data-stu-id="f07b4-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="f07b4-106">Les types de données des fichiers importés avec la directive import ne sont pas répliqués dans le fichier d’en-tête. au lieu de cela, le fichier d’en-tête généré contient une ligne include dans le fichier H généré à partir du fichier importé.</span><span class="sxs-lookup"><span data-stu-id="f07b4-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="f07b4-107">Le fichier d’en-tête doit être inclus par tous les modules d’application qui appellent les opérations définies, implémentent les opérations définies ou manipulent les types définis.</span><span class="sxs-lookup"><span data-stu-id="f07b4-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="f07b4-108">Le compilateur MIDL bascule [**/header**](-header.md) et [**/out**](-out.md) sur le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f07b4-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




