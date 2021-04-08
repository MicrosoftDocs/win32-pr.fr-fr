---
title: Concepts de base du compresseur et du décompresseur
description: Concepts de base du compresseur et du décompresseur
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Gestionnaire de compression vidéo (VCM), ouverture de compresseurs
- VCM (Video Compression Manager), ouverture de compresseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839937"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="b25c6-105">Concepts de base du compresseur et du décompresseur</span><span class="sxs-lookup"><span data-stu-id="b25c6-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="b25c6-106">Pour ouvrir et localiser un compresseur, vous pouvez utiliser les fonctions [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) et [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) .</span><span class="sxs-lookup"><span data-stu-id="b25c6-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="b25c6-107">Vous pouvez utiliser **ICLocate** pour rechercher un compresseur d’un type spécifique et obtenir un handle de celui-ci en vue de son utilisation dans d’autres fonctions VCM.</span><span class="sxs-lookup"><span data-stu-id="b25c6-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="b25c6-108">Pour ouvrir un compresseur, vous pouvez utiliser **ICOpen**.</span><span class="sxs-lookup"><span data-stu-id="b25c6-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="b25c6-109">Votre application utilise le descripteur retourné par cette fonction pour identifier le compresseur ouvert lorsqu’il utilise d’autres fonctions VCM.</span><span class="sxs-lookup"><span data-stu-id="b25c6-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="b25c6-110">Pour ouvrir et localiser un décompresseur, les applications peuvent utiliser les macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) et [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) .</span><span class="sxs-lookup"><span data-stu-id="b25c6-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="b25c6-111">Ces macros utilisent **ICLocate** pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b25c6-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="b25c6-112">Lorsque votre application a terminé d’utiliser un compresseur ou un décompresseur, elle doit la fermer pour libérer toutes les ressources utilisées pour la compression ou la décompression.</span><span class="sxs-lookup"><span data-stu-id="b25c6-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="b25c6-113">Votre application peut utiliser la fonction [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) pour fermer le compresseur ou le décompresseur.</span><span class="sxs-lookup"><span data-stu-id="b25c6-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="b25c6-114">En outre, votre application peut énumérer les compresseurs ou les décompresseurs sur un système à l’aide de la fonction [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="b25c6-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="b25c6-115">L’en-tête de flux d’un fichier AVI contient des informations sur le type de flux et le gestionnaire spécifique pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="b25c6-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="b25c6-116">Dans l’en-tête de flux, les membres **fccType** et **fccHandler** identifient le type de flux et le gestionnaire de flux spécifiés pour le flux.</span><span class="sxs-lookup"><span data-stu-id="b25c6-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




