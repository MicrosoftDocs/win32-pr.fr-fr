---
description: Le fichier d’en-tête winternl. h expose les prototypes des API Windows internes. Étant donné qu’il n’y a pas de bibliothèque d’importation associée, les développeurs doivent utiliser la liaison dynamique au moment de l’exécution pour appeler les fonctions décrites dans ce fichier d’en-tête.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Appel d’API internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950578"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="663b3-104">Appel d’API internes</span><span class="sxs-lookup"><span data-stu-id="663b3-104">Calling Internal APIs</span></span>

<span data-ttu-id="663b3-105">Le fichier d’en-tête winternl. h expose les prototypes des API Windows internes.</span><span class="sxs-lookup"><span data-stu-id="663b3-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="663b3-106">Étant donné qu’il n’y a pas de bibliothèque d’importation associée, les développeurs doivent utiliser la liaison dynamique au moment de l’exécution pour appeler les fonctions décrites dans ce fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="663b3-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="663b3-107">Les fonctions et structures dans winternl. h sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à l’autre, voire entre les service packs pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="663b3-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="663b3-108">Pour maintenir la compatibilité de votre application, vous devez utiliser à la place les fonctions publiques équivalentes.</span><span class="sxs-lookup"><span data-stu-id="663b3-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="663b3-109">Des informations supplémentaires sont disponibles dans le fichier d’en-tête, winternl. h, ainsi que la documentation de chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="663b3-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="663b3-110">Si vous utilisez ces fonctions, vous pouvez y accéder via la liaison dynamique au moment de l’exécution à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="663b3-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="663b3-111">Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="663b3-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="663b3-112">Toutefois, les modifications de signature peuvent ne pas être détectables.</span><span class="sxs-lookup"><span data-stu-id="663b3-112">Signature changes, however, may not be detectable.</span></span>

 

 
