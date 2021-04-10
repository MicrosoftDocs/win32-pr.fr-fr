---
title: Obtention des fonctionnalités de format via IWMDMDevice3
description: Obtention des fonctionnalités de format sur les appareils qui prennent en charge IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Gestionnaire de périphériques Windows Media, fonctionnalités de l’appareil
- Gestionnaire de périphériques, fonctionnalités de l’appareil
- Guide de programmation, fonctionnalités de l’appareil
- applications de bureau, fonctionnalités de l’appareil
- création d’applications Windows Media Gestionnaire de périphériques, fonctionnalités de l’appareil
- écriture de fichiers sur des appareils, fonctionnalités de l’appareil
- Méthode IWMDMDevice3
- Gestionnaire de périphériques Windows Media, méthode IWMDMDevice3
- Gestionnaire de périphériques, méthode IWMDMDevice3
- Guide de programmation, méthode IWMDMDevice3
- applications de bureau, méthode IWMDMDevice3
- création d’applications Windows Media Gestionnaire de périphériques, méthode IWMDMDevice3
- écriture de fichiers sur des appareils, méthode IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104030654"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="805ce-116">Obtention des fonctionnalités de format via IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="805ce-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="805ce-117">[**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) est la méthode recommandée pour demander à un appareil les formats qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="805ce-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="805ce-118">Les étapes suivantes montrent comment utiliser cette méthode pour interroger un appareil pour ses fonctionnalités de format :</span><span class="sxs-lookup"><span data-stu-id="805ce-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="805ce-119">L’application doit déterminer les formats pris en charge par un appareil et ceux qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="805ce-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="805ce-120">Pour ce faire, l’application peut demander une liste de formats pris en charge par l’appareil en appelant [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span><span class="sxs-lookup"><span data-stu-id="805ce-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="805ce-121">L’application parcourt tous les formats pris en charge et demande les capacités de format d’un appareil pour un format spécifique (par exemple, WMA ou WMV) en appelant **IWMDMDevice3 :: GetFormatCapability** et en spécifiant un format à l’aide de l’énumération [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) .</span><span class="sxs-lookup"><span data-stu-id="805ce-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="805ce-122">Cette méthode récupère une structure [**de \_ \_ capacité de format WMDM**](wmdm-format-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="805ce-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="805ce-123">Parcourez toutes les structures de [**\_ \_ configuration prop WMDM**](wmdm-prop-config.md) dans la structure de **\_ \_ capacité de format WMDM** récupérée.</span><span class="sxs-lookup"><span data-stu-id="805ce-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="805ce-124">Chaque structure de **\_ \_ configuration WMDM prop** contient un groupe de propriétés avec des valeurs prises en charge, représentant une configuration pour ce format.</span><span class="sxs-lookup"><span data-stu-id="805ce-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="805ce-125">Chaque configuration possède un numéro de préférence, où un nombre inférieur indique une préférence supérieure par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="805ce-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="805ce-126">Parcourez toutes les structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) dans la **\_ \_ configuration WMDM prop** récupérée.</span><span class="sxs-lookup"><span data-stu-id="805ce-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="805ce-127">Chaque **WMDM \_ prop \_ desc** contient une liste de paires propriété/valeur prises en charge.</span><span class="sxs-lookup"><span data-stu-id="805ce-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="805ce-128">Récupérez les noms et les valeurs des propriétés de la structure **WMDM \_ prop \_ desc** .</span><span class="sxs-lookup"><span data-stu-id="805ce-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="805ce-129">Les propriétés incluent la vitesse de transmission, le codec et la taille de trame.</span><span class="sxs-lookup"><span data-stu-id="805ce-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="805ce-130">Les noms de propriété sont définis dans le fichier d’en-tête mswmdm. h. une liste de la plupart de ces constantes est donnée dans les [constantes de métadonnées](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="805ce-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="805ce-131">Trois types de valeurs de propriété sont possibles :</span><span class="sxs-lookup"><span data-stu-id="805ce-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="805ce-132">Une valeur unique, WMDM \_ enum \_ prop \_ valeurs valides \_ \_ Any, indiquant la prise en charge de toutes les valeurs de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="805ce-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="805ce-133">Plage de valeurs, définie par une valeur maximale, une valeur minimale et un intervalle.</span><span class="sxs-lookup"><span data-stu-id="805ce-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="805ce-134">Liste de valeurs discrètes.</span><span class="sxs-lookup"><span data-stu-id="805ce-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="805ce-135">Effacez les valeurs stockées.</span><span class="sxs-lookup"><span data-stu-id="805ce-135">Clear the stored values.</span></span> <span data-ttu-id="805ce-136">La mémoire pour ces valeurs est allouée par Windows Media Gestionnaire de périphériques ; votre appareil est responsable de la libération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="805ce-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="805ce-137">La procédure à suivre est décrite à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="805ce-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="805ce-138">Lors de la réponse à **GetFormatCapability**, un appareil peut \_ signaler \_ \_ des valeurs valides de WMDM enum prop \_ pour la \_ **fonctionnalité de format WMDM \_ \_ . configuration de WMDM \_ prop \_ . WMDM \_ prop \_ desc. ValidValuesForm** pour revendiquer la prise en charge de toutes les valeurs pour la vitesse de transmission, les canaux, etc.</span><span class="sxs-lookup"><span data-stu-id="805ce-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="805ce-139">Toutefois, vous devez traiter cette revendication avec précaution, car les appareils peuvent parfois signaler la prise en charge de toutes les valeurs lorsque, en fait, elles ne prennent pas en charge toutes les tailles d’image ou les vitesses de transmission.</span><span class="sxs-lookup"><span data-stu-id="805ce-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="805ce-140">Vous pouvez envisager de faire en sorte que votre application transporte des fichiers de très grande taille ou de haut débit vers des versions plus petites ou moins gourmand en mémoire et des versions gourmandes en ressources processeur lors de leur envoi à des appareils destinés à lire ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="805ce-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="805ce-141">La fonction C++ suivante montre comment demander la prise en charge du format de périphérique pour un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="805ce-141">The following C++ function shows how to request device format support for a specific format.</span></span>


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



<span data-ttu-id="805ce-142">**Effacement de la mémoire allouée**</span><span class="sxs-lookup"><span data-stu-id="805ce-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="805ce-143">Après avoir récupéré les fonctionnalités de format d’un appareil, l’application doit libérer la mémoire allouée pour contenir la description.</span><span class="sxs-lookup"><span data-stu-id="805ce-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="805ce-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) et [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) ont des tableaux de structures simples qui peuvent être effacées en appelant simplement **CoTaskMemFree** avec le tableau.</span><span class="sxs-lookup"><span data-stu-id="805ce-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="805ce-145">Toutefois, **GetFormatCapability** a une structure de données plus complexe avec une mémoire allouée dynamiquement qui doit être effacée en parcourant tous les éléments et en les libérant individuellement.</span><span class="sxs-lookup"><span data-stu-id="805ce-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="805ce-146">Le code C++ suivant montre comment une application peut libérer la mémoire allouée pour une structure de **\_ \_ capacité de format WMDM** .</span><span class="sxs-lookup"><span data-stu-id="805ce-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



<span data-ttu-id="805ce-147">**Interrogation de tous les formats pris en charge**</span><span class="sxs-lookup"><span data-stu-id="805ce-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="805ce-148">En règle générale, une application interroge un appareil à un format spécifique, car il souhaite envoyer un fichier spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="805ce-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="805ce-149">Toutefois, si vous souhaitez interroger une application pour tous les formats pris en charge, vous pouvez appeler [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) et transmettre g \_ wszWMDMFormatsSupported pour récupérer une liste complète.</span><span class="sxs-lookup"><span data-stu-id="805ce-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="805ce-150">Si un appareil ne retourne qu’un seul élément, WMDM \_ FORMATCODE \_ non défini, cela signifie généralement que l’appareil ne prend pas en charge les codes de format.</span><span class="sxs-lookup"><span data-stu-id="805ce-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="805ce-151">L’appel de **GetFormatCapability** avec WMDM \_ FORMATCODE \_ non défini peut récupérer des fonctionnalités, mais ces propriétés peuvent être relativement génériques (telles que le nom, la taille du fichier, la date de la dernière modification, etc.).</span><span class="sxs-lookup"><span data-stu-id="805ce-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="805ce-152">Les étapes suivantes montrent comment interroger une liste de tous les formats pris en charge :</span><span class="sxs-lookup"><span data-stu-id="805ce-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="805ce-153">Demandez une liste de tous les codes de format pris en charge en appelant **IWMDMDevice3 :: GetProperty** et en passant dans g \_ wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="805ce-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="805ce-154">Cela renvoie un **PROPVARIANT** contenant un **SAFEARRAY** de formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="805ce-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="805ce-155">Parcourez les éléments en appelant **SafeArrayGetElement**.</span><span class="sxs-lookup"><span data-stu-id="805ce-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="805ce-156">Chaque élément est une énumération **WMDM \_ FORMATCODE** .</span><span class="sxs-lookup"><span data-stu-id="805ce-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="805ce-157">Demandez les fonctionnalités pour chaque format, en libérant la mémoire pour chaque élément de **\_ \_ fonctionnalité de format de WMDM** une fois qu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="805ce-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="805ce-158">Effacez le **PROPVARIANT** récupéré à l’étape 1 en appelant **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="805ce-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="805ce-159">L’exemple de code C++ suivant récupère la liste des formats pris en charge pour un appareil.</span><span class="sxs-lookup"><span data-stu-id="805ce-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="805ce-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="805ce-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="805ce-161">**Découverte des fonctionnalités de format des appareils**</span><span class="sxs-lookup"><span data-stu-id="805ce-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




