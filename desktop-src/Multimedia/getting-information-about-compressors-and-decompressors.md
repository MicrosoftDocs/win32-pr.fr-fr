---
title: Obtention d’informations sur les compresseurs et les décompresseurs
description: Obtention d’informations sur les compresseurs et les décompresseurs
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Video Compression Manager (VCM), obtention d’informations sur les compresseurs
- VCM (Video Compression Manager), obtention d’informations sur les compresseurs
- ICGetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940009"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="6b669-106">Obtention d’informations sur les compresseurs et les décompresseurs</span><span class="sxs-lookup"><span data-stu-id="6b669-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="6b669-107">Pour obtenir des informations générales sur un compresseur ou un décompresseur, votre application peut utiliser la fonction [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) .</span><span class="sxs-lookup"><span data-stu-id="6b669-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="6b669-108">Cette fonction remplit une structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) avec des informations sur le compresseur ou le décompresseur.</span><span class="sxs-lookup"><span data-stu-id="6b669-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="6b669-109">Votre application doit allouer la mémoire pour la structure **ICINFO** et lui passer un pointeur dans **ICGetInfo**.</span><span class="sxs-lookup"><span data-stu-id="6b669-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="6b669-110">À moins que votre application ne recherche un compresseur ou décompresseur particulier, les indicateurs de la structure **ICINFO** fournissent les informations les plus utiles sur les fonctionnalités d’un compresseur ou d’un décompresseur.</span><span class="sxs-lookup"><span data-stu-id="6b669-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="6b669-111">Pour obtenir la fréquence d’images clé par défaut et la valeur de qualité par défaut d’un compresseur ou d’un décompresseur, votre application peut envoyer les messages [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) et [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (ou utiliser les macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) et [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).</span><span class="sxs-lookup"><span data-stu-id="6b669-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="6b669-112">Pour déterminer le meilleur format d’affichage d’un compresseur ou d’un décompresseur, votre application peut utiliser la fonction [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .</span><span class="sxs-lookup"><span data-stu-id="6b669-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="6b669-113">Pour déterminer si un compresseur ou un décompresseur peut afficher une boîte de dialogue à propos de, envoyez le message [**ICM \_ à propos**](icm-about.md) de (ou utilisez la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ).</span><span class="sxs-lookup"><span data-stu-id="6b669-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="6b669-114">Vous pouvez également afficher la boîte de dialogue à propos d’un compresseur ou d’un décompresseur en envoyant l’ICM \_ à propos du message et en modifiant la valeur du paramètre *wParam* (ou à l’aide de la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).</span><span class="sxs-lookup"><span data-stu-id="6b669-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




