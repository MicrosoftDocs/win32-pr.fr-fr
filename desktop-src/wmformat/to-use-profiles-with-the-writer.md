---
title: Pour utiliser des profils avec l’auteur
description: Pour utiliser des profils avec l’auteur
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, écriture de fichiers ASF
- Windows Media Format SDK, création de fichiers ASF
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), écriture de fichiers
- ASF (format de systèmes avancés), écriture de fichiers
- ASF (Advanced Systems Format), création de fichiers
- ASF (format des systèmes avancés), création de fichiers
- profils, création de fichiers ASF
- profils, écriture de fichiers ASF
- profils, création de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030925"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="94c6d-113">Pour utiliser des profils avec l’auteur</span><span class="sxs-lookup"><span data-stu-id="94c6d-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="94c6d-114">Le writer utilise les données de profil pour créer des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="94c6d-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="94c6d-115">Vous devez spécifier un profil à utiliser avant d’effectuer toute autre opération avec le writer.</span><span class="sxs-lookup"><span data-stu-id="94c6d-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="94c6d-116">Vous pouvez définir un profil système à utiliser avec le writer en passant l’ID de profil à la méthode [**IWMWriter :: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .</span><span class="sxs-lookup"><span data-stu-id="94c6d-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="94c6d-117">Pour spécifier un profil personnalisé à utiliser avec le writer, vous devez obtenir une interface [**IWMProfile**](iwmprofile.md) pour un objet contenant les données de profil souhaitées.</span><span class="sxs-lookup"><span data-stu-id="94c6d-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="94c6d-118">Pour ce faire, vous pouvez utiliser l’une des méthodes de chargement de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="94c6d-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="94c6d-119">Une fois que vous disposez d’une interface **IWMProfile** valide, vous pouvez lui passer un pointeur vers la méthode [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) .</span><span class="sxs-lookup"><span data-stu-id="94c6d-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="94c6d-120">Pour plus d’informations sur les paramètres de profil, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="94c6d-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="94c6d-121">Si vous apportez des modifications à l’objet de profil à l’aide de l’interface **IWMProfile** après avoir défini le profil dans le writer, vous devez rappeler **SetProfile** , sinon les modifications ne seront pas reflétées dans le writer.</span><span class="sxs-lookup"><span data-stu-id="94c6d-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="94c6d-122">Toutefois, l’appel de **SetProfile** réinitialisera tous les attributs d’en-tête. par conséquent, veillez à définir les attributs d’en-tête requis après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="94c6d-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="94c6d-123">L’exemple de fonction suivant définit le profil sur « Windows Media Video 8 pour les modems d’accès à distance (56 Kbits/s) » :</span><span class="sxs-lookup"><span data-stu-id="94c6d-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="94c6d-124">Il n’existe pas de profils système prédéfinis qui utilisent les codecs de série Windows Media Audio et Video 9.</span><span class="sxs-lookup"><span data-stu-id="94c6d-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="94c6d-125">Pour plus d’informations, consultez [réutilisation des configurations de flux](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="94c6d-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94c6d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94c6d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c6d-127">**IWMWriter::SetProfileByID**</span><span class="sxs-lookup"><span data-stu-id="94c6d-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="94c6d-128">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="94c6d-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="94c6d-129">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="94c6d-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




