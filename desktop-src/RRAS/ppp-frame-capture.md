---
title: Écriture d’un pilote pour capturer des frames PPP
description: Ce document explique comment développer un pilote capable de capturer des frames PPP dans Windows Vista avant de les compresser/les chiffrer dans le chemin d’envoi ou lorsqu’ils sont décompressés/déchiffrés dans le chemin de réception.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030855"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a><span data-ttu-id="803e6-103">Écriture d’un pilote pour capturer des frames PPP</span><span class="sxs-lookup"><span data-stu-id="803e6-103">Writing a Driver to Capture PPP Frames</span></span>

<span data-ttu-id="803e6-104">Lorsque les trames de protocole PPP (PPP) sont envoyées via un tunnel PPTP (point-to-Point Tunneling Protocol) avec le chiffrement activé, ou via un tunnel L2TP (Layer 2 Tunneling Protocol) qui utilise IPSec pour le chiffrement, l’utilitaire classique de capture de trames PPP peut uniquement capturer des frames PPP qui ont un champ d’identité de protocole chiffré.</span><span class="sxs-lookup"><span data-stu-id="803e6-104">When Point-to-Point Protocol (PPP) frames are sent through a Point-to-Point Tunneling Protocol (PPTP) tunnel with encryption turned on, or through a Layer 2 Tunneling Protocol (L2TP) tunnel that uses IPSec for encryption, the typical PPP frame capture utility can only capture PPP frames that have an encrypted protocol identity field.</span></span> <span data-ttu-id="803e6-105">Ce document explique comment développer un pilote capable de capturer des frames PPP dans Windows Vista avant de les compresser/les chiffrer dans le chemin d’envoi ou lorsqu’ils sont décompressés/déchiffrés dans le chemin de réception.</span><span class="sxs-lookup"><span data-stu-id="803e6-105">This document explains how to develop a driver that can capture PPP frames in Windows Vista before they are compressed/encrypted in the send path or after they are decompressed/decrypted in the receive path.</span></span>

1.  <span data-ttu-id="803e6-106">Écrire un pilote de protocole NDIS.</span><span class="sxs-lookup"><span data-stu-id="803e6-106">Write an NDIS protocol driver.</span></span> <span data-ttu-id="803e6-107">Pour plus d’informations, consultez [pilotes de protocole ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) ou [pilotes de protocole ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).</span><span class="sxs-lookup"><span data-stu-id="803e6-107">For details, see [NDIS 6.0 Protocol Drivers](https://msdn.microsoft.com/library/ms795570.aspx) or [NDIS Protocol Drivers (NDIS 5.1)](https://msdn.microsoft.com/library/ms801145.aspx).</span></span>
2.  <span data-ttu-id="803e6-108">Installez le pilote avec une identité matérielle « MS \_ Netmon ».</span><span class="sxs-lookup"><span data-stu-id="803e6-108">Install the driver with a hardware identity of "ms\_netmon".</span></span> <span data-ttu-id="803e6-109">Pour obtenir des instructions détaillées sur l’installation du pilote avec une identité matérielle spécifique, consultez la [section modèles INF](https://msdn.microsoft.com/library/ms794357.aspx).</span><span class="sxs-lookup"><span data-stu-id="803e6-109">For detailed instructions on how to install the driver with a specific hardware identity, see [INF Models Section](https://msdn.microsoft.com/library/ms794357.aspx).</span></span>
    > [!Note]  
    > <span data-ttu-id="803e6-110">Chaque ordinateur Windows Vista autorise l’installation d’une seule entité de pilote ayant l' \_ identité matérielle « MS Netmon ».</span><span class="sxs-lookup"><span data-stu-id="803e6-110">Each Windows Vista machine permits the installation of only one driver entity that has the "ms\_netmon" hardware identity.</span></span> <span data-ttu-id="803e6-111">Pour installer un autre pilote avec cette identité, vous devez désinstaller le premier pilote.</span><span class="sxs-lookup"><span data-stu-id="803e6-111">To install another driver with this identity, the first driver must be uninstalled.</span></span> <span data-ttu-id="803e6-112">Un pilote installé sans utiliser l’identité matérielle « MS \_ Netmon » ne peut pas effectuer la liaison nécessaire pour capturer des frames PPP.</span><span class="sxs-lookup"><span data-stu-id="803e6-112">A driver that is installed without using the "ms\_netmon" hardware identity cannot perform the binding needed to capture PPP frames.</span></span>

     

3.  <span data-ttu-id="803e6-113">Le pilote de protocole doit spécifier « ndiswanbh » comme interface de liaison pour la capture des frames PPP.</span><span class="sxs-lookup"><span data-stu-id="803e6-113">The protocol driver should specify "ndiswanbh" as the binding interface for capturing PPP frames.</span></span> <span data-ttu-id="803e6-114">Pour obtenir des instructions détaillées, consultez [spécification des interfaces de liaison](https://msdn.microsoft.com/library/aa937923.aspx).</span><span class="sxs-lookup"><span data-stu-id="803e6-114">For detailed instructions, see [Specifying Binding Interfaces](https://msdn.microsoft.com/library/aa937923.aspx).</span></span>
4.  <span data-ttu-id="803e6-115">L’implémentation [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) dans le pilote doit prendre en charge « NdisMediumWan » dans le cadre de la baie de taille moyenne, afin de pouvoir ouvrir le bord du port ndiswanbh à l’aide de la fonction [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .</span><span class="sxs-lookup"><span data-stu-id="803e6-115">The [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) implementation in the driver should support "NdisMediumWan" as a part of the medium array, so that it can open the ndiswanbh miniport edge using the [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) function.</span></span>
5.  <span data-ttu-id="803e6-116">Si la fonction [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) est appelée avec l’état \_ NDIS \_ réussite, le pilote de protocole doit définir l’OID du [ \_ \_ \_ \_ filtre de paquets actuel](https://msdn.microsoft.com/library/bb314089.aspx) de l’OID avec les indicateurs [NDIS \_ \_ \_ promiscuité de type](https://msdn.microsoft.com/library/bb314089.aspx) de paquet et [NDIS type de \_ paquet \_ \_ \_ local](https://msdn.microsoft.com/library/bb314089.aspx) sur cette liaison.</span><span class="sxs-lookup"><span data-stu-id="803e6-116">If the [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) function is called with status NDIS\_STATUS\_SUCCESS, the protocol driver should set the [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/bb314089.aspx) OID with the flags [NDIS\_PACKET\_TYPE\_PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) and [NDIS\_PACKET\_TYPE\_ALL\_LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) over this binding.</span></span> <span data-ttu-id="803e6-117">Une fois cette opération effectuée, le pilote de protocole reçoit les trames PPP déchiffrées de la couche de tramage PPP dans sa fonction [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .</span><span class="sxs-lookup"><span data-stu-id="803e6-117">Once this is done, the protocol driver will receive the decrypted PPP frames from the PPP framing layer in its [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) function.</span></span>

> [!Note]  
> <span data-ttu-id="803e6-118">Ces informations s’appliquent uniquement aux pilotes sur un ordinateur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="803e6-118">This information only applies to drivers on a Windows Vista machine.</span></span>

 

 

 




