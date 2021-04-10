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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Obtention des fonctionnalités de format via IWMDMDevice3

[**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) est la méthode recommandée pour demander à un appareil les formats qu’il prend en charge. Les étapes suivantes montrent comment utiliser cette méthode pour interroger un appareil pour ses fonctionnalités de format :

1.  L’application doit déterminer les formats pris en charge par un appareil et ceux qui vous intéressent. Pour ce faire, l’application peut demander une liste de formats pris en charge par l’appareil en appelant [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  L’application parcourt tous les formats pris en charge et demande les capacités de format d’un appareil pour un format spécifique (par exemple, WMA ou WMV) en appelant **IWMDMDevice3 :: GetFormatCapability** et en spécifiant un format à l’aide de l’énumération [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) . Cette méthode récupère une structure [**de \_ \_ capacité de format WMDM**](wmdm-format-capability.md) .
3.  Parcourez toutes les structures de [**\_ \_ configuration prop WMDM**](wmdm-prop-config.md) dans la structure de **\_ \_ capacité de format WMDM** récupérée. Chaque structure de **\_ \_ configuration WMDM prop** contient un groupe de propriétés avec des valeurs prises en charge, représentant une configuration pour ce format. Chaque configuration possède un numéro de préférence, où un nombre inférieur indique une préférence supérieure par l’appareil.
4.  Parcourez toutes les structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) dans la **\_ \_ configuration WMDM prop** récupérée. Chaque **WMDM \_ prop \_ desc** contient une liste de paires propriété/valeur prises en charge.
5.  Récupérez les noms et les valeurs des propriétés de la structure **WMDM \_ prop \_ desc** . Les propriétés incluent la vitesse de transmission, le codec et la taille de trame. Les noms de propriété sont définis dans le fichier d’en-tête mswmdm. h. une liste de la plupart de ces constantes est donnée dans les [constantes de métadonnées](metadata-constants.md). Trois types de valeurs de propriété sont possibles :
    -   Une valeur unique, WMDM \_ enum \_ prop \_ valeurs valides \_ \_ Any, indiquant la prise en charge de toutes les valeurs de cette propriété.
    -   Plage de valeurs, définie par une valeur maximale, une valeur minimale et un intervalle.
    -   Liste de valeurs discrètes.
6.  Effacez les valeurs stockées. La mémoire pour ces valeurs est allouée par Windows Media Gestionnaire de périphériques ; votre appareil est responsable de la libération de la mémoire. La procédure à suivre est décrite à la fin de cette rubrique.

Lors de la réponse à **GetFormatCapability**, un appareil peut \_ signaler \_ \_ des valeurs valides de WMDM enum prop \_ pour la \_ **fonctionnalité de format WMDM \_ \_ . configuration de WMDM \_ prop \_ . WMDM \_ prop \_ desc. ValidValuesForm** pour revendiquer la prise en charge de toutes les valeurs pour la vitesse de transmission, les canaux, etc. Toutefois, vous devez traiter cette revendication avec précaution, car les appareils peuvent parfois signaler la prise en charge de toutes les valeurs lorsque, en fait, elles ne prennent pas en charge toutes les tailles d’image ou les vitesses de transmission. Vous pouvez envisager de faire en sorte que votre application transporte des fichiers de très grande taille ou de haut débit vers des versions plus petites ou moins gourmand en mémoire et des versions gourmandes en ressources processeur lors de leur envoi à des appareils destinés à lire ces fichiers.

La fonction C++ suivante montre comment demander la prise en charge du format de périphérique pour un format spécifique.


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



**Effacement de la mémoire allouée**

Après avoir récupéré les fonctionnalités de format d’un appareil, l’application doit libérer la mémoire allouée pour contenir la description. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) et [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) ont des tableaux de structures simples qui peuvent être effacées en appelant simplement **CoTaskMemFree** avec le tableau. Toutefois, **GetFormatCapability** a une structure de données plus complexe avec une mémoire allouée dynamiquement qui doit être effacée en parcourant tous les éléments et en les libérant individuellement.

Le code C++ suivant montre comment une application peut libérer la mémoire allouée pour une structure de **\_ \_ capacité de format WMDM** .


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



**Interrogation de tous les formats pris en charge**

En règle générale, une application interroge un appareil à un format spécifique, car il souhaite envoyer un fichier spécifique à l’appareil. Toutefois, si vous souhaitez interroger une application pour tous les formats pris en charge, vous pouvez appeler [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) et transmettre g \_ wszWMDMFormatsSupported pour récupérer une liste complète.

Si un appareil ne retourne qu’un seul élément, WMDM \_ FORMATCODE \_ non défini, cela signifie généralement que l’appareil ne prend pas en charge les codes de format. L’appel de **GetFormatCapability** avec WMDM \_ FORMATCODE \_ non défini peut récupérer des fonctionnalités, mais ces propriétés peuvent être relativement génériques (telles que le nom, la taille du fichier, la date de la dernière modification, etc.).

Les étapes suivantes montrent comment interroger une liste de tous les formats pris en charge :

1.  Demandez une liste de tous les codes de format pris en charge en appelant **IWMDMDevice3 :: GetProperty** et en passant dans g \_ wszWMDMFormatsSupported. Cela renvoie un **PROPVARIANT** contenant un **SAFEARRAY** de formats pris en charge.
2.  Parcourez les éléments en appelant **SafeArrayGetElement**. Chaque élément est une énumération **WMDM \_ FORMATCODE** .
3.  Demandez les fonctionnalités pour chaque format, en libérant la mémoire pour chaque élément de **\_ \_ fonctionnalité de format de WMDM** une fois qu’il est terminé.
4.  Effacez le **PROPVARIANT** récupéré à l’étape 1 en appelant **PropVariantClear**.

L’exemple de code C++ suivant récupère la liste des formats pris en charge pour un appareil.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Découverte des fonctionnalités de format des appareils**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




