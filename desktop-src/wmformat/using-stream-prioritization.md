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
ms.openlocfilehash: 3db00466eb27685a33851f7bffa5133e1d94a203985b1a0a56b110a09ad88ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963948"
---
# <a name="using-stream-prioritization"></a>Utilisation de la hiérarchisation des flux

La hiérarchisation des flux vous permet d’avoir davantage de contrôle sur la lecture du contenu en vous permettant de spécifier l’ordre de priorité des flux dans un profil. Lorsque le lecteur et le serveur de streaming rencontrent une pénurie de bande passante pendant la lecture, il peut être nécessaire de supprimer des échantillons pour fournir une lecture ininterrompue. Si vous spécifiez un ordre de priorité avec un objet de priorité de flux dans le profil, les exemples seront supprimés en premier des flux de priorité les plus faibles.

Contrairement au partage de bande passante et aux objets d’exclusion mutuelle, un objet de priorité de flux n’utilise pas l’interface [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) pour effectuer le suivi de la liste de flux. Au lieu de cela, vous devez utiliser un tableau de structures d' [**\_ enregistrement de \_ priorité \_ de flux WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) . Les structures doivent être organisées dans le tableau dans l’ordre de priorité décroissant. En plus de contenir un numéro de flux, la structure de priorité de flux vous permet également de spécifier si un flux est obligatoire. Les flux obligatoires ne sont pas supprimés, quel que soit leur emplacement dans la liste.

L’exemple de code suivant montre comment inclure une priorité de flux dans un profil. Ce profil est destiné à une présentation en salle de classe, avec un flux audio du professeur, un flux vidéo du professeur et un flux vidéo capturant les diapositives de présentation. Le flux audio est le plus important et sera obligatoire. Les diapositives de présentation auront la priorité la plus faible, car l’image sera assez constante, donc quelques frames sont perdus ici et il n’y a pas de différence.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




