---
title: Configuration commune à tous les flux
description: Configuration commune à tous les flux
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profils, configurations communes à tous les flux
- flux, configurations communes
- flux, noms
- flux, noms de connexion
- flux, nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104381717"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="d1ff1-108">Configuration commune à tous les flux</span><span class="sxs-lookup"><span data-stu-id="d1ff1-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="d1ff1-109">Tous les flux, quel que soit leur type, doivent recevoir un nom de flux, un nom de connexion et un numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="d1ff1-110">Le nom du flux est simplement un nom descriptif que vous attribuez au flux.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="d1ff1-111">Un flux n’a pas besoin d’avoir un nom de flux, mais il vous aide à identifier le flux lorsque vous modifiez le profil ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="d1ff1-112">Vous pouvez définir un nom pour le flux en appelant [**IWMStreamConfig :: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span><span class="sxs-lookup"><span data-stu-id="d1ff1-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="d1ff1-113">Chaque flux doit avoir un nom de connexion, également appelé nom d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="d1ff1-114">Lorsque vous définissez le profil dans l’objet Writer pour écrire un fichier, le writer associe chaque nom de connexion à une entrée.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="d1ff1-115">Pour identifier les entrées, vous devez appeler [**IWMInputMediaProps :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) pour récupérer le nom de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="d1ff1-116">Les noms de connexion standard sont des descriptions simples du contenu, telles que « audio ».</span><span class="sxs-lookup"><span data-stu-id="d1ff1-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="d1ff1-117">Si votre profil contient des flux qui sont mutuellement exclusifs par vitesse de transmission, chacun des flux mutuellement exclusifs doit avoir le même nom de connexion.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="d1ff1-118">Si ce n’est pas le cas, le profil n’est pas valide et sera rejeté par le writer.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="d1ff1-119">Vous pouvez définir un nom de connexion en appelant [**IWMStreamConfig :: SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span><span class="sxs-lookup"><span data-stu-id="d1ff1-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="d1ff1-120">Le numéro de flux identifie le flux au sein du fichier.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="d1ff1-121">Contrairement aux nombres d’entrée et aux numéros de sortie, les numéros de flux commencent à 1, et non à 0.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="d1ff1-122">Un numéro de flux est différent d’un index de flux, que vous utilisez pour obtenir des flux dans un profil à l’aide de [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="d1ff1-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="d1ff1-123">L’index de flux est un nombre affecté au flux par l’objet de profil.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="d1ff1-124">Les index de flux sont compris entre 0 et un de moins que le nombre de flux récupérés par [**IWMProfile :: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span><span class="sxs-lookup"><span data-stu-id="d1ff1-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="d1ff1-125">Les numéros de flux n’ont pas besoin d’être séquentiels, même s’ils sont généralement, et peuvent être compris entre 1 et 63.</span><span class="sxs-lookup"><span data-stu-id="d1ff1-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="d1ff1-126">Vous pouvez définir un numéro de flux en appelant [**IWMStreamConfig :: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span><span class="sxs-lookup"><span data-stu-id="d1ff1-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1ff1-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1ff1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ff1-128">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="d1ff1-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="d1ff1-129">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="d1ff1-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




