---
title: Utilisation de la hiérarchisation des flux
description: Utilisation de la hiérarchisation des flux
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media Format SDK, hiérarchisation des flux
- profils, hiérarchisation des flux
- flux, hiérarchisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940663"
---
# <a name="using-stream-prioritization"></a><span data-ttu-id="c59b8-106">Utilisation de la hiérarchisation des flux</span><span class="sxs-lookup"><span data-stu-id="c59b8-106">Using Stream Prioritization</span></span>

<span data-ttu-id="c59b8-107">La hiérarchisation des flux vous permet d’avoir davantage de contrôle sur la lecture du contenu en vous permettant de spécifier l’ordre de priorité des flux dans un profil.</span><span class="sxs-lookup"><span data-stu-id="c59b8-107">Stream prioritization enables you to have more control over the playback of content by allowing you to specify priority order for the streams in a profile.</span></span> <span data-ttu-id="c59b8-108">Lorsque le lecteur et le serveur de streaming rencontrent une pénurie de bande passante pendant la lecture, il peut être nécessaire de supprimer des échantillons pour fournir une lecture ininterrompue.</span><span class="sxs-lookup"><span data-stu-id="c59b8-108">When the reader and streaming server encounter a bandwidth shortage during playback, samples may have to be dropped to provide uninterrupted playback.</span></span> <span data-ttu-id="c59b8-109">Si vous spécifiez un ordre de priorité avec un objet de priorité de flux dans le profil, les exemples seront supprimés en premier des flux de priorité les plus faibles.</span><span class="sxs-lookup"><span data-stu-id="c59b8-109">If you specify a priority order with a stream prioritization object in the profile, samples will be dropped from the lowest priority streams first.</span></span>

<span data-ttu-id="c59b8-110">Contrairement au partage de bande passante et aux objets d’exclusion mutuelle, un objet de priorité de flux n’utilise pas l’interface [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) pour effectuer le suivi de la liste de flux.</span><span class="sxs-lookup"><span data-stu-id="c59b8-110">Unlike bandwidth sharing and mutual exclusion objects, a stream prioritization object does not use the [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) interface to keep track of the list of streams.</span></span> <span data-ttu-id="c59b8-111">Au lieu de cela, vous devez utiliser un tableau de structures d' [**\_ enregistrement de \_ priorité \_ de flux WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) .</span><span class="sxs-lookup"><span data-stu-id="c59b8-111">Instead, you must use an array of [**WM\_STREAM\_PRIORITY\_RECORD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) structures.</span></span> <span data-ttu-id="c59b8-112">Les structures doivent être organisées dans le tableau dans l’ordre de priorité décroissant.</span><span class="sxs-lookup"><span data-stu-id="c59b8-112">The structures must be organized in the array in descending order of priority.</span></span> <span data-ttu-id="c59b8-113">En plus de contenir un numéro de flux, la structure de priorité de flux vous permet également de spécifier si un flux est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c59b8-113">In addition to holding a stream number, the stream priority structure also enables you to specify whether a stream is mandatory.</span></span> <span data-ttu-id="c59b8-114">Les flux obligatoires ne sont pas supprimés, quel que soit leur emplacement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c59b8-114">Mandatory streams will not be dropped, regardless of their position in the list.</span></span>

<span data-ttu-id="c59b8-115">L’exemple de code suivant montre comment inclure une priorité de flux dans un profil.</span><span class="sxs-lookup"><span data-stu-id="c59b8-115">The following example code shows how to include a stream prioritization in a profile.</span></span> <span data-ttu-id="c59b8-116">Ce profil est destiné à une présentation en salle de classe, avec un flux audio du professeur, un flux vidéo du professeur et un flux vidéo capturant les diapositives de présentation.</span><span class="sxs-lookup"><span data-stu-id="c59b8-116">This profile is for a classroom presentation, with an audio stream of the lecturer speaking, a video stream of the lecturer, and a video stream capturing the presentation slides.</span></span> <span data-ttu-id="c59b8-117">Le flux audio est le plus important et sera obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c59b8-117">The audio stream is the most important and will be mandatory.</span></span> <span data-ttu-id="c59b8-118">Les diapositives de présentation auront la priorité la plus faible, car l’image sera assez constante, donc quelques frames sont perdus ici et il n’y a pas de différence.</span><span class="sxs-lookup"><span data-stu-id="c59b8-118">The presentation slides will have the lowest priority because the image will be pretty constant, so a few frames lost here and there won't make much difference.</span></span>


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="c59b8-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c59b8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c59b8-120">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="c59b8-120">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




