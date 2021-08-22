---
title: Affichage du ruban
description: l’infrastructure du ruban Windows expose un ensemble de propriétés qui permettent à une application de spécifier le mode d’affichage de l’interface utilisateur du ruban au moment de l’exécution.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows Ruban, personnalisation des couleurs
- Ruban, personnalisation des couleurs
- personnalisation des couleurs du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b61bae9bae5620d556f26f6c7103ef222f14892c8ce12acd21289dd7bc53b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964431"
---
# <a name="displaying-the-ribbon"></a>Affichage du ruban

l’infrastructure du ruban Windows expose un ensemble de propriétés qui permettent à une application de spécifier le mode d’affichage de l’interface utilisateur du ruban au moment de l’exécution.

-   [Introduction](#introduction)
-   [Réduire le ruban](#minimize-the-ribbon)
-   [Masquer le ruban](#hide-the-ribbon)
-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Pour maximiser la zone disponible pour l’espace de document (ou le port d’affichage) d’une application de Framework de ruban, une application peut spécifier si l’interface utilisateur du ruban est visible ou masquée et, lorsqu’elle est visible, si le ruban est dans un état développé ou réduit.

Les [clés de propriété de Framework](windowsribbon-reference-properties-framework.md) répertoriées dans le tableau suivant sont utilisées pour définir de manière explicite les caractéristiques d’affichage de l’interface utilisateur du ruban dans une application de l’infrastructure du ruban. Ces propriétés n’ont aucun effet sur l’affichage du contrôle contextuel [contexte](windowsribbon-controls-contextpopup.md) .



| État d’affichage         | Clé de propriété du ruban                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Développé ou réduit | [IU-au-dessus \_ \_ minimisé](windowsribbon-reference-properties-uipkey-minimized.md) |
| Visible ou masqué     | [IU de l’interface utilisateur \_ \_ visible](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Réduire le ruban

Une application de Framework de ruban peut définir dynamiquement l’État réduit de la barre de commandes du ruban en affectant à la clé de propriété [ \_ \_ minimisé de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) la valeur **true** ou **false**.



| État d’affichage | Valeur de la clé de propriété |
|---------------|--------------------|
| Développé      | **false**          |
| Collapsed     | **true**           |



 

Lorsque l’interface utilisateur du ruban est dans un État réduit, la ligne de l’onglet du ruban reste visible et entièrement fonctionnelle.

La capture d’écran suivante montre le ruban dans un État réduit.

![capture d’écran montrant l’interface utilisateur du ruban réduite.](images/overviews/ribbon-minimized.png)

> [!Note]  
> L’infrastructure du ruban expose cette fonctionnalité à l’utilisateur final via la sélection « réduire le ruban » du menu contextuel du ruban.

 

## <a name="hide-the-ribbon"></a>Masquer le ruban

Une application de Framework de ruban peut définir dynamiquement l’État affichable de la barre de commandes du ruban en affectant à la clé de propriété [ \_ \_ affichable de l’interface utilisateur](windowsribbon-reference-properties-uipkey-viewable.md) la valeur **true** ou **false**.



| État d’affichage | Valeur de la clé de propriété |
|---------------|--------------------|
| Visible       | **false**          |
| Hidden        | **true**           |



 

Contrairement à la propriété [ \_ \_ minimisée de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) , le paramétrage de l’interface utilisateur de l’IU sur **faux** rend l’interface ruban invisible et complètement inutilisable pour un utilisateur final. [ \_ \_](windowsribbon-reference-properties-uipkey-viewable.md)

La capture d’écran suivante montre le ruban dans un état masqué.

![capture d’écran montrant l’interface utilisateur du ruban masquée.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Exemples

L’exemple suivant montre comment définir l’état de l’interface utilisateur du ruban au moment de l’exécution.

Dans ce cas, la fonction [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) est utilisée pour développer ou réduire l’interface ruban en fonction de l’État bascule d’un [bouton bascule](windowsribbon-controls-togglebutton.md).


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du ruban](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 