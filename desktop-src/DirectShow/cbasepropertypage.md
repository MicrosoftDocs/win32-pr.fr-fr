---
description: La classe CBasePropertyPage est une classe abstraite pour l’implémentation d’une page de propriétés. Utilisez cette classe si vous écrivez un filtre (ou un autre objet) qui prend en charge les pages de propriétés.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: CBasePropertyPage, classe (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543847"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="88ea6-104">CBasePropertyPage, classe</span><span class="sxs-lookup"><span data-stu-id="88ea6-104">CBasePropertyPage class</span></span>

![hiérarchie de la classe CBasePropertyPage](images/cprop01.png)

<span data-ttu-id="88ea6-106">La `CBasePropertyPage` classe est une classe abstraite pour l’implémentation d’une page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="88ea6-107">Utilisez cette classe si vous écrivez un filtre (ou un autre objet) qui prend en charge les pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="88ea6-108">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="88ea6-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="88ea6-109">Description</span><span class="sxs-lookup"><span data-stu-id="88ea6-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88ea6-110">**m \_ bDirty**</span><span class="sxs-lookup"><span data-stu-id="88ea6-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="88ea6-111">Indique si l’une des propriétés a changé.</span><span class="sxs-lookup"><span data-stu-id="88ea6-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="88ea6-112">**m \_ DialogId**</span><span class="sxs-lookup"><span data-stu-id="88ea6-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="88ea6-113">Identificateur de ressource pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="88ea6-114">**m \_ DLG**</span><span class="sxs-lookup"><span data-stu-id="88ea6-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="88ea6-115">Handle de la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="88ea6-116">**HWND de m \_**</span><span class="sxs-lookup"><span data-stu-id="88ea6-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="88ea6-117">Handle de la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="88ea6-118">**m \_ pPageSite**</span><span class="sxs-lookup"><span data-stu-id="88ea6-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="88ea6-119">Pointeur vers l’interface **IPropertyPageSite** du site de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="88ea6-120">**m \_ TitleId**</span><span class="sxs-lookup"><span data-stu-id="88ea6-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="88ea6-121">Identificateur de ressource pour une chaîne qui contient le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="88ea6-122">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="88ea6-122">Public Methods</span></span>                                                         | <span data-ttu-id="88ea6-123">Description</span><span class="sxs-lookup"><span data-stu-id="88ea6-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="88ea6-124">**CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="88ea6-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="88ea6-125">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="88ea6-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="88ea6-126">**~ CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="88ea6-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="88ea6-127">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="88ea6-127">Destructor method.</span></span> <span data-ttu-id="88ea6-128">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="88ea6-129">**Activé**</span><span class="sxs-lookup"><span data-stu-id="88ea6-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="88ea6-130">Appelé lorsque la page de propriétés est activée.</span><span class="sxs-lookup"><span data-stu-id="88ea6-130">Called when the property page is activated.</span></span> <span data-ttu-id="88ea6-131">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="88ea6-132">**OnApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="88ea6-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="88ea6-133">Appelé lorsque l’utilisateur applique des modifications à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="88ea6-134">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="88ea6-135">**OnConnect**</span><span class="sxs-lookup"><span data-stu-id="88ea6-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="88ea6-136">Fournit un pointeur **IUnknown** vers l’objet associé à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="88ea6-137">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="88ea6-138">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="88ea6-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="88ea6-139">Appelé lorsque la fenêtre de boîte de dialogue est détruite.</span><span class="sxs-lookup"><span data-stu-id="88ea6-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="88ea6-140">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="88ea6-141">**OnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="88ea6-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="88ea6-142">Appelé lorsque la page de propriétés doit libérer l’objet associé.</span><span class="sxs-lookup"><span data-stu-id="88ea6-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="88ea6-143">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="88ea6-144">**OnReceiveMessage**</span><span class="sxs-lookup"><span data-stu-id="88ea6-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="88ea6-145">Appelé lorsque la boîte de dialogue reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="88ea6-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="88ea6-146">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="88ea6-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="88ea6-147">Méthodes IPropertyPage</span><span class="sxs-lookup"><span data-stu-id="88ea6-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="88ea6-148">Description</span><span class="sxs-lookup"><span data-stu-id="88ea6-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="88ea6-149">**Activer**</span><span class="sxs-lookup"><span data-stu-id="88ea6-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="88ea6-150">Crée la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="88ea6-151">**Appliquer**</span><span class="sxs-lookup"><span data-stu-id="88ea6-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="88ea6-152">Applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="88ea6-153">**Désactivation**</span><span class="sxs-lookup"><span data-stu-id="88ea6-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="88ea6-154">Détruit la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="88ea6-155">**GetPageInfo**</span><span class="sxs-lookup"><span data-stu-id="88ea6-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="88ea6-156">Récupère des informations sur la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="88ea6-157">**Aide**</span><span class="sxs-lookup"><span data-stu-id="88ea6-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="88ea6-158">Appelle l’aide de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="88ea6-159">**IsPageDirty**</span><span class="sxs-lookup"><span data-stu-id="88ea6-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="88ea6-160">Indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à **IPropertyPage :: apply**.</span><span class="sxs-lookup"><span data-stu-id="88ea6-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="88ea6-161">**Activer**</span><span class="sxs-lookup"><span data-stu-id="88ea6-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="88ea6-162">Positionne et redimensionne la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="88ea6-163">**SetObjects**</span><span class="sxs-lookup"><span data-stu-id="88ea6-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="88ea6-164">Fournit des pointeurs **IUnknown** pour les objets associés à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="88ea6-165">**SetPageSite**</span><span class="sxs-lookup"><span data-stu-id="88ea6-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="88ea6-166">Initialise la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="88ea6-167">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="88ea6-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="88ea6-168">Affiche ou masque la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="88ea6-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="88ea6-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="88ea6-170">Indique à la page de propriétés de traiter une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="88ea6-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="88ea6-171">Notes</span><span class="sxs-lookup"><span data-stu-id="88ea6-171">Remarks</span></span>

<span data-ttu-id="88ea6-172">Une page de propriétés étant un objet COM, vous devez générer un GUID pour l’identificateur de classe (CLSID) et fournir une entrée dans le tableau [**CFactoryTemplate**](cfactorytemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="88ea6-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="88ea6-173">Pour plus d’informations, consultez [DirectShow et com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="88ea6-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="88ea6-174">L’exemple suivant illustre une entrée de fabrique de classes typique :</span><span class="sxs-lookup"><span data-stu-id="88ea6-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="88ea6-175">Votre filtre doit exposer l’interface **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="88ea6-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="88ea6-176">Cette interface contient une méthode unique, **GetPages**, qui retourne le CLSID de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="88ea6-177">L’exemple suivant montre comment implémenter cette méthode :</span><span class="sxs-lookup"><span data-stu-id="88ea6-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="88ea6-178">N’oubliez pas de remplacer la méthode **NonDelegatingQueryInterface** du filtre.</span><span class="sxs-lookup"><span data-stu-id="88ea6-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="88ea6-179">Pour plus d’informations, consultez [DirectShow et com](directshow-and-com.md) et [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="88ea6-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="88ea6-180">Ensuite, créez la boîte de dialogue en tant que ressource dans votre projet, puis créez une ressource de type chaîne qui contient le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="88ea6-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="88ea6-181">Ces deux ID de ressource sont des paramètres du constructeur **CBasePropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="88ea6-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="88ea6-182">Si vous conservez la chaîne de titre dans une ressource, il est plus facile de localiser la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88ea6-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="88ea6-183">La classe **CBasePropertyPage** fournit une infrastructure pour l’interface **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="88ea6-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="88ea6-184">Ce Framework appelle plusieurs méthodes virtuelles, notamment [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md), etc.</span><span class="sxs-lookup"><span data-stu-id="88ea6-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="88ea6-185">Dans la classe de base, ces méthodes retournent simplement S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88ea6-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="88ea6-186">Votre classe dérivée doit substituer une partie ou l’ensemble de ces méthodes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="88ea6-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="88ea6-187">Pour plus d’informations, consultez les notes relatives aux différentes méthodes.</span><span class="sxs-lookup"><span data-stu-id="88ea6-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="88ea6-188">Pour obtenir un exemple étendu de l’utilisation de cette classe pour créer une page de propriétés, consultez [création d’une page de propriétés de filtre](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="88ea6-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88ea6-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88ea6-189">Requirements</span></span>



| <span data-ttu-id="88ea6-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88ea6-190">Requirement</span></span> | <span data-ttu-id="88ea6-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="88ea6-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ea6-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="88ea6-192">Header</span></span><br/>  | <dl> <span data-ttu-id="88ea6-193"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ea6-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="88ea6-194">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88ea6-194">Library</span></span><br/> | <dl> <span data-ttu-id="88ea6-195"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88ea6-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




