---
title: Configuration de l’environnement
description: Le kit de développement logiciel (SDK) de plateforme installé fournit un fichier Setenv.bat situé dans le répertoire racine du kit de développement logiciel (SDK) de plateforme que vous pouvez exécuter pour configurer votre environnement en vue de créer des applications qui utilisent le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509998"
---
# <a name="environment-setup"></a><span data-ttu-id="dcf18-103">Configuration de l’environnement</span><span class="sxs-lookup"><span data-stu-id="dcf18-103">Environment Setup</span></span>

<span data-ttu-id="dcf18-104">Le kit de développement logiciel (SDK) de plateforme installé fournit un fichier Setenv.bat situé dans le répertoire racine du kit de développement logiciel (SDK) de plateforme que vous pouvez exécuter pour configurer votre environnement en vue de créer des applications qui utilisent le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="dcf18-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="dcf18-105">Paramètres et variables</span><span class="sxs-lookup"><span data-stu-id="dcf18-105">Settings and Variables</span></span>

<span data-ttu-id="dcf18-106">Vous pouvez également configurer manuellement votre environnement en ajoutant ce qui suit à votre fichier Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="dcf18-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="dcf18-107">À l’aide de Windows, vous pouvez modifier le fichier Autoexec.bat pour inclure ces commandes.</span><span class="sxs-lookup"><span data-stu-id="dcf18-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="dcf18-108">À l’aide de Windows Server 2003, Windows XP, Windows 2000 ou Windows NT, vous pouvez modifier ou ajouter ces paramètres à vos variables d’environnement à l’aide de la boîte de dialogue système que vous pouvez exécuter à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="dcf18-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="dcf18-109">Ces paramètres conviennent pour une plateforme Intel 80386 ou ultérieure exécutant Windows Me, Windows 98 ou Windows 95 avec Microsoft Visual C++ et le kit de développement logiciel (SDK) de plateforme installé.</span><span class="sxs-lookup"><span data-stu-id="dcf18-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="dcf18-110">Par exemple, sur ce système, Visual C++ version 5,0 est installée sous le répertoire C : \\ msdev.</span><span class="sxs-lookup"><span data-stu-id="dcf18-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="dcf18-111">Le kit de développement Platform SDK est installé sous le répertoire D : \\ MSSDK</span><span class="sxs-lookup"><span data-stu-id="dcf18-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="dcf18-112">La configuration de votre disque peut être différente.</span><span class="sxs-lookup"><span data-stu-id="dcf18-112">Your disk configuration may be different.</span></span> <span data-ttu-id="dcf18-113">Les répertoires du kit de développement Platform SDK (pour cet exemple, ceux avec D : \\ MSSDK dans ceux-ci) sont tous antérieurs dans chaque séquence de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dcf18-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="dcf18-114">Cette séquence suppose que les compilations de ligne de commande sont destinées à être exécutées dans la fenêtre d’invite de commandes et que les fichiers de bibliothèque include et. lib dans le kit de développement Platform SDK sont préférés pour ces compilations.</span><span class="sxs-lookup"><span data-stu-id="dcf18-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="dcf18-115">La variable d’environnement UC est définie pour contrôler les builds Win32, en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="dcf18-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="dcf18-116">Les valeurs possibles actuelles sont i386, MIPS, ALPHA et PPC.</span><span class="sxs-lookup"><span data-stu-id="dcf18-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="dcf18-117">Pour plus d’informations, consultez le fichier Win32. mak fourni dans le kit de développement logiciel (SDK) de plateforme dans le \\ \\ répertoire include MSSDK.</span><span class="sxs-lookup"><span data-stu-id="dcf18-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="dcf18-118">Tous les exemples de fichiers de code du didacticiel COM incluent Win32. mak.</span><span class="sxs-lookup"><span data-stu-id="dcf18-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




