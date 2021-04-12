---
title: Persistance de l’état du ruban
description: Windows Ribon Framework (ruban) offre la possibilité de conserver l’état d’une variété de paramètres utilisateur et de préférences dans les sessions d’application.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315762"
---
# <a name="persisting-ribbon-state"></a>Persistance de l’état du ruban

Windows Ribon Framework (ruban) offre la possibilité de conserver l’état d’une variété de paramètres utilisateur et de préférences dans les sessions d’application.

-   [Introduction](#introduction)
-   [Une expérience prévisible](#a-predictable-experience)
-   [Enregistrer les paramètres du ruban](#save-ribbon-settings)
-   [Charger les paramètres du ruban](#load-ribbon-settings)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Divers aspects d’un ruban, y compris les préférences de configuration et d’interaction, peuvent être personnalisés par un utilisateur au moment de l’exécution pour améliorer la convivialité et la productivité. L’infrastructure du ruban fournit les fonctionnalités permettant de conserver ces paramètres entre les sessions d’application par le biais de deux méthodes définies dans l’implémentation de l’interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) et [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Une expérience prévisible

Les [instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) indiquent que, pour fournir l’expérience utilisateur la plus prévisible possible, les applications du ruban doivent préserver l’état du ruban (à part le dernier onglet sélectionné) lorsque l’application est fermée. Ainsi, lorsque la même application est lancée, les paramètres et les personnalisations de la session précédente peuvent être restaurés et l’utilisateur peut s’attendre à continuer à interagir avec l’application de la même façon qu’elle l’a laissée.

Les paramètres de ruban qui peuvent être modifiés au moment de l’exécution et conservés d’une session d’application à l’autre sont répertoriés dans le menu contextuel de la commande. Ils comprennent :

-   Commandes ajoutées à la liste de commandes de la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) par l’utilisateur. Spécifié par un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) .

    La capture d’écran suivante montre la commande de menu contextuel **Ajouter à la barre d’outils accès rapide** .

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   État d’ancrage de la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) par défaut. Spécifié par la [**valeur \_ CONTROLDOCK de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la clé de propriété [ \_ \_ QuickAccessToolbarDock de l’interface utilisateur](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .

    Cette capture d’écran montre la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) à l’emplacement de la barre de titre de l’application par défaut et la **barre d’outils afficher l’accès rapide sous la commande de** menu contextuel du ruban.

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Cette capture d’écran montre la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) sous le ruban.

    ![capture d’écran de la barre d’outils accès rapide ancrée sous le ruban.](images/controls/qat-dockbottom.png)

-   État réduit du ruban, tel que spécifié par la valeur booléenne de la clé de propriété [ \_ \_ minimisée de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) .

    > [!Note]  
    > L’État réduit du ruban n’est pas équivalent à l’État réduit du ruban. En cas d’État réduit, le ruban est complètement masqué et ne peut pas être interagi avec. L’infrastructure appelle cet État automatiquement si la taille de la fenêtre d’application est réduite, horizontalement ou verticalement, jusqu’au point où le ruban masque l’espace de travail de l’application. Le Framework restaure le ruban lorsque la taille de la fenêtre d’application est augmentée.

     

    Cette capture d’écran montre la commande **réduire le** menu contextuel du ruban.

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    Cette capture d’écran montre un ruban réduit.

    ![capture d’écran du ruban Microsoft Paint réduit.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Enregistrer les paramètres du ruban

La méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) écrit une représentation binaire de l’état persistant du ruban (décrite dans la section précédente) dans un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) . L’application enregistre ensuite le contenu de l’objet IStream dans un fichier ou dans le Registre Windows.

L’exemple suivant montre le code de base requis pour écrire l’état du ruban dans un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) à l’aide de la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a>Charger les paramètres du ruban

La méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) est utilisée pour récupérer les informations persistantes sur l’état du ruban stockées en tant qu’objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) par la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) . Les informations de l’objet IStream sont appliquées à l’interface ruban lorsque l’application est initialisée.

L’exemple suivant montre le code de base requis pour charger l’état du ruban à partir d’un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) avec la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



Pour des performances optimales, la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) doit être appelée à partir de la fonction de rappel [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) pendant la phase d’initialisation du Framework, comme illustré dans l’exemple suivant.


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



Plusieurs instances de la même application de Framework du ruban peuvent gérer chaque État du ruban indépendamment en tant qu’objets [IStream](/windows/win32/api/objidl/nn-objidl-istream) séparés ou en tant que groupe via un seul objet IStream.

Lors de la synchronisation de l’état du ruban sur un groupe d’instances d’application, chaque fenêtre de niveau supérieur doit écouter une notification [WM \_ Activate](../inputdev/wm-activate.md) . La fenêtre de niveau supérieur désactivée enregistre son état de ruban à l’aide de la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) , et la fenêtre de niveau supérieur en cours d’activation charge son état de ruban à l’aide de la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 