---
title: Sortie du compilateur MIDL
description: Avec les fichiers IDL et ACF comme entrée, le compilateur MIDL génère jusqu’à cinq fichiers sources en langage C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028844"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="472a6-103">Sortie du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="472a6-103">MIDL Compiler Output</span></span>

<span data-ttu-id="472a6-104">Avec les fichiers IDL et ACF comme entrée, le compilateur MIDL génère jusqu’à cinq fichiers sources en langage C.</span><span class="sxs-lookup"><span data-stu-id="472a6-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="472a6-105">Par défaut, le compilateur MIDL utilise le nom de fichier de base du fichier IDL dans le cadre des fichiers stub générés.</span><span class="sxs-lookup"><span data-stu-id="472a6-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="472a6-106">Lorsque plus de six caractères sont présents dans le nom de fichier de base, certains systèmes de fichiers peuvent ne pas accepter le nom de stub complet.</span><span class="sxs-lookup"><span data-stu-id="472a6-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="472a6-107">Le tableau suivant répertorie les conventions utilisées pour les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="472a6-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="472a6-108">Fichier</span><span class="sxs-lookup"><span data-stu-id="472a6-108">File</span></span>        | <span data-ttu-id="472a6-109">Partie par défaut du nom de fichier de base</span><span class="sxs-lookup"><span data-stu-id="472a6-109">Default portion of base file name</span></span> | <span data-ttu-id="472a6-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="472a6-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="472a6-111">Fichier IDL</span><span class="sxs-lookup"><span data-stu-id="472a6-111">IDL file</span></span>    | ---                               | <span data-ttu-id="472a6-112">ABCDEFGH. idl</span><span class="sxs-lookup"><span data-stu-id="472a6-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="472a6-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="472a6-113">Header</span></span>      | <span data-ttu-id="472a6-114">.h</span><span class="sxs-lookup"><span data-stu-id="472a6-114">.h</span></span>                                | <span data-ttu-id="472a6-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="472a6-115">Abcdef.h</span></span>     |
| <span data-ttu-id="472a6-116">Stub client</span><span class="sxs-lookup"><span data-stu-id="472a6-116">Client stub</span></span> | <span data-ttu-id="472a6-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="472a6-117">\_c.c</span></span>                             | <span data-ttu-id="472a6-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="472a6-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="472a6-119">Stub serveur</span><span class="sxs-lookup"><span data-stu-id="472a6-119">Server stub</span></span> | <span data-ttu-id="472a6-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="472a6-120">\_s.c</span></span>                             | <span data-ttu-id="472a6-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="472a6-121">Abcdef\_s.c</span></span>  |



 

 

 




