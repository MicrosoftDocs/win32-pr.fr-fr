---
description: Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: À propos de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514521"
---
# <a name="about-imagehlp"></a><span data-ttu-id="c2c50-103">À propos de ImageHlp</span><span class="sxs-lookup"><span data-stu-id="c2c50-103">About ImageHlp</span></span>

<span data-ttu-id="c2c50-104">Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE.</span><span class="sxs-lookup"><span data-stu-id="c2c50-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="c2c50-105">Toutes les fonctions ImageHlp sont à thread unique.</span><span class="sxs-lookup"><span data-stu-id="c2c50-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="c2c50-106">Par conséquent, les appels à partir de plusieurs threads à cette fonction entraîneront probablement un comportement inattendu ou une altération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c2c50-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="c2c50-107">Pour éviter cela, vous devez synchroniser tous les appels simultanés à partir de plusieurs threads à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c2c50-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="c2c50-108">Les rubriques suivantes décrivent les images PE et les fonctionnalités fournies par les fonctions ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="c2c50-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="c2c50-109">Format PE</span><span class="sxs-lookup"><span data-stu-id="c2c50-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="c2c50-110">Fonctions d’accès aux images</span><span class="sxs-lookup"><span data-stu-id="c2c50-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="c2c50-111">Fonctions d’intégrité de l’image</span><span class="sxs-lookup"><span data-stu-id="c2c50-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="c2c50-112">Fonctions de modification d’image</span><span class="sxs-lookup"><span data-stu-id="c2c50-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



