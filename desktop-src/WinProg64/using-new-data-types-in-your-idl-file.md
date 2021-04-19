---
title: Utilisation de nouveaux types de données dans votre fichier IDL
description: Le fichier d’en-tête Basetsd. h définit les nouveaux types de données nécessaires pour écrire des applications qui s’exécutent sur des fenêtres 32 et 64 bits.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Fichier d’en-tête Basetsd. h programmation Windows 64 bits
- types de données dans le fichier IDL programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509041"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="ab7ac-105">Utilisation de nouveaux types de données dans votre fichier IDL</span><span class="sxs-lookup"><span data-stu-id="ab7ac-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="ab7ac-106">Le fichier d’en-tête Basetsd. h définit les nouveaux types de données nécessaires pour écrire des applications qui s’exécutent sur des fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="ab7ac-107">Pour utiliser ces types de données dans vos interfaces, importez Basetsd. h dans votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="ab7ac-108">N' \# incluez pas le fichier ou vous obtenez plusieurs définitions au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="ab7ac-109">Vous pouvez également inclure ou importer le fichier Basetsd. idl dans votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="ab7ac-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="ab7ac-110">Pour plus d’informations sur l’ajout de fichiers d’en-tête système à votre fichier IDL, consultez [importation de fichiers et de bibliothèques de types](/windows/desktop/Midl/importing-files-and-type-libraries) et importation de fichiers d' [en-tête système](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="ab7ac-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 