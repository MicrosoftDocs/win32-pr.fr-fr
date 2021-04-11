---
description: Cette rubrique décrit comment créer un expert générique fourni avec le kit de développement logiciel (SDK) Moniteur réseau.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Création d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202730"
---
# <a name="building-an-expert"></a><span data-ttu-id="7a88b-103">Création d’un expert</span><span class="sxs-lookup"><span data-stu-id="7a88b-103">Building an Expert</span></span>

<span data-ttu-id="7a88b-104">Cette rubrique décrit comment créer un expert générique fourni avec le kit de développement logiciel (SDK) Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="7a88b-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="7a88b-105">Avant de créer les exemples de code suivants, installez le kit de développement logiciel (SDK) Moniteur réseau et initialisez le fichier MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="7a88b-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="7a88b-106">**Pour créer un expert générique**</span><span class="sxs-lookup"><span data-stu-id="7a88b-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="7a88b-107">Ouvrez une invite de commandes Moniteur réseau et accédez au \\ sous-répertoire experts, par exemple C : \\ Program Files \\ NetMonSDK2 \\ experts.</span><span class="sxs-lookup"><span data-stu-id="7a88b-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="7a88b-108">Tapez **xcopy/e/s/V Blrplate MyExpert**; Ensuite, lorsque vous y êtes invité, tapez **D**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="7a88b-109">Accédez au \\ sous-répertoire MyExpert.</span><span class="sxs-lookup"><span data-stu-id="7a88b-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="7a88b-110">Tapez **ren Blrplate \* . \* MyExpert \* . \***.</span><span class="sxs-lookup"><span data-stu-id="7a88b-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="7a88b-111">Assurez-vous que tous les fichiers sont correctement renommés.</span><span class="sxs-lookup"><span data-stu-id="7a88b-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="7a88b-112">Vérifiez les noms de fichiers en comparant les fichiers dans le \\ \\ sous-répertoire Blrplate experts.</span><span class="sxs-lookup"><span data-stu-id="7a88b-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="7a88b-113">Modifiez le Makefile en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="7a88b-114">Modifiez les deux fichiers. cpp en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="7a88b-115">N’oubliez pas que l’identificateur de la boîte de dialogue dans config. cpp doit être en majuscules (par exemple, **MYEXPERT**).</span><span class="sxs-lookup"><span data-stu-id="7a88b-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="7a88b-116">Modifiez MyExpert. h en remplaçant toutes les occurrences de **Blrplate** par **MyExpert**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="7a88b-117">Modifiez Resrc1. h en renommant **BLRPLATE** en **MYEXPERT**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="7a88b-118">(N’oubliez pas que **MYEXPERT** doit être en majuscules).</span><span class="sxs-lookup"><span data-stu-id="7a88b-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="7a88b-119">Modifiez le fichier MyExpert. RC en renommant la **boîte de dialogue d’IDD \_ BLRPLATE \_ config \_** en **IDD \_ MyExpert \_ config \_ Dialog**.</span><span class="sxs-lookup"><span data-stu-id="7a88b-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="7a88b-120">Tapez **NMAKE** pour générer le fichier dll.</span><span class="sxs-lookup"><span data-stu-id="7a88b-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="7a88b-121">Pour vérifier la build, accédez au \\ sous-répertoire objet vérifiez que le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="7a88b-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="7a88b-122">Pour plus d’informations, consultez Affichage des propriétés d’un [expert dll](viewing-expert-dll-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7a88b-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="7a88b-123">Une fois la génération terminée, vous disposez d’une DLL d’expert que vous pouvez tester et déployer avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="7a88b-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="7a88b-124">Pour plus d’informations sur l’installation d’un expert, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="7a88b-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="7a88b-125">Pour plus d’informations sur le débogage d’un expert, consultez [débogage d’un expert](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="7a88b-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



