---
title: L’environnement
description: Les développeurs qui travaillent sur des applications pour Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour Windows 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- environnement de développement 64 programmation Windows bits
- environnement de programmation Windows 64 bits
- Guide de programmation Windows 64 bits sur la programmation Windows 64 bits, environnement de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028879"
---
# <a name="the-environment"></a><span data-ttu-id="87ae4-106">L’environnement</span><span class="sxs-lookup"><span data-stu-id="87ae4-106">The Environment</span></span>

<span data-ttu-id="87ae4-107">Les développeurs qui travaillent sur des applications pour Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87ae4-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="87ae4-108">Les API existantes ont été modifiées, le cas échéant, afin de leur permettre de refléter la précision de la plateforme sur laquelle elles s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="87ae4-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="87ae4-109">Le résultat est la simplicité et une petite courbe d’apprentissage pour le développeur : écrire du code pour Windows 64 bits revient à écrire du code pour Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87ae4-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="87ae4-110">Les fichiers d’en-tête Windows prennent en charge de nouveaux types de données qui permettent aux pointeurs et aux variables associées au pointeur de refléter la précision de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="87ae4-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="87ae4-111">Cela signifie que les développeurs peuvent compiler une base source unique pour une exécution en mode natif sur Windows 32 bits ou Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87ae4-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="87ae4-112">Cette stratégie réduit le coût du développement d’applications qui tirent parti du matériel 64, comme les processeurs AMD Opteron ou Athlon64 ou les processeurs Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="87ae4-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="87ae4-113">Vous aurez plus de temps pour rendre vos applications 64 bits prêtes si vous adoptez les nouvelles conventions de type de données dès que possible.</span><span class="sxs-lookup"><span data-stu-id="87ae4-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="87ae4-114">Si vous modifiez votre code, vous devez modifier les définitions de données en même temps.</span><span class="sxs-lookup"><span data-stu-id="87ae4-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="87ae4-115">Testez l’application sur Windows 32 bits, exécutez-la via le compilateur 64 bits (décrit dans [les outils](the-tools.md)) et l’application sera prête à être testée lorsque vous disposerez du matériel 64 bits approprié.</span><span class="sxs-lookup"><span data-stu-id="87ae4-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




