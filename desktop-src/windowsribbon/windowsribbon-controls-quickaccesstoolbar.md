---
title: Barre d'outils Accès rapide
description: La barre d’outils accès rapide (QAT) est une petite barre d’outils personnalisable qui expose un ensemble de commandes spécifiées par l’application ou sélectionnées par l’utilisateur.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110723"
---
# <a name="quick-access-toolbar"></a>Barre d'outils Accès rapide

La barre d’outils accès rapide (QAT) est une petite barre d’outils personnalisable qui expose un ensemble de commandes spécifiées par l’application ou sélectionnées par l’utilisateur.

- [Introduction](#introduction)
- [Implémenter la barre d’outils accès rapide](#implement-the-quick-access-toolbar)
  - [balisage](#markup)
  - [Code](#code)
- [Persistance de QAT](#qat-persistence)
- [Propriétés de la barre d’outils accès rapide](#quick-access-toolbar-properties)
- [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Par défaut, la barre d’outils accès rapide (QAT) est située dans la barre de titre de la fenêtre d’application, mais elle peut être configurée pour s’afficher sous le ruban. En plus de l’exposition des commandes, la barre d’outils accès rapide (QAT) inclut également un menu déroulant personnalisable qui contient l’ensemble complet des commandes de la barre d’outils accès rapide (QAT) par défaut (masqué ou affiché dans la barre d’outils accès rapide) et un ensemble de la barre d’outils accès rapide (qat) et des options du ruban.

La capture d’écran suivante montre un exemple de la barre d’outils accès rapide du ruban (QAT).

![capture d’écran du qat dans le ruban Microsoft Paint.](images/markup/qat-and-menu.png)

La barre d’outils accès rapide (QAT) est constituée d’une combinaison d’au plus 20 commandes spécifiées par l’application (appelée liste des valeurs par défaut de l’application) ou sélectionnées par l’utilisateur. La barre d’outils accès rapide (QAT) peut contenir des commandes uniques qui ne sont pas disponibles ailleurs dans l’interface ruban.

> [!Note]
> Bien que presque tous les contrôles de ruban autorisent l’ajout de leur commande associée à la barre d’outils accès rapide (QAT) via le menu contextuel affiché dans la capture d’écran suivante, les commandes exposées dans une [fenêtre contextuelle de contexte](windowsribbon-controls-contextpopup.md) ne fournissent pas ce menu contextuel.
>
> ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implémenter la barre d’outils accès rapide

comme avec tous les contrôles Windows framework de ruban, tirer pleinement parti de la barre d’outils accès rapide (QAT) nécessite un composant de balisage qui contrôle sa présentation dans le ruban et un composant de code qui régit ses fonctionnalités.

### <a name="markup"></a>balisage

Le contrôle de la barre d’outils accès rapide (QAT) est déclaré et associé à un ID de commande, dans le balisage par le biais de l’élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) . L’ID de commande est utilisé pour identifier et lier la barre d’outils accès rapide (QAT) à un gestionnaire de commandes défini par l’application.

En plus du gestionnaire de commandes de base pour la fonctionnalité de la barre d’outils accès rapide principale (QAT), la déclaration de l’attribut facultatif de l’élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) *CustomizeCommandName* fait que l’infrastructure ajoute un élément **commandes supplémentaires** à la liste des commandes du menu déroulant de la barre d’outils accès rapide (qat) qui requiert la définition d’un gestionnaire de commandes secondaire.

Pour assurer la cohérence entre les applications du ruban, il est recommandé que le gestionnaire de commandes *CustomizeCommandName* lance une boîte de dialogue de personnalisation de la barre d’outils accès rapide. Étant donné que l’infrastructure de ruban fournit uniquement le point de lancement dans l’interface utilisateur, l’application est uniquement responsable de la mise en œuvre de la boîte de dialogue de personnalisation lorsque la notification de rappel pour cette commande est reçue.

La capture d’écran suivante montre un menu déroulant de barre d’outils accès rapide (QAT) avec l’élément de commande **autres commandes** .

![capture d’écran d’un menu qat avec les commandes supplémentaires... élément de commande.](images/markup/qat-customizecommandname.png)

La liste des valeurs par défaut de l’application pour la barre d’outils accès rapide (QAT) est spécifiée par le biais de la propriété [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , qui identifie une liste par défaut des commandes recommandées, toutes répertoriées dans le menu déroulant de la barre d’outils accès rapide (qat).

Pour afficher les commandes à partir de la liste des valeurs par défaut de l’application dans la barre d’outils de la barre d’outils accès rapide (QAT), l’attribut *ApplicationDefaults. IsChecked* de chaque élément de contrôle doit avoir la valeur `true` . Les images précédentes montrent les résultats de la définition de cet attribut sur `true` pour les commandes **Enregistrer**, **Annuler** et **rétablir** .

[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) prend en charge trois types de contrôles de ruban : [bouton](windowsribbon-controls-button.md), [bouton bascule](windowsribbon-controls-togglebutton.md)et case [à cocher](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 et versions ultérieures : tous les contrôles basés sur la galerie sont pris en charge ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)et [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Les éléments d’un contrôle Gallery peuvent prendre en charge la mise en surbrillance au pointage. Pour prendre en charge la mise en surbrillance au pointage, la Galerie doit être une galerie d’éléments et utiliser un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) de type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).

L’exemple suivant illustre le balisage de base pour un élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .

Cette section de code montre les déclarations de commande pour un élément de la [barre d’outils accès rapide (qat)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Cette section de code montre les déclarations de contrôle pour un élément de la [barre d’outils accès rapide (qat)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a>Code

L’application de l’infrastructure du ruban doit fournir une méthode de rappel du gestionnaire de commandes pour manipuler la barre d’outils accès rapide (QAT). Ce gestionnaire fonctionne de la même façon que les gestionnaires de la bibliothèque de commandes, sauf que la barre d’outils accès rapide (QAT) ne prend pas en charge les catégories. Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).

La collection de commandes de la barre d’outils accès rapide (QAT) est récupérée sous la forme d’un objet [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) . L’ajout de commandes à la barre d’outils accès rapide (QAT) au moment de l’exécution s’effectue en ajoutant un objet [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) à **IUICollection**.

Contrairement aux galeries de commandes, une propriété de type de commande ([UI de l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) n’est pas requise pour l’objet [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) de la barre d’outils accès rapide (qat). Toutefois, la commande doit exister dans la liste des valeurs par défaut de l’application ruban ou barre d’outils accès rapide (QAT). Impossible de créer une nouvelle commande au moment de l’exécution et de l’ajouter à la barre d’outils accès rapide (QAT).

> [!Note]  
> L’application ruban ne peut pas remplacer la barre d’outils accès rapide (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) par un objet de collection personnalisé dérivé de IEnumUnknown.

L’exemple suivant illustre une implémentation du gestionnaire de commandes de la barre d’outils d’accès rapide (QAT) de base.

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a>Persistance de QAT

Les éléments et les paramètres de commande de la barre d’outils accès rapide (QAT) peuvent être rendus persistants entre les sessions d’application à l’aide des fonctions [IUIRibbon :: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) et [IUIRibbon :: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) . Pour plus d’informations, consultez [persistance de l’état du ruban](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Propriétés de la barre d’outils accès rapide

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de la barre d’outils accès rapide (qat).

En règle générale, une propriété de la barre d’outils accès rapide (QAT) est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [IUIFramework :: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [IUICommandHandler :: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [IUICommandHandler :: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [IUIFramework :: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

Le tableau suivant répertorie les clés de propriété associées au contrôle de la barre d’outils accès rapide (QAT).

| Clé de propriété | Remarques |
|---|---|
| [IU de l’IU \_ \_](windowsribbon-reference-properties-uipkey-itemssource.md) | Prend en charge [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (ne prend pas en charge [IUIFramework :: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) retourne un pointeur vers un objet IUICollection qui représente les commandes dans le qat. Chaque commande est identifiée par son ID de commande, qui est obtenu en appelant la méthode [IUISimplePropertySet :: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) et en passant la clé de propriété de l' [interface utilisateur de l’interface utilisateur \_ \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md). |

Aucune clé de propriété n’est associée à l’élément de commande **autres commandes** du menu déroulant de la barre d’outils accès rapide (qat)

## <a name="related-topics"></a>Rubriques connexes

- [Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
- [Élément de balisage QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md)