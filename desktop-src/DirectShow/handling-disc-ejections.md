---
description: Gestion des éjections de disque
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Gestion des éjections de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845701"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="8b576-103">Gestion des éjections de disque</span><span class="sxs-lookup"><span data-stu-id="8b576-103">Handling Disc Ejections</span></span>

<span data-ttu-id="8b576-104">Lorsque l’utilisateur éjecte un DVD du lecteur, le navigateur DVD envoie à votre application un message d' \_ \_ éjection du disque DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="8b576-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="8b576-105">L’application peut ignorer ce message en toute sécurité et laisser le navigateur DVD gérer l’état du graphique.</span><span class="sxs-lookup"><span data-stu-id="8b576-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="8b576-106">Une application peut également gérer la \_ \_ méthode d’éjection du disque DVD EC \_ pour implémenter un comportement personnalisé lorsqu’un disque est éjecté.</span><span class="sxs-lookup"><span data-stu-id="8b576-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="8b576-107">Si vous gérez le message, vous devez définir l' \_ indicateur DVD ResetOnStop sur **true** avec la méthode [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , puis appeler [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) avant de fermer l’application ou de regarder un autre disque.</span><span class="sxs-lookup"><span data-stu-id="8b576-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b576-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b576-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b576-109">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="8b576-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



