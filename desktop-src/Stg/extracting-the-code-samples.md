---
title: Extraction des exemples de code
description: Bien que les exemples de code soient divisés en une série de leçons du didacticiel, les exemples de regroupements appropriés peuvent être facilement extraits de la collection.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379809"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="3f203-103">Extraction des exemples de code</span><span class="sxs-lookup"><span data-stu-id="3f203-103">Extracting the Code Samples</span></span>

<span data-ttu-id="3f203-104">Bien que les exemples de code soient divisés en une série de leçons du didacticiel, les exemples de regroupements appropriés peuvent être facilement extraits de la collection.</span><span class="sxs-lookup"><span data-stu-id="3f203-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="3f203-105">La plupart des exemples de répertoires individuels sont conçus pour fonctionner conjointement avec au moins un autre répertoire d’exemples.</span><span class="sxs-lookup"><span data-stu-id="3f203-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="3f203-106">Les exemples liés aux composants se composent d’une paire client/serveur, le serveur nécessitant l’utilisation de l’utilitaire REGISTER Sample.</span><span class="sxs-lookup"><span data-stu-id="3f203-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="3f203-107">Voici un résumé des regroupements d’exemples et comment extraire chaque groupe comme une unité qui peut être générée.</span><span class="sxs-lookup"><span data-stu-id="3f203-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="3f203-108">Pour chaque exemple de regroupement, copiez le contenu des répertoires affichés.</span><span class="sxs-lookup"><span data-stu-id="3f203-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="3f203-109">Le \[ \] Répertoire de destination parent indiqué ne requiert aucun contenu de la branche Samples.</span><span class="sxs-lookup"><span data-stu-id="3f203-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="3f203-110">Toutefois, les menus d’aide des exemples en cours d’exécution partent du principe que le didacticiel approprié est utilisé. Les fichiers d’aide HTM se trouvent dans ce \[ Répertoire de destination parent \] .</span><span class="sxs-lookup"><span data-stu-id="3f203-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="3f203-111">Pour l’application Win32 READTUT :</span><span class="sxs-lookup"><span data-stu-id="3f203-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="3f203-112">Pour l’application squelette Win32 EXE :</span><span class="sxs-lookup"><span data-stu-id="3f203-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="3f203-113">Pour la structure de la DLL Win32 :</span><span class="sxs-lookup"><span data-stu-id="3f203-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="3f203-114">Pour obtenir des exemples d’objets COM de base :</span><span class="sxs-lookup"><span data-stu-id="3f203-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="3f203-115">Pour les exemples de client/serveur de composant DLL in-process de base :</span><span class="sxs-lookup"><span data-stu-id="3f203-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="3f203-116">Pour les exemples de client/serveur de composants sous licence :</span><span class="sxs-lookup"><span data-stu-id="3f203-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="3f203-117">Pour les exemples de marshaling standard :</span><span class="sxs-lookup"><span data-stu-id="3f203-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="3f203-118">Pour obtenir des exemples de client/serveur locaux hors processus :</span><span class="sxs-lookup"><span data-stu-id="3f203-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="3f203-119">Pour obtenir des exemples de client/serveur cloisonnés :</span><span class="sxs-lookup"><span data-stu-id="3f203-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="3f203-120">Pour obtenir des exemples de client/serveur DCOM (Distributed COM) :</span><span class="sxs-lookup"><span data-stu-id="3f203-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="3f203-121">Pour obtenir les exemples de client/serveur gratuits :</span><span class="sxs-lookup"><span data-stu-id="3f203-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="3f203-122">Pour obtenir des exemples de client/serveur d’objets COM connectables :</span><span class="sxs-lookup"><span data-stu-id="3f203-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="3f203-123">Pour obtenir des exemples de client/serveur de stockage structuré :</span><span class="sxs-lookup"><span data-stu-id="3f203-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="3f203-124">Pour obtenir des exemples d’objets client/serveur persistants :</span><span class="sxs-lookup"><span data-stu-id="3f203-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="3f203-125">Pour obtenir des exemples de client/serveur de sécurité DCOM :</span><span class="sxs-lookup"><span data-stu-id="3f203-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




