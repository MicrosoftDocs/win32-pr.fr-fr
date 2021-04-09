---
description: Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Fichiers minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110207"
---
# <a name="minidump-files"></a><span data-ttu-id="8a5e9-103">Fichiers minidump</span><span class="sxs-lookup"><span data-stu-id="8a5e9-103">Minidump Files</span></span>

<span data-ttu-id="8a5e9-104">Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="8a5e9-105">Les applications peuvent créer des fichiers Minidump très rapidement et efficacement.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="8a5e9-106">Étant donné que les fichiers Minidump sont peu volumineux, ils peuvent être facilement envoyés via Internet au support technique de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="8a5e9-107">Un fichier Minidump ne contient pas autant d’informations qu’un fichier de vidage sur incident complet, mais il contient suffisamment d’informations pour effectuer des opérations de débogage de base.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="8a5e9-108">Pour lire un fichier minidump, les fichiers binaires et les fichiers de symboles doivent être disponibles pour le débogueur.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="8a5e9-109">Les versions actuelles de Microsoft Office et Microsoft Windows créent des fichiers minidump pour l’analyse des défaillances sur les ordinateurs des clients.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="8a5e9-110">Les fonctions DbgHelp suivantes sont utilisées avec les fichiers minidump.</span><span class="sxs-lookup"><span data-stu-id="8a5e9-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="8a5e9-111">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="8a5e9-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="8a5e9-112">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="8a5e9-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="8a5e9-113">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="8a5e9-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



