---
title: API serveur DVC
description: Les API de serveur de canal virtuel dynamique (DVC) sont implémentées par le serveur Connexion Bureau à distance (RDC) de la connexion.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382608"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="dd3c2-103">API serveur DVC</span><span class="sxs-lookup"><span data-stu-id="dd3c2-103">DVC Server APIs</span></span>

<span data-ttu-id="dd3c2-104">Les API de serveur de canal virtuel dynamique (DVC) sont implémentées par le serveur Connexion Bureau à distance (RDC) de la connexion.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd3c2-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dd3c2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="dd3c2-106">**IWTSServerChannel**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="dd3c2-107">Cette interface n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="dd3c2-108">**IWTSServerChannelManager**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="dd3c2-109">Cette interface n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="dd3c2-110">**TPriority**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="dd3c2-111">Cette énumération n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="dd3c2-112">Changements de comportement pour d’autres API serveur</span><span class="sxs-lookup"><span data-stu-id="dd3c2-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="dd3c2-113">L’API serveur a été étendue avec un appel supplémentaire qui ouvre un canal virtuel dynamique (DVC).</span><span class="sxs-lookup"><span data-stu-id="dd3c2-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="dd3c2-114">L’appel supplémentaire est effectué à l’aide de la fonction [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .</span><span class="sxs-lookup"><span data-stu-id="dd3c2-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="dd3c2-115">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="dd3c2-116">Lors de l’utilisation de cette API avec DVC, elle ajoutera toujours les données lues avec l' [**\_ \_ en-tête**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)de l’PDU de canal.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="dd3c2-117">Cela signifie que toute lecture doit être effectuée avec au moins le bloc de données de **\_ \_ longueur PDU de canal** passé comme mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="dd3c2-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="dd3c2-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="dd3c2-119">Si le descripteur de fichier du DVC est récupéré en appelant [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) avec le paramètre *WTSVirtualFileHandle*, la même règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="dd3c2-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="dd3c2-120">Toutes les lectures incluent l' [**\_ \_ en-tête**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)de l’PDU du canal, et la mémoire tampon de lecture doit être au moins égale à la taille de la **\_ PDU \_ du canal** .</span><span class="sxs-lookup"><span data-stu-id="dd3c2-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 