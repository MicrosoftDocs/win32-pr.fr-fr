---
description: Crée un fichier de catalogue non signé, qui contient les hachages d’un ensemble de fichiers, ainsi que les attributs associés de chaque fichier du jeu. Un fichier catalogue permet à l’utilisateur de signer un fichier (le catalogue) au lieu de signer de nombreux fichiers individuels.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Utilisation de MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518573"
---
# <a name="using-makecat"></a><span data-ttu-id="7f013-104">Utilisation de MakeCat</span><span class="sxs-lookup"><span data-stu-id="7f013-104">Using MakeCat</span></span>

<span data-ttu-id="7f013-105">L’outil [MakeCat](makecat.md) crée un fichier catalogue non signé, qui contient les [*hachages*](../secgloss/h-gly.md) d’un ensemble de fichiers, ainsi que les attributs associés de chaque fichier du jeu.</span><span class="sxs-lookup"><span data-stu-id="7f013-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="7f013-106">Un fichier catalogue permet à l’utilisateur de signer un fichier (le catalogue) au lieu de signer de nombreux fichiers individuels.</span><span class="sxs-lookup"><span data-stu-id="7f013-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="7f013-107">Une fois que le fichier de catalogue non signé est signé et transmis, le destinataire peut comparer les hachages des fichiers d’origine avec les hachages contenus dans le fichier catalogue et vérifier que les fichiers ne sont pas falsifiés.</span><span class="sxs-lookup"><span data-stu-id="7f013-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="7f013-108">Avant d’utiliser l’outil [MakeCat](makecat.md) , l’utilisateur doit préparer un fichier de définition de catalogue (. CDF) à l’aide de n’importe quel éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="7f013-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="7f013-109">Le fichier. CDF contient la liste des fichiers et les attributs des fichiers à cataloguer (les spécifications sont répertoriées ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="7f013-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="7f013-110">L’outil MakeCat analyse le fichier. CDF, vérifie la liste des attributs de chaque fichier répertorié, ajoute les attributs répertoriés au catalogue lui-même, hache chacun des fichiers répertoriés et stocke les hachages de chaque fichier dans le fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="7f013-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="7f013-111">Le hachage et les attributs de chaque fichier sont stockés séparément dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="7f013-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="7f013-112">Ce fichier de catalogue peut ensuite être signé et transmis.</span><span class="sxs-lookup"><span data-stu-id="7f013-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="7f013-113">Le destinataire peut ensuite comparer le hachage de chaque fichier au sein du catalogue avec le hachage des fichiers d’origine pour prouver que le contenu d’origine est exempt de falsification.</span><span class="sxs-lookup"><span data-stu-id="7f013-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="7f013-114">MakeCat ne modifie pas le fichier. CDF.</span><span class="sxs-lookup"><span data-stu-id="7f013-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="7f013-115">Les exemples suivants utilisent des commandes [MakeCat](makecat.md) .</span><span class="sxs-lookup"><span data-stu-id="7f013-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="7f013-116">Générez un fichier catalogue à partir du fichier Good. CDF.</span><span class="sxs-lookup"><span data-stu-id="7f013-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="7f013-117">**MakeCat-v Good. CDF**</span><span class="sxs-lookup"><span data-stu-id="7f013-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="7f013-118">Un fichier, Good. CDF, produit un fichier catalogue, Good.cat, en analysant les fichiers UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class et SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="7f013-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="7f013-119">Les fichiers analysés, ainsi que Good. CDF et les Good.cat récemment générés, se trouvent tous dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="7f013-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> <span data-ttu-id="7f013-120">La dernière entrée dans le fichier. CDF doit toujours avoir un caractère de saut de ligne explicite à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="7f013-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
