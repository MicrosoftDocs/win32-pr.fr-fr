---
title: Configuration du compresseur et du décompresseur
description: Configuration du compresseur et du décompresseur
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Gestionnaire de compression vidéo (VCM), configuration des compresseurs
- VCM (gestionnaire de compression vidéo), configuration des compresseurs
- Message ICM_CONFIGURE
- ICQueryConfigure macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939890"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="13b11-107">Configuration du compresseur et du décompresseur</span><span class="sxs-lookup"><span data-stu-id="13b11-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="13b11-108">Votre application peut configurer automatiquement le compresseur ou le décompresseur, ou elle peut permettre à l’utilisateur de les configurer.</span><span class="sxs-lookup"><span data-stu-id="13b11-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="13b11-109">Si cela est possible, autorisez l’utilisateur à configurer le compresseur ou le décompresseur ; Cela vous évite d’avoir à prendre en compte toutes les options pour le compresseur ou le décompresseur.</span><span class="sxs-lookup"><span data-stu-id="13b11-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="13b11-110">L’utilisateur peut configurer le compresseur ou le décompresseur à l’aide d’une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="13b11-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="13b11-111">Vous pouvez envoyer le message de [**\_ configuration ICM**](icm-configure.md) à VCM (ou utiliser la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) pour déterminer si un compresseur ou un décompresseur peut afficher une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="13b11-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="13b11-112">Dans ce cas, envoyez le \_ message de configuration ICM (ou utilisez la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="13b11-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="13b11-113">Votre application peut envoyer les [**messages \_ GETSTATE**](icm-getstate.md) et [**ICM \_ SETSTATE**](icm-setstate.md) (ou utiliser les macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)et [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) pour obtenir et définir l’état d’un compresseur ou d’un décompresseur.</span><span class="sxs-lookup"><span data-stu-id="13b11-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="13b11-114">Si votre application crée ou modifie l’État, elle doit obtenir la disposition des données du compresseur ou du décompresseur avant de restaurer son état.</span><span class="sxs-lookup"><span data-stu-id="13b11-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="13b11-115">En guise d’alternative, si votre application obtient l’État à partir d’un compresseur ou d’un décompresseur et l’utilise pour restaurer l’État dans une session suivante, elle doit s’assurer qu’elle restaure uniquement les informations d’État obtenues à partir du compresseur ou du décompresseur qu’elle utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="13b11-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




