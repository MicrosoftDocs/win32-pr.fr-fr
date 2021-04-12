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
# <a name="persisting-ribbon-state"></a><span data-ttu-id="fe30b-103">Persistance de l’état du ruban</span><span class="sxs-lookup"><span data-stu-id="fe30b-103">Persisting Ribbon State</span></span>

<span data-ttu-id="fe30b-104">Windows Ribon Framework (ruban) offre la possibilité de conserver l’état d’une variété de paramètres utilisateur et de préférences dans les sessions d’application.</span><span class="sxs-lookup"><span data-stu-id="fe30b-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="fe30b-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="fe30b-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fe30b-106">Une expérience prévisible</span><span class="sxs-lookup"><span data-stu-id="fe30b-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="fe30b-107">Enregistrer les paramètres du ruban</span><span class="sxs-lookup"><span data-stu-id="fe30b-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="fe30b-108">Charger les paramètres du ruban</span><span class="sxs-lookup"><span data-stu-id="fe30b-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="fe30b-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe30b-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="fe30b-110">Introduction</span><span class="sxs-lookup"><span data-stu-id="fe30b-110">Introduction</span></span>

<span data-ttu-id="fe30b-111">Divers aspects d’un ruban, y compris les préférences de configuration et d’interaction, peuvent être personnalisés par un utilisateur au moment de l’exécution pour améliorer la convivialité et la productivité.</span><span class="sxs-lookup"><span data-stu-id="fe30b-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="fe30b-112">L’infrastructure du ruban fournit les fonctionnalités permettant de conserver ces paramètres entre les sessions d’application par le biais de deux méthodes définies dans l’implémentation de l’interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) et [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="fe30b-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="fe30b-113">Une expérience prévisible</span><span class="sxs-lookup"><span data-stu-id="fe30b-113">A Predictable Experience</span></span>

<span data-ttu-id="fe30b-114">Les [instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) indiquent que, pour fournir l’expérience utilisateur la plus prévisible possible, les applications du ruban doivent préserver l’état du ruban (à part le dernier onglet sélectionné) lorsque l’application est fermée.</span><span class="sxs-lookup"><span data-stu-id="fe30b-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="fe30b-115">Ainsi, lorsque la même application est lancée, les paramètres et les personnalisations de la session précédente peuvent être restaurés et l’utilisateur peut s’attendre à continuer à interagir avec l’application de la même façon qu’elle l’a laissée.</span><span class="sxs-lookup"><span data-stu-id="fe30b-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="fe30b-116">Les paramètres de ruban qui peuvent être modifiés au moment de l’exécution et conservés d’une session d’application à l’autre sont répertoriés dans le menu contextuel de la commande.</span><span class="sxs-lookup"><span data-stu-id="fe30b-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="fe30b-117">Ils comprennent :</span><span class="sxs-lookup"><span data-stu-id="fe30b-117">They include:</span></span>

-   <span data-ttu-id="fe30b-118">Commandes ajoutées à la liste de commandes de la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fe30b-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="fe30b-119">Spécifié par un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="fe30b-120">La capture d’écran suivante montre la commande de menu contextuel **Ajouter à la barre d’outils accès rapide** .</span><span class="sxs-lookup"><span data-stu-id="fe30b-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="fe30b-122">État d’ancrage de la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="fe30b-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="fe30b-123">Spécifié par la [**valeur \_ CONTROLDOCK de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la clé de propriété [ \_ \_ QuickAccessToolbarDock de l’interface utilisateur](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="fe30b-124">Cette capture d’écran montre la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) à l’emplacement de la barre de titre de l’application par défaut et la **barre d’outils afficher l’accès rapide sous la commande de** menu contextuel du ruban.</span><span class="sxs-lookup"><span data-stu-id="fe30b-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="fe30b-126">Cette capture d’écran montre la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) sous le ruban.</span><span class="sxs-lookup"><span data-stu-id="fe30b-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![capture d’écran de la barre d’outils accès rapide ancrée sous le ruban.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="fe30b-128">État réduit du ruban, tel que spécifié par la valeur booléenne de la clé de propriété [ \_ \_ minimisée de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="fe30b-129">L’État réduit du ruban n’est pas équivalent à l’État réduit du ruban.</span><span class="sxs-lookup"><span data-stu-id="fe30b-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="fe30b-130">En cas d’État réduit, le ruban est complètement masqué et ne peut pas être interagi avec.</span><span class="sxs-lookup"><span data-stu-id="fe30b-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="fe30b-131">L’infrastructure appelle cet État automatiquement si la taille de la fenêtre d’application est réduite, horizontalement ou verticalement, jusqu’au point où le ruban masque l’espace de travail de l’application.</span><span class="sxs-lookup"><span data-stu-id="fe30b-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="fe30b-132">Le Framework restaure le ruban lorsque la taille de la fenêtre d’application est augmentée.</span><span class="sxs-lookup"><span data-stu-id="fe30b-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="fe30b-133">Cette capture d’écran montre la commande **réduire le** menu contextuel du ruban.</span><span class="sxs-lookup"><span data-stu-id="fe30b-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="fe30b-135">Cette capture d’écran montre un ruban réduit.</span><span class="sxs-lookup"><span data-stu-id="fe30b-135">This screen shot shows a minimized ribbon.</span></span>

    ![capture d’écran du ruban Microsoft Paint réduit.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="fe30b-137">Enregistrer les paramètres du ruban</span><span class="sxs-lookup"><span data-stu-id="fe30b-137">Save Ribbon Settings</span></span>

<span data-ttu-id="fe30b-138">La méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) écrit une représentation binaire de l’état persistant du ruban (décrite dans la section précédente) dans un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="fe30b-139">L’application enregistre ensuite le contenu de l’objet IStream dans un fichier ou dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="fe30b-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="fe30b-140">L’exemple suivant montre le code de base requis pour écrire l’état du ruban dans un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) à l’aide de la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


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



## <a name="load-ribbon-settings"></a><span data-ttu-id="fe30b-141">Charger les paramètres du ruban</span><span class="sxs-lookup"><span data-stu-id="fe30b-141">Load Ribbon Settings</span></span>

<span data-ttu-id="fe30b-142">La méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) est utilisée pour récupérer les informations persistantes sur l’état du ruban stockées en tant qu’objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) par la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="fe30b-143">Les informations de l’objet IStream sont appliquées à l’interface ruban lorsque l’application est initialisée.</span><span class="sxs-lookup"><span data-stu-id="fe30b-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="fe30b-144">L’exemple suivant montre le code de base requis pour charger l’état du ruban à partir d’un objet [IStream](/windows/win32/api/objidl/nn-objidl-istream) avec la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


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



<span data-ttu-id="fe30b-145">Pour des performances optimales, la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) doit être appelée à partir de la fonction de rappel [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) pendant la phase d’initialisation du Framework, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fe30b-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


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



<span data-ttu-id="fe30b-146">Plusieurs instances de la même application de Framework du ruban peuvent gérer chaque État du ruban indépendamment en tant qu’objets [IStream](/windows/win32/api/objidl/nn-objidl-istream) séparés ou en tant que groupe via un seul objet IStream.</span><span class="sxs-lookup"><span data-stu-id="fe30b-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="fe30b-147">Lors de la synchronisation de l’état du ruban sur un groupe d’instances d’application, chaque fenêtre de niveau supérieur doit écouter une notification [WM \_ Activate](../inputdev/wm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="fe30b-148">La fenêtre de niveau supérieur désactivée enregistre son état de ruban à l’aide de la méthode [**IUIRibbon :: SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) , et la fenêtre de niveau supérieur en cours d’activation charge son état de ruban à l’aide de la méthode [**IUIRibbon :: LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="fe30b-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe30b-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe30b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe30b-150">Barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="fe30b-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 