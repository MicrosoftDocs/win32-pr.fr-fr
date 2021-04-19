---
description: Utilisation du récepteur multimédia EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Utilisation du récepteur multimédia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106545211"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="085b0-103">Utilisation du récepteur multimédia EVR</span><span class="sxs-lookup"><span data-stu-id="085b0-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="085b0-104">Le récepteur multimédia EVR (Enhanced Video Renderer) peut être utilisé en tant que composant autonome.</span><span class="sxs-lookup"><span data-stu-id="085b0-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="085b0-105">Toutefois, plus souvent, une application crée le récepteur multimédia EVR à l’intérieur d’une topologie, puis utilise la session multimédia pour contrôler la lecture.</span><span class="sxs-lookup"><span data-stu-id="085b0-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="085b0-106">Il existe deux façons de créer le récepteur multimédia EVR :</span><span class="sxs-lookup"><span data-stu-id="085b0-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="085b0-107">La fonction [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crée le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="085b0-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="085b0-108">La fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crée un objet d’activation pour le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="085b0-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="085b0-109">Le récepteur multimédia EVR a initialement un récepteur de flux, qui correspond au flux de référence.</span><span class="sxs-lookup"><span data-stu-id="085b0-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="085b0-110">Pour ajouter de nouveaux récepteurs de flux, appelez [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="085b0-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="085b0-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="085b0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="085b0-112">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="085b0-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="085b0-113">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="085b0-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



