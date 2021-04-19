---
title: Magasins en ligne exclusifs
description: Magasins en ligne exclusifs
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online stores, exclusif
- magasins en ligne, exclusifs
- tapez 1 magasins en ligne, exclusif
- tapez 2 magasins en ligne, exclusif
- magasins en ligne exclusifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511058"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="3e273-108">Magasins en ligne exclusifs</span><span class="sxs-lookup"><span data-stu-id="3e273-108">Exclusive Online Stores</span></span>

<span data-ttu-id="3e273-109">Avec le lecteur Windows Media 11, une application qui incorpore le contrôle du lecteur à distance peut spécifier un magasin en ligne exclusif.</span><span class="sxs-lookup"><span data-stu-id="3e273-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="3e273-110">Dans ce cas, le sélecteur de service dans le lecteur Windows Media est désactivé et seule la Banque en ligne spécifiée est disponible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3e273-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="3e273-111">En outre, le lecteur Windows Media adopte la couleur spécifiée par l’élément **Color** du document serviceInfo de la boutique en ligne exclusive.</span><span class="sxs-lookup"><span data-stu-id="3e273-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="3e273-112">Pour spécifier un magasin en ligne exclusif, une application doit ajouter ExclusiveService :*keyName* à la fin de la chaîne qu’elle retourne à partir de [IWMPRemoteMediaServices :: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span><span class="sxs-lookup"><span data-stu-id="3e273-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="3e273-113">Par exemple, supposons que Proseware est le nom de clé donné à un magasin en ligne particulier.</span><span class="sxs-lookup"><span data-stu-id="3e273-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="3e273-114">Si **GetServiceType** retourne la chaîne « Remote ExclusiveService : Proseware », le Proseware sera le seul magasin en ligne disponible dans le contrôle de lecteur incorporé à distance.</span><span class="sxs-lookup"><span data-stu-id="3e273-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="3e273-115">Une application peut limiter le lecteur Windows Media à une boutique en ligne exclusive uniquement si le lecteur Windows Media n’est pas déjà en cours d’exécution lorsque l’application est lancée.</span><span class="sxs-lookup"><span data-stu-id="3e273-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="3e273-116">Il incombe à l’application d’informer l’utilisateur qu’il doit fermer le lecteur Windows Media avant d’exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="3e273-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e273-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e273-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e273-118">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="3e273-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3e273-119">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="3e273-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




