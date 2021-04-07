---
title: Utilisation des marqueurs
description: Utilisation des marqueurs
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marqueurs
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- ASF (Advanced Systems Format), recherche de marqueurs
- ASF (format de systèmes avancés), recherche de marqueurs
- marqueurs, à propos de
- marqueurs, ajout
- marqueurs, suppression
- marqueurs, récupération
- marqueurs, recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724114"
---
# <a name="using-markers"></a><span data-ttu-id="e9557-113">Utilisation des marqueurs</span><span class="sxs-lookup"><span data-stu-id="e9557-113">Using Markers</span></span>

<span data-ttu-id="e9557-114">Un *marqueur* est un point nommé dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="e9557-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="e9557-115">Chaque marqueur se compose d’un nom et d’une heure associée, mesuré comme un décalage par rapport au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="e9557-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="e9557-116">Une application peut utiliser des marqueurs pour affecter des noms à différents points dans le contenu, afficher ces noms à l’utilisateur, puis rechercher les positions des marqueurs.</span><span class="sxs-lookup"><span data-stu-id="e9557-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="e9557-117">Une application peut ajouter ou supprimer des marqueurs d’un fichier ASF existant.</span><span class="sxs-lookup"><span data-stu-id="e9557-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="e9557-118">L’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contient des méthodes permettant d’utiliser des marqueurs.</span><span class="sxs-lookup"><span data-stu-id="e9557-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="e9557-119">L’objet éditeur de métadonnées prend en charge l’ajout et la suppression de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="e9557-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="e9557-120">Les objets Writer et Reader peuvent récupérer des marqueurs, mais ils ne peuvent pas ajouter ou supprimer des marqueurs.</span><span class="sxs-lookup"><span data-stu-id="e9557-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="e9557-121">Ajouter des marqueurs</span><span class="sxs-lookup"><span data-stu-id="e9557-121">Adding Markers</span></span>

<span data-ttu-id="e9557-122">Pour ajouter un marqueur, interrogez l’éditeur de métadonnées pour l’interface **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="e9557-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="e9557-123">Appelez ensuite la méthode [**IWMHeaderInfo :: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , en spécifiant le nom du marqueur sous la forme d’une chaîne de caractères larges et le temps en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="e9557-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="e9557-124">L’heure ne doit pas dépasser la durée du fichier.</span><span class="sxs-lookup"><span data-stu-id="e9557-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="e9557-125">Deux marqueurs peuvent avoir la même heure.</span><span class="sxs-lookup"><span data-stu-id="e9557-125">Two markers can have the same time.</span></span>

<span data-ttu-id="e9557-126">L’exemple suivant ajoute plusieurs marqueurs à un fichier :</span><span class="sxs-lookup"><span data-stu-id="e9557-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="e9557-127">Supprimer des marqueurs</span><span class="sxs-lookup"><span data-stu-id="e9557-127">Removing Markers</span></span>

<span data-ttu-id="e9557-128">Pour supprimer un marqueur, appelez [**IWMHeaderInfo :: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), en spécifiant l’index du marqueur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e9557-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="e9557-129">Les marqueurs sont automatiquement triés dans l’ordre chronologique plus important, de sorte que l’index 0 est toujours le premier marqueur.</span><span class="sxs-lookup"><span data-stu-id="e9557-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="e9557-130">Notez que l’appel de **RemoveMarker** modifie les numéros d’index des marqueurs qui suivent.</span><span class="sxs-lookup"><span data-stu-id="e9557-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="e9557-131">Le code suivant, où *pinfo* est un pointeur vers une interface **IWMHeaderInfo** , supprime tous les marqueurs d’un fichier :</span><span class="sxs-lookup"><span data-stu-id="e9557-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="e9557-132">Récupération des marqueurs</span><span class="sxs-lookup"><span data-stu-id="e9557-132">Retrieving Markers</span></span>

<span data-ttu-id="e9557-133">Pour récupérer le nom et l’heure d’un marqueur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9557-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="e9557-134">Appelez la méthode [**IWMHeaderInfo :: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) pour déterminer le nombre de marqueurs que contient le fichier.</span><span class="sxs-lookup"><span data-stu-id="e9557-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="e9557-135">Récupérez la taille de la chaîne nécessaire pour contenir le nom du marqueur.</span><span class="sxs-lookup"><span data-stu-id="e9557-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="e9557-136">Pour ce faire, appelez la méthode [**IWMHeaderInfo :: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) .</span><span class="sxs-lookup"><span data-stu-id="e9557-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="e9557-137">Spécifiez l’index du marqueur à récupérer, et **null** pour la mémoire tampon de la chaîne (paramètre *pwszMarkerName* ).</span><span class="sxs-lookup"><span data-stu-id="e9557-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="e9557-138">La méthode retourne la longueur de la chaîne, y compris le caractère « \\ 0 » de fin, dans le paramètre *pcchMarkerNameLen* .</span><span class="sxs-lookup"><span data-stu-id="e9557-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="e9557-139">Allouez une chaîne de caractères larges pour recevoir le nom.</span><span class="sxs-lookup"><span data-stu-id="e9557-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="e9557-140">Appelez à nouveau **GetMarker** , mais cette fois, vous transmettez l’adresse de la chaîne dans le paramètre *pwszMarkerName* .</span><span class="sxs-lookup"><span data-stu-id="e9557-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="e9557-141">La méthode écrit le nom du marqueur dans la chaîne et retourne l’heure du marqueur dans le paramètre *pcnsMarkerTime* .</span><span class="sxs-lookup"><span data-stu-id="e9557-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="e9557-142">Le code suivant parcourt chaque marqueur dans l’ordre et récupère le nom et l’heure :</span><span class="sxs-lookup"><span data-stu-id="e9557-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="e9557-143">Recherche d’un marqueur</span><span class="sxs-lookup"><span data-stu-id="e9557-143">Seeking to a Marker</span></span>

<span data-ttu-id="e9557-144">Pour démarrer la lecture à partir d’un emplacement de marqueur, appelez la méthode [**IWMReaderAdvanced2 :: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) de l’objet lecteur, en spécifiant l’index du marqueur.</span><span class="sxs-lookup"><span data-stu-id="e9557-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="e9557-145">Les paramètres restants sont identiques à ceux de la méthode [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) .</span><span class="sxs-lookup"><span data-stu-id="e9557-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="e9557-146">L’exemple suivant interroge le lecteur pour obtenir l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) et recherche le premier marqueur.</span><span class="sxs-lookup"><span data-stu-id="e9557-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="e9557-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9557-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9557-148">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="e9557-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="e9557-149">**IWMReaderAdvanced2::StartAtMarker**</span><span class="sxs-lookup"><span data-stu-id="e9557-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="e9557-150">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="e9557-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




