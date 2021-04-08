---
title: Liaison à la DLL d’accès à distance
description: Si une application est liée de manière statique à la DLL RASAPI32, le chargement de l’application échoue si le service d’accès à distance n’est pas installé.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842553"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="a09a2-103">Liaison à la DLL d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="a09a2-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="a09a2-104">Si une application est liée de manière statique à la DLL RASAPI32, le chargement de l’application échoue si le service d’accès à distance n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="a09a2-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="a09a2-105">Une application RAS peut se charger lorsque RAS n’est pas installé à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger la dll et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir des pointeurs vers les fonctions RAS.</span><span class="sxs-lookup"><span data-stu-id="a09a2-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="a09a2-106">Les fonctions RAS se trouvent dans RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="a09a2-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="a09a2-107">La bibliothèque d’importation pour ces fonctions est RASAPI32. LIB.</span><span class="sxs-lookup"><span data-stu-id="a09a2-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="a09a2-108">Pour utiliser les fonctions RAS, vos programmes doivent inclure les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="a09a2-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="a09a2-109">Fichier</span><span class="sxs-lookup"><span data-stu-id="a09a2-109">File</span></span>       | <span data-ttu-id="a09a2-110">Description</span><span class="sxs-lookup"><span data-stu-id="a09a2-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a09a2-111">Exécutant. Manutention</span><span class="sxs-lookup"><span data-stu-id="a09a2-111">RAS.H</span></span>      | <span data-ttu-id="a09a2-112">Contient les prototypes de fonction RAS, les constantes et les définitions de structure.</span><span class="sxs-lookup"><span data-stu-id="a09a2-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="a09a2-113">RASERROR. Manutention</span><span class="sxs-lookup"><span data-stu-id="a09a2-113">RASERROR.H</span></span> | <span data-ttu-id="a09a2-114">Contient les codes d’erreur RAS.</span><span class="sxs-lookup"><span data-stu-id="a09a2-114">Contains the RAS error codes.</span></span>                                               |



 

 

 