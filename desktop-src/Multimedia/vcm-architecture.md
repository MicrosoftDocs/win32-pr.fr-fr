---
title: Architecture VCM
description: Architecture VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video for Windows (VFW), architecture VCM
- VFW (vidéo pour Windows), architecture VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310569"
---
# <a name="vcm-architecture"></a><span data-ttu-id="0ebe1-105">Architecture VCM</span><span class="sxs-lookup"><span data-stu-id="0ebe1-105">VCM Architecture</span></span>

<span data-ttu-id="0ebe1-106">VCM est un intermédiaire entre une application et les pilotes de compression et de décompression.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="0ebe1-107">Les pilotes de compression et de décompression compressent et décompressent des frames de données individuels.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="0ebe1-108">Lorsqu’une application effectue un appel à VCM, VCM convertit l’appel en message.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="0ebe1-109">Le message est envoyé à l’aide de la fonction [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) vers le compresseur ou décompresseur approprié, qui compresse ou décompresse les données.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="0ebe1-110">VCM reçoit la valeur de retour du pilote de compression ou de décompression, puis renvoie le contrôle à l’application.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="0ebe1-111">Si une macro est définie pour un message, la macro se développe en un appel de fonction **ICSendMessage** fournissant les paramètres appropriés pour ce message.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="0ebe1-112">Si une macro est définie pour un message, votre application doit l’utiliser plutôt que le message.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="0ebe1-113">Dans cette vue d’ensemble, ces macros suivent des messages entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="0ebe1-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




