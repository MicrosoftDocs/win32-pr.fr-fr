---
title: Pour identifier les entrées par nombre
description: Pour identifier les entrées par nombre
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- ASF (Advanced Systems Format), identification des entrées par numéro
- ASF (format avancé des systèmes), identification des entrées par numéro
- profils, identification des entrées par numéro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030793"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="bf1f0-106">Pour identifier les entrées par nombre</span><span class="sxs-lookup"><span data-stu-id="bf1f0-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="bf1f0-107">Chaque exemple que vous transmettez à l’enregistreur doit être associé à un numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="bf1f0-108">Chaque numéro d’entrée correspond à un ou plusieurs flux du profil utilisé par le writer pour écrire le fichier.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="bf1f0-109">Dans un profil, les sources de média sont identifiées par un nom de connexion.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="bf1f0-110">Le writer associe un numéro d’entrée à chaque nom de connexion lorsque vous définissez le profil pour le writer.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="bf1f0-111">Avant de pouvoir passer des exemples au writer, vous devez déterminer quelles sont les données attendues par chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="bf1f0-112">Vous ne pouvez pas supposer que les entrées seront dans le même ordre que les flux dans un profil, même si c’est souvent le cas.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="bf1f0-113">Par conséquent, la seule façon fiable de faire correspondre les entrées aux flux consiste à comparer le nom de connexion de l’entrée avec le nom de connexion du flux.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="bf1f0-114">Pour identifier les noms de connexion et les numéros d’entrée correspondants pour un profil chargé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bf1f0-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="bf1f0-115">Créez un objet Writer et définissez un profil à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="bf1f0-116">Pour plus d’informations sur la définition des profils dans le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="bf1f0-117">Vous devez connaître les noms de connexion utilisés pour les flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="bf1f0-118">Vous pouvez obtenir le nom de la connexion dans le profil en obtenant l’objet de configuration Stream pour chaque flux et en appelant [**IWMStreamConfig :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="bf1f0-119">Pour plus d’informations sur les profils et les objets de configuration de flux, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="bf1f0-120">Récupérez le nombre total d’entrées en appelant [**IWMWriter :: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="bf1f0-121">Parcourez toutes les entrées, en procédant comme suit pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="bf1f0-122">Récupérez l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour l’entrée en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="bf1f0-123">Récupérez le nom de la connexion qui correspond au numéro d’entrée en appelant [**IWMInputMediaProps :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="bf1f0-124">Une fois que vous avez le nom de la connexion, vous connaissez les flux associés aux numéros d’entrée affectés par le writer.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="bf1f0-125">L’exemple de code suivant affiche le nom de la connexion pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="bf1f0-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="bf1f0-126">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="bf1f0-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="bf1f0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf1f0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf1f0-128">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="bf1f0-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="bf1f0-129">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="bf1f0-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




