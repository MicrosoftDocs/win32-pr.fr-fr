---
title: Spinner
description: Le compteur est un contrôle composite qui se compose d’un bouton d’incrémentation, d’un bouton de décrémentation et d’un contrôle d’édition, qui sont tous utilisés pour fournir des valeurs décimales à l’application.
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0875fb31d0dac73c88f3bd502746c473dc1c2b1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106538998"
---
# <a name="spinner"></a>Spinner

Le compteur est un contrôle composite qui se compose d’un bouton d’incrémentation, d’un bouton de décrémentation et d’un contrôle d’édition, qui sont tous utilisés pour fournir des valeurs décimales à l’application.

-   [Détails](#details)
-   [Propriétés du compteur](#spinner-properties)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

La capture d’écran suivante illustre le compteur de ruban.

![capture d’écran d’un contrôle Spinner dans le ruban Windows Live MovieMaker.](images/controls/spinner.png)

## <a name="spinner-properties"></a>Propriétés du compteur

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle Spinner.

En règle générale, une propriété de compteur est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle Spinner.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clé de propriété</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.
<blockquote>
[!Note]<br />
Si la commande associée au contrôle est invalidée via un appel à <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework :: InvalidateUICommand</strong></a>, le Framework interroge cette propriété lorsque <code>UI_INVALIDATIONS_VALUE</code> est passé comme valeur d' <em>indicateurs</em>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
</tbody>
</table>



 

La section de code suivante montre comment différentes propriétés du contrôle Spinner sont mises à jour dans la méthode [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Notes

Si la valeur minimale ([UI hyperdimensionnel \_ \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) d’un compteur est initialisée à 0,0, l’application doit s’assurer que toute valeur suivante fournie par le contrôle n’est pas égale à-0,0 (zéro négatif). Si le compteur fournit la valeur-0,0, l’application doit réinitialiser cette valeur à 0,0 (valeur positive zéro) à l’aide de la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , comme indiqué dans l’exemple suivant d’une méthode [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) pour un contrôle Spinner.

> [!Note]  
> Si ce test n’est pas effectué et que la valeur n’a pas été corrigée, le champ d’édition du contrôle affiche la chaîne « auto ».

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Spinner, élément de balisage**](windowsribbon-element-spinner.md)
</dt> </dl>

