---
description: Pour obtenir un contrôle plus détaillé sur le comportement de la saisie semi-automatique, ou pour ajouter une source personnalisée de chaînes de saisie semi-automatique, vous devez gérer vous-même l’objet de saisie semi-automatique.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Procédure d’activation manuelle de la saisie semi-automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973158"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="0ee88-103">Procédure d’activation manuelle de la saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="0ee88-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="0ee88-104">Pour obtenir un contrôle plus détaillé sur le comportement de la saisie semi-automatique, ou pour ajouter une source personnalisée de chaînes de saisie semi-automatique, vous devez gérer vous-même l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="0ee88-105">Vous pouvez activer la saisie semi-automatique manuellement de l’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ee88-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="0ee88-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="0ee88-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="0ee88-107">Création d’un objet de saisie semi-automatique simple</span><span class="sxs-lookup"><span data-stu-id="0ee88-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="0ee88-108">Les étapes suivantes montrent comment créer et initialiser un objet de saisie semi-automatique simple.</span><span class="sxs-lookup"><span data-stu-id="0ee88-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="0ee88-109">Un objet de saisie semi-automatique simple effectue des chaînes à partir d’une source unique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="0ee88-110">La vérification des erreurs a été intentionnellement omise dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0ee88-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="0ee88-111">Créez l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="0ee88-112">Créez la source de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-112">Create the autocomplete source.</span></span> <span data-ttu-id="0ee88-113">Vous pouvez utiliser une [source de saisie semi-automatique prédéfinie](ac-ovw.md) ou vous pouvez écrire votre propre source personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0ee88-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="0ee88-114">Le code suivant utilise l’une des sources de saisie semi-automatique prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="0ee88-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="0ee88-115">Le code suivant utilise une source de saisie semi-automatique personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0ee88-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="0ee88-116">Vous pouvez écrire votre propre source de saisie semi-automatique en implémentant un objet qui expose l’interface [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) .</span><span class="sxs-lookup"><span data-stu-id="0ee88-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="0ee88-117">L’objet peut également implémenter les interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) et [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="0ee88-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="0ee88-118">Définissez les options sur la source de saisie semi-automatique (facultatif).</span><span class="sxs-lookup"><span data-stu-id="0ee88-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="0ee88-119">Vous pouvez personnaliser le comportement de la source de saisie semi-automatique en définissant ses options si la source expose l’interface [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .</span><span class="sxs-lookup"><span data-stu-id="0ee88-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="0ee88-120">Lorsque vous utilisez les sources de saisie semi-automatique prédéfinies, seul CLSID \_ ACListISF exporte **IACList2**.</span><span class="sxs-lookup"><span data-stu-id="0ee88-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="0ee88-121">Pour obtenir la liste complète des options et leurs valeurs, consultez [**IACList2 :: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="0ee88-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="0ee88-122">Initialise l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="0ee88-123">Dans cet exemple, **hwndEdit** est le handle de la fenêtre de contrôle d’édition pour laquelle la saisie semi-automatique doit être activée.</span><span class="sxs-lookup"><span data-stu-id="0ee88-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="0ee88-124">Consultez [**IAutoComplete :: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) pour obtenir une description des deux derniers paramètres inutilisés.</span><span class="sxs-lookup"><span data-stu-id="0ee88-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="0ee88-125">Définissez les options de l’objet de saisie semi-automatique (facultatif).</span><span class="sxs-lookup"><span data-stu-id="0ee88-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="0ee88-126">Vous pouvez personnaliser le comportement de l’objet de saisie semi-automatique en définissant ses options.</span><span class="sxs-lookup"><span data-stu-id="0ee88-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="0ee88-127">Pour obtenir la liste complète des options et leurs valeurs, consultez la documentation de [**IACList2 :: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="0ee88-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="0ee88-128">Libère les objets.</span><span class="sxs-lookup"><span data-stu-id="0ee88-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="0ee88-129">L’objet de saisie semi-automatique reste attaché au contrôle d’édition même après sa publication.</span><span class="sxs-lookup"><span data-stu-id="0ee88-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="0ee88-130">Si vous prévoyez d’avoir accès à ces objets ultérieurement, si vous souhaitez modifier les options de saisie semi-automatique ultérieurement, par exemple, il n’est pas nécessaire de les libérer à ce stade.</span><span class="sxs-lookup"><span data-stu-id="0ee88-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="0ee88-131">Création d’un objet de saisie semi-automatique composée</span><span class="sxs-lookup"><span data-stu-id="0ee88-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="0ee88-132">Un objet de saisie semi-automatique composée correspond aux chaînes de plusieurs sources.</span><span class="sxs-lookup"><span data-stu-id="0ee88-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="0ee88-133">Par exemple, la barre d’adresses Windows Internet Explorer utilise un objet de saisie semi-automatique composée, car l’utilisateur peut commencer à taper le nom d’un fichier ou d’une URL.</span><span class="sxs-lookup"><span data-stu-id="0ee88-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="0ee88-134">La plupart des étapes impliquées dans la création d’un objet de saisie semi-automatique composée sont identiques à celles décrites dans la section « création d’un objet à saisie semi-automatique simple ».</span><span class="sxs-lookup"><span data-stu-id="0ee88-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="0ee88-135">Ces étapes sont indiquées comme telles.</span><span class="sxs-lookup"><span data-stu-id="0ee88-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="0ee88-136">Créez l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-136">Create the autocomplete object.</span></span> <span data-ttu-id="0ee88-137">Il s’agit du même que celui de l’étape 1 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="0ee88-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="0ee88-138">Créez le gestionnaire d’objets de source composée automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="0ee88-139">L’objet source composée automatique permet de combiner plusieurs sources de saisie semi-automatique en une seule source de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="0ee88-140">Créez et définissez des options pour chacune des sources de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="0ee88-141">Répétez les étapes 2 et 3 ci-dessus pour chaque source.</span><span class="sxs-lookup"><span data-stu-id="0ee88-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="0ee88-142">Attachez chaque source de saisie semi-automatique au gestionnaire d’objets source.</span><span class="sxs-lookup"><span data-stu-id="0ee88-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="0ee88-143">Initialise l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="0ee88-144">Il s’agit du même que celui de l’étape 4 ci-dessus, mais au lieu de passer la source de saisie semi-automatique simple à [**IAutoComplete :: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), vous transmettez le gestionnaire d’objets source composite.</span><span class="sxs-lookup"><span data-stu-id="0ee88-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="0ee88-145">Définissez les options de l’objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="0ee88-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="0ee88-146">Il s’agit du même que celui de l’étape 5 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="0ee88-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="0ee88-147">Libère les objets.</span><span class="sxs-lookup"><span data-stu-id="0ee88-147">Release the objects.</span></span>

    <span data-ttu-id="0ee88-148">Comme dans le cas simple, vous pouvez libérer les objets dès que vous avez terminé de les utiliser, mais vous pouvez également les conserver pour modifier les options ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0ee88-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
