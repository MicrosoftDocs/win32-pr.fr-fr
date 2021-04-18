---
description: Exemple de filtre InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemple de filtre InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515906"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="454a5-103">Exemple de filtre InfTee</span><span class="sxs-lookup"><span data-stu-id="454a5-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="454a5-104">Description</span><span class="sxs-lookup"><span data-stu-id="454a5-104">Description</span></span>

<span data-ttu-id="454a5-105">Le filtre InfTee fournit un exemple d’implémentation du filtre [tee de code PIN infinie](infinite-pin-tee-filter.md) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="454a5-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="454a5-106">Le filtre a une broche d’entrée et un nombre dynamique de broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="454a5-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="454a5-107">Tous les exemples de supports envoyés au filtre sont remis simultanément à partir de toutes les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="454a5-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="454a5-108">Ce filtre apparaît dans GraphEdit sous le nom « sample infini pin tee » pour le distinguer du filtre tee de code confidentiel infini standard fourni dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="454a5-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="454a5-109">Utilisation</span><span class="sxs-lookup"><span data-stu-id="454a5-109">Usage</span></span>

<span data-ttu-id="454a5-110">Étant donné que ce filtre ne modifie pas les données qu’il reçoit, tous les codes confidentiels doivent accepter le même type de média.</span><span class="sxs-lookup"><span data-stu-id="454a5-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="454a5-111">Pendant le processus de connexion, le filtre peut reconnecter certains codes confidentiels pour que les types de média correspondent.</span><span class="sxs-lookup"><span data-stu-id="454a5-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="454a5-112">Les données arrivant à la broche d’entrée ne sont pas copiées avant d’être envoyées aux broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="454a5-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="454a5-113">Le filtre garantit également que les données sont remises aux filtres en aval, pour garantir que les deux sorties reçoivent le service en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="454a5-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="454a5-114">En particulier, si l’une des sorties peut se bloquer dans la fonction membre [**COutputQueue :: Receive**](coutputqueue-receive.md) , l’tee crée un thread pour remettre l’exemple.</span><span class="sxs-lookup"><span data-stu-id="454a5-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="454a5-115">S’il n’existait aucun thread pour remettre l’exemple, le thread qui remet l’échantillon à la broche d’entrée tee peut passer les données à un filtre en aval ; à ce stade, il peut bloquer, en conservant les données de l’autre filtre en aval pendant de longues périodes.</span><span class="sxs-lookup"><span data-stu-id="454a5-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="454a5-116">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="454a5-116">Downloading the Sample</span></span>

<span data-ttu-id="454a5-117">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="454a5-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="454a5-118">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ fichiers de \\ \\ \\ filtres DirectShow \\ InfTee.</span><span class="sxs-lookup"><span data-stu-id="454a5-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="454a5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="454a5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="454a5-120">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="454a5-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



