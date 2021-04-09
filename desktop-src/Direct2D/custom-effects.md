---
title: Effets personnalisés
description: Montre comment écrire vos propres effets personnalisés à l’aide du langage HLSL standard.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102293"
---
# <a name="custom-effects"></a><span data-ttu-id="ae97f-103">Effets personnalisés</span><span class="sxs-lookup"><span data-stu-id="ae97f-103">Custom effects</span></span>

<span data-ttu-id="ae97f-104">[Direct2D](./direct2d-portal.md) est fourni avec une bibliothèque d’effets qui effectuent diverses opérations d’image courantes.</span><span class="sxs-lookup"><span data-stu-id="ae97f-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="ae97f-105">Pour obtenir la liste complète des effets, consultez la rubrique [effets intégrés](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="ae97f-106">Pour les fonctionnalités qui ne peuvent pas être obtenues avec les effets intégrés, Direct2D vous permet d’écrire vos propres effets personnalisés à l’aide du [langage HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)standard.</span><span class="sxs-lookup"><span data-stu-id="ae97f-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="ae97f-107">Vous pouvez utiliser ces effets personnalisés avec les effets intégrés fournis avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ae97f-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="ae97f-108">Pour obtenir des exemples d’un effet complet de nuanceur de pixels, de vertex et de calcul, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ae97f-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ae97f-109">Dans cette rubrique, nous vous montrons les étapes et les concepts dont vous avez besoin pour concevoir et créer un effet personnalisé complet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="ae97f-110">Présentation : qu’est-ce qui se trouve à l’intérieur d’un effet ?</span><span class="sxs-lookup"><span data-stu-id="ae97f-110">Introduction: What is inside an effect?</span></span>

![diagramme des effets d’ombre portée.](images/custom-effects1.png)

<span data-ttu-id="ae97f-112">D’un côté, un effet [Direct2D](./direct2d-portal.md) effectue une tâche de création d’images, telle que la modification de la luminosité, la désaturation d’une image ou, comme illustré ci-dessus, la création d’une ombre portée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="ae97f-113">Pour l’application, elles sont simples.</span><span class="sxs-lookup"><span data-stu-id="ae97f-113">To the app, they are simple.</span></span> <span data-ttu-id="ae97f-114">Ils peuvent accepter zéro ou plusieurs images d’entrée, exposer plusieurs propriétés qui contrôlent leur fonctionnement et générer une seule image de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="ae97f-115">Il existe quatre parties différentes d’un effet personnalisé qui est responsable de l’auteur d’un effet :</span><span class="sxs-lookup"><span data-stu-id="ae97f-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="ae97f-116">Interface Effect : l’interface Effect définit de manière conceptuelle comment une application interagit avec un effet personnalisé (comme le nombre d’entrées acceptées par l’effet et les propriétés disponibles).</span><span class="sxs-lookup"><span data-stu-id="ae97f-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="ae97f-117">L’interface Effect gère un graphique de transformation, qui contient les opérations de création d’images réelles.</span><span class="sxs-lookup"><span data-stu-id="ae97f-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="ae97f-118">Graphique de transformation : chaque effet crée un graphique de transformation interne constitué de transformations individuelles.</span><span class="sxs-lookup"><span data-stu-id="ae97f-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="ae97f-119">Chaque transformation représente une opération d’image unique.</span><span class="sxs-lookup"><span data-stu-id="ae97f-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="ae97f-120">L’effet est responsable de la liaison de ces transformations dans un graphique pour effectuer l’effet de création d’images prévu.</span><span class="sxs-lookup"><span data-stu-id="ae97f-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="ae97f-121">Un effet permet d’ajouter, de supprimer, de modifier et de réorganiser des transformations en réponse à des modifications apportées aux propriétés externes de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="ae97f-122">Transformation : une transformation représente une opération d’image unique.</span><span class="sxs-lookup"><span data-stu-id="ae97f-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="ae97f-123">Son objectif principal est d’héberger les nuanceurs qui sont exécutés pour chaque pixel de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="ae97f-124">À cette fin, il est responsable du calcul de la nouvelle taille de son image de sortie en fonction de la logique dans ses nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="ae97f-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="ae97f-125">Il doit également calculer la zone de son image d’entrée à partir de laquelle les nuanceurs doivent lire pour afficher la région de sortie demandée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="ae97f-126">Nuanceur : un nuanceur est exécuté sur l’entrée de la transformation sur le GPU (ou processeur si le rendu logiciel est spécifié lorsque l’application crée l’appareil Direct3D).</span><span class="sxs-lookup"><span data-stu-id="ae97f-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="ae97f-127">Les nuanceurs d’effet sont écrits en langage[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(High Level Shading Language) et sont compilés en code d’octet pendant la compilation de l’effet, qui est ensuite chargé par l’effet au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ae97f-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="ae97f-128">Ce document de référence décrit comment écrire le langage HLSL conforme à [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="ae97f-129">La documentation Direct3D contient une vue d’ensemble du langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="ae97f-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="ae97f-130">Création d’une interface Effect</span><span class="sxs-lookup"><span data-stu-id="ae97f-130">Creating an effect interface</span></span>

<span data-ttu-id="ae97f-131">L’interface Effect définit la manière dont une application interagit avec l’effet personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ae97f-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="ae97f-132">Pour créer une interface Effect, une classe doit implémenter ID2D1EffectImpl, définir des métadonnées qui décrivent l’effet (par exemple son nom, son nombre d’entrées et ses propriétés) et créer des méthodes qui inscrivent l’effet personnalisé à utiliser avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="ae97f-133">Une fois que tous les composants d’une interface Effect ont été implémentés, l’en-tête de la classe s’affiche comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae97f-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="ae97f-134">Implémenter ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="ae97f-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="ae97f-135">L’interface [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contient trois méthodes que vous devez implémenter :</span><span class="sxs-lookup"><span data-stu-id="ae97f-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="ae97f-136">Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="ae97f-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="ae97f-137">[Direct2D](./direct2d-portal.md) appelle la méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) après que la méthode [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) a été appelée par l’application.</span><span class="sxs-lookup"><span data-stu-id="ae97f-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="ae97f-138">Vous pouvez utiliser cette méthode pour effectuer une initialisation interne ou toute autre opération nécessaire pour l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="ae97f-139">En outre, vous pouvez l’utiliser pour créer le graphique de transformation initial de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="ae97f-140">SetGraph (ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="ae97f-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="ae97f-141">[Direct2D](./direct2d-portal.md) appelle la méthode [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) lorsque le nombre d’entrées à l’effet change.</span><span class="sxs-lookup"><span data-stu-id="ae97f-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="ae97f-142">Alors que la plupart des effets ont un nombre constant d’entrées, d’autres comme l' [effet composite](composite.md) prennent en charge un nombre variable d’entrées.</span><span class="sxs-lookup"><span data-stu-id="ae97f-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="ae97f-143">Cette méthode permet à ces effets de mettre à jour leur graphique de transformation en réponse à un nombre d’entrées variable.</span><span class="sxs-lookup"><span data-stu-id="ae97f-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="ae97f-144">Si un effet ne prend pas en charge un nombre d’entrées de variables, cette méthode peut simplement retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ae97f-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="ae97f-145">PrepareForRender (D2D1 \_ type de modification \_ ChangeType)</span><span class="sxs-lookup"><span data-stu-id="ae97f-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="ae97f-146">La méthode [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) offre la possibilité d’effectuer des opérations en réponse à des modifications externes.</span><span class="sxs-lookup"><span data-stu-id="ae97f-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="ae97f-147">[Direct2D](./direct2d-portal.md) appelle cette méthode juste avant de restituer un effet si au moins l’une d’entre elles est vraie :</span><span class="sxs-lookup"><span data-stu-id="ae97f-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="ae97f-148">L’effet a été précédemment initialisé mais pas encore dessiné.</span><span class="sxs-lookup"><span data-stu-id="ae97f-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="ae97f-149">Une propriété Effect a changé depuis le dernier appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="ae97f-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="ae97f-150">L’état du contexte [Direct2D](./direct2d-portal.md) appelant (comme PPP) a changé depuis le dernier appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="ae97f-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="ae97f-151">Implémenter les méthodes d’inscription et de rappel des effets</span><span class="sxs-lookup"><span data-stu-id="ae97f-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="ae97f-152">Les applications doivent inscrire des effets avec [Direct2D](./direct2d-portal.md) avant de les instancier.</span><span class="sxs-lookup"><span data-stu-id="ae97f-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="ae97f-153">Cette inscription est limitée à une instance d’une fabrique Direct2D et doit être répétée chaque fois que l’application est exécutée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="ae97f-154">Pour activer cette inscription, un effet personnalisé définit un GUID unique, une méthode publique qui enregistre l’effet et une méthode de rappel privée qui retourne une instance de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="ae97f-155">Définir un GUID</span><span class="sxs-lookup"><span data-stu-id="ae97f-155">Define a GUID</span></span>

<span data-ttu-id="ae97f-156">Vous devez définir un GUID qui identifie de façon unique l’effet de l’inscription avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ae97f-157">L’application utilise le même pour identifier l’effet quand elle appelle [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span><span class="sxs-lookup"><span data-stu-id="ae97f-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="ae97f-158">Ce code illustre la définition d’un GUID de ce type pour un effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="ae97f-159">Vous devez créer son propre GUID unique à l’aide d’un outil de génération de GUID, tel que guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="ae97f-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="ae97f-160">Définir une méthode d’inscription publique</span><span class="sxs-lookup"><span data-stu-id="ae97f-160">Define a public registration method</span></span>

<span data-ttu-id="ae97f-161">Ensuite, définissez une méthode publique pour que l’application appelle pour inscrire l’effet avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ae97f-162">Étant donné que l’inscription de l’effet est spécifique à une instance d’une fabrique Direct2D, la méthode accepte une interface [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="ae97f-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="ae97f-163">Pour inscrire l’effet, la méthode appelle ensuite l’API [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) sur le paramètre **ID2D1Factory1** .</span><span class="sxs-lookup"><span data-stu-id="ae97f-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="ae97f-164">Cette API accepte une chaîne XML décrivant les métadonnées, les entrées et les propriétés de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="ae97f-165">Les métadonnées d’un effet sont fournies à titre d’information uniquement et peuvent être interrogées par l’application par le biais de l’interface [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="ae97f-166">Les données d’entrée et de propriété, en revanche, sont utilisées par [Direct2D](./direct2d-portal.md) et représentent les fonctionnalités de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="ae97f-167">Une chaîne XML pour un exemple d’effet minimal est présentée ici.</span><span class="sxs-lookup"><span data-stu-id="ae97f-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="ae97f-168">L’ajout de propriétés personnalisées au XML est traité dans la section Ajout de propriétés personnalisées à un effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="ae97f-169">Définir une méthode de rappel de la fabrique Effect</span><span class="sxs-lookup"><span data-stu-id="ae97f-169">Define an effect factory callback method</span></span>

<span data-ttu-id="ae97f-170">L’effet doit également fournir une méthode de rappel privée qui retourne une instance de l’effet via un seul \* \* paramètre IUnknown.</span><span class="sxs-lookup"><span data-stu-id="ae97f-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="ae97f-171">Un pointeur vers cette méthode est fourni à [Direct2D](./direct2d-portal.md) lorsque l’effet est inscrit via l’API [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) via le paramètre de [**\_ \_ fabrique d’effets PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .</span><span class="sxs-lookup"><span data-stu-id="ae97f-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="ae97f-172">Implémenter l’interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae97f-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="ae97f-173">Enfin, l’effet doit implémenter l’interface IUnknown pour la compatibilité avec COM.</span><span class="sxs-lookup"><span data-stu-id="ae97f-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="ae97f-174">Création du graphique de transformation de l’effet</span><span class="sxs-lookup"><span data-stu-id="ae97f-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="ae97f-175">Un effet peut utiliser plusieurs transformations différentes (opérations d’images individuelles) pour créer l’effet d’image souhaité.</span><span class="sxs-lookup"><span data-stu-id="ae97f-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="ae97f-176">Pour contrôler l’ordre dans lequel ces transformations sont appliquées à l’image d’entrée, l’effet les réorganise dans un graphique de transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="ae97f-177">Un graphique de transformation peut utiliser les effets et les transformations inclus dans [Direct2D](./direct2d-portal.md) , ainsi que les transformations personnalisées créées par l’auteur de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="ae97f-178">Utilisation des transformations incluses avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="ae97f-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="ae97f-179">Il s’agit des transformations les plus couramment utilisées avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="ae97f-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): cette transformation fusionne un nombre arbitraire d’entrées en fonction d’une description de Blend, reportez-vous à la rubrique [**d2d1 \_ Blend \_ Description**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) et à l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) pour les exemples de fusion.</span><span class="sxs-lookup"><span data-stu-id="ae97f-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="ae97f-181">Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="ae97f-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): cette transformation développe la taille de sortie d’une image en fonction [**du \_ \_ mode d’extension d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae97f-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="ae97f-183">Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="ae97f-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): cette transformation décale (traduit) son entrée par un nombre entier de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="ae97f-185">Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="ae97f-186">Tout effet existant peut être traité comme une transformation dans le cadre de la création de graphiques de transformation à l’aide de la méthode [**ID2D1EffectContext :: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="ae97f-187">Création d’un graphique de transformation à nœud unique</span><span class="sxs-lookup"><span data-stu-id="ae97f-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="ae97f-188">Une fois que vous avez créé une transformation, l’entrée de l’effet doit être connectée à l’entrée de la transformation, et la sortie de la transformation doit être connectée à la sortie de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="ae97f-189">Quand un effet ne contient qu’une seule transformation, vous pouvez utiliser la méthode [**ID2D1TransformGraph :: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) pour y parvenir facilement.</span><span class="sxs-lookup"><span data-stu-id="ae97f-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="ae97f-190">Vous pouvez créer ou modifier une transformation dans les méthodes [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) ou [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) de l’effet à l’aide du paramètre ID2D1TransformGraph fourni.</span><span class="sxs-lookup"><span data-stu-id="ae97f-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="ae97f-191">Si un effet doit apporter des modifications au graphique de transformation dans une autre méthode où ce paramètre n’est pas disponible, l’effet peut enregistrer le paramètre [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) en tant que variable membre de la classe et y accéder ailleurs, par exemple [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) ou une méthode de rappel de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="ae97f-192">Un exemple de méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) est illustré ici.</span><span class="sxs-lookup"><span data-stu-id="ae97f-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="ae97f-193">Cette méthode crée un graphique de transformation à nœud unique qui décale l’image de 100 pixels sur chaque axe.</span><span class="sxs-lookup"><span data-stu-id="ae97f-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="ae97f-194">Création d’un graphique de transformation à plusieurs nœuds</span><span class="sxs-lookup"><span data-stu-id="ae97f-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="ae97f-195">L’ajout de plusieurs transformations au graphique de transformation d’un effet permet aux effets d’effectuer en interne plusieurs opérations d’image présentées à une application sous la forme d’un effet unifié unique.</span><span class="sxs-lookup"><span data-stu-id="ae97f-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="ae97f-196">Comme indiqué ci-dessus, le graphique de transformation de l’effet peut être modifié dans toute méthode d’effet à l’aide du paramètre [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) reçu dans la méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="ae97f-197">Les API suivantes de cette interface peuvent être utilisées pour créer ou modifier le graphique de transformation d’un effet :</span><span class="sxs-lookup"><span data-stu-id="ae97f-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="ae97f-198">AddNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="ae97f-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="ae97f-199">La méthode [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , en fait, enregistre la transformation avec l’effet et doit être appelée avant que la transformation puisse être utilisée avec l’une des autres méthodes de graphique de transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="ae97f-200">ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UInt32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="ae97f-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="ae97f-201">La méthode [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) connecte l’entrée d’image de l’effet à l’entrée d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="ae97f-202">La même entrée d’effet peut être connectée à plusieurs transformations.</span><span class="sxs-lookup"><span data-stu-id="ae97f-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="ae97f-203">ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UInt32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="ae97f-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="ae97f-204">La méthode [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) connecte la sortie d’une transformation à l’entrée d’une autre transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="ae97f-205">Une sortie de transformation peut être connectée à plusieurs transformations.</span><span class="sxs-lookup"><span data-stu-id="ae97f-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="ae97f-206">SetOutputNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="ae97f-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="ae97f-207">La méthode [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) connecte la sortie d’une transformation à la sortie de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="ae97f-208">Étant donné qu’un effet n’a qu’une seule sortie, une seule transformation peut être désignée comme « nœud de sortie ».</span><span class="sxs-lookup"><span data-stu-id="ae97f-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="ae97f-209">Ce code utilise deux transformations distinctes pour créer un effet unifié.</span><span class="sxs-lookup"><span data-stu-id="ae97f-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="ae97f-210">Dans ce cas, l’effet est une ombre portée convertie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-210">In this case, the effect is a translated drop shadow.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="ae97f-211">Ajout de propriétés personnalisées à un effet</span><span class="sxs-lookup"><span data-stu-id="ae97f-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="ae97f-212">Les effets peuvent définir des propriétés personnalisées qui permettent à une application de modifier le comportement de l’effet lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ae97f-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="ae97f-213">Il existe trois étapes pour définir une propriété pour un effet personnalisé :</span><span class="sxs-lookup"><span data-stu-id="ae97f-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="ae97f-214">Ajouter les métadonnées de la propriété aux données d’inscription de l’effet</span><span class="sxs-lookup"><span data-stu-id="ae97f-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="ae97f-215">Ajouter une propriété au fichier XML d’inscription</span><span class="sxs-lookup"><span data-stu-id="ae97f-215">Add property to registration XML</span></span>

<span data-ttu-id="ae97f-216">Vous devez définir les propriétés d’un effet personnalisé lors de l’inscription initiale de l’effet avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ae97f-217">Tout d’abord, vous devez mettre à jour le XML d’inscription de l’effet dans sa méthode d’inscription publique avec la nouvelle propriété :</span><span class="sxs-lookup"><span data-stu-id="ae97f-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



<span data-ttu-id="ae97f-218">Quand vous définissez une propriété Effect dans XML, elle a besoin d’un nom, d’un type et d’un nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ae97f-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="ae97f-219">Le nom d’affichage d’une propriété, ainsi que les valeurs de catégorie, d’auteur et de description de l’effet global peuvent et doivent être localisés.</span><span class="sxs-lookup"><span data-stu-id="ae97f-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="ae97f-220">Pour chaque propriété, un effet peut éventuellement spécifier les valeurs par défaut, minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="ae97f-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="ae97f-221">Ces valeurs sont fournies à titre d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="ae97f-221">These values are for informational use only.</span></span> <span data-ttu-id="ae97f-222">Ils ne sont pas appliqués par [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ae97f-223">C’est à vous de mettre en œuvre la logique par défaut/min/max spécifiée dans la classe Effect.</span><span class="sxs-lookup"><span data-stu-id="ae97f-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="ae97f-224">La valeur de type figurant dans le XML pour la propriété doit correspondre au type de données correspondant utilisé par les méthodes getter et setter de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ae97f-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="ae97f-225">Les valeurs XML correspondantes pour chaque type de données sont indiquées dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ae97f-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="ae97f-226">Type de données</span><span class="sxs-lookup"><span data-stu-id="ae97f-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="ae97f-227">Valeur XML correspondante</span><span class="sxs-lookup"><span data-stu-id="ae97f-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="ae97f-228">PWSTR</span><span class="sxs-lookup"><span data-stu-id="ae97f-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="ae97f-229">string</span><span class="sxs-lookup"><span data-stu-id="ae97f-229">string</span></span>                  |
| <span data-ttu-id="ae97f-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="ae97f-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="ae97f-231">bool</span><span class="sxs-lookup"><span data-stu-id="ae97f-231">bool</span></span>                    |
| <span data-ttu-id="ae97f-232">UINT</span><span class="sxs-lookup"><span data-stu-id="ae97f-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="ae97f-233">uint32</span><span class="sxs-lookup"><span data-stu-id="ae97f-233">uint32</span></span>                  |
| <span data-ttu-id="ae97f-234">INT</span><span class="sxs-lookup"><span data-stu-id="ae97f-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="ae97f-235">int32</span><span class="sxs-lookup"><span data-stu-id="ae97f-235">int32</span></span>                   |
| <span data-ttu-id="ae97f-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ae97f-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="ae97f-237">float</span><span class="sxs-lookup"><span data-stu-id="ae97f-237">float</span></span>                   |
| [<span data-ttu-id="ae97f-238">**\_Vecteur D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="ae97f-239">Vector2</span><span class="sxs-lookup"><span data-stu-id="ae97f-239">vector2</span></span>                 |
| [<span data-ttu-id="ae97f-240">**Le \_ vecteur D2D \_ 3F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="ae97f-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="ae97f-241">vector3</span></span>                 |
| [<span data-ttu-id="ae97f-242">**Le \_ vecteur D2D \_ 4F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="ae97f-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="ae97f-243">vector4</span></span>                 |
| <span data-ttu-id="ae97f-244">[**\_Matrice matrice \_ D2D \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="ae97f-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="ae97f-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="ae97f-245">matrix3x2</span></span>               |
| [<span data-ttu-id="ae97f-246">**\_4X3 matrice \_ D2D \_ F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="ae97f-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="ae97f-247">matrix4x3</span></span>               |
| [<span data-ttu-id="ae97f-248">**\_Matrice D2D \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="ae97f-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="ae97f-249">matrix4x4</span></span>               |
| [<span data-ttu-id="ae97f-250">**\_5x4 matrice \_ D2D \_ F**</span><span class="sxs-lookup"><span data-stu-id="ae97f-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="ae97f-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="ae97f-251">matrix5x4</span></span>               |
| <span data-ttu-id="ae97f-252">POIDS\[\]</span><span class="sxs-lookup"><span data-stu-id="ae97f-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="ae97f-253">objet BLOB</span><span class="sxs-lookup"><span data-stu-id="ae97f-253">blob</span></span>                    |
| <span data-ttu-id="ae97f-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="ae97f-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="ae97f-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae97f-255">iunknown</span></span>                |
| <span data-ttu-id="ae97f-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="ae97f-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="ae97f-257">colorcontext</span><span class="sxs-lookup"><span data-stu-id="ae97f-257">colorcontext</span></span>            |
| <span data-ttu-id="ae97f-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="ae97f-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="ae97f-259">clsid</span><span class="sxs-lookup"><span data-stu-id="ae97f-259">clsid</span></span>                   |
| <span data-ttu-id="ae97f-260">Énumération [**( \_ \_ mode d’interpolation d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span><span class="sxs-lookup"><span data-stu-id="ae97f-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="ae97f-261">enum</span><span class="sxs-lookup"><span data-stu-id="ae97f-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="ae97f-262">Mapper la nouvelle propriété à des méthodes getter et setter</span><span class="sxs-lookup"><span data-stu-id="ae97f-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="ae97f-263">Ensuite, l’effet doit mapper cette nouvelle propriété à des méthodes getter et Setter.</span><span class="sxs-lookup"><span data-stu-id="ae97f-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="ae97f-264">Cette opération s’effectue par le biais du tableau de [**\_ \_ liaison de propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) passé dans la méthode [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="ae97f-265">Le tableau de [**\_ \_ liaison de la propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae97f-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



<span data-ttu-id="ae97f-266">Une fois que vous avez créé le tableau de liaisons et XML, transmettez-les à la méthode [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :</span><span class="sxs-lookup"><span data-stu-id="ae97f-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="ae97f-267">La \_ macro de liaison de type valeur d2d1 \_ \_ requiert que la classe Effect hérite de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) avant toute autre interface.</span><span class="sxs-lookup"><span data-stu-id="ae97f-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="ae97f-268">Les propriétés personnalisées d’un effet sont indexées dans l’ordre dans lequel elles sont déclarées dans le code XML, et une fois créées est accessible par l’application à l’aide des méthodes [**ID2D1Properties :: SetValue**](id2d1properties-setvalue-overload.md) et [**ID2D1Properties :: GetValue**](id2d1properties-getvalue-overload.md) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="ae97f-269">Pour plus de commodité, vous pouvez créer une énumération publique qui répertorie chaque propriété dans le fichier d’en-tête de l’effet :</span><span class="sxs-lookup"><span data-stu-id="ae97f-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="ae97f-270">Créer les méthodes getter et setter pour la propriété</span><span class="sxs-lookup"><span data-stu-id="ae97f-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="ae97f-271">L’étape suivante consiste à créer les méthodes getter et setter pour la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="ae97f-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="ae97f-272">Les noms des méthodes doivent correspondre à ceux spécifiés dans le tableau de [**\_ \_ liaison de propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="ae97f-273">En outre, le type de propriété spécifié dans le XML de l’effet doit correspondre au type du paramètre de la méthode setter et à la valeur de retour de la méthode d’accesseur Get.</span><span class="sxs-lookup"><span data-stu-id="ae97f-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="ae97f-274">Mettre à jour les transformations de l’effet en réponse à une modification de propriété</span><span class="sxs-lookup"><span data-stu-id="ae97f-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="ae97f-275">Pour mettre à jour la sortie d’image d’un effet en réponse à une modification de propriété, l’effet doit modifier ses transformations sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="ae97f-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="ae97f-276">Cette opération s’effectue généralement dans la méthode [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) de l’effet que [Direct2D](./direct2d-portal.md) appelle automatiquement quand l’une des propriétés d’un effet a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="ae97f-277">Toutefois, les transformations peuvent être mises à jour dans n’importe laquelle des méthodes de l’effet : par exemple, Initialize ou les méthodes setter de propriété de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="ae97f-278">Par exemple, si un effet contenait un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) et souhaite modifier sa valeur de décalage en réponse à la propriété offset de l’effet en cours de modification, il ajouterait le code suivant dans [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span><span class="sxs-lookup"><span data-stu-id="ae97f-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a><span data-ttu-id="ae97f-279">Création d’une transformation personnalisée</span><span class="sxs-lookup"><span data-stu-id="ae97f-279">Creating a custom transform</span></span>

<span data-ttu-id="ae97f-280">Pour implémenter des opérations d’image au-delà de ce qui est fourni dans [Direct2D](./direct2d-portal.md), vous devez implémenter des transformations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ae97f-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="ae97f-281">Les transformations personnalisées peuvent modifier arbitrairement une image d’entrée à l’aide d’un nuanceur HLSL personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ae97f-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="ae97f-282">Les transformations implémentent l’une des deux interfaces différentes selon les types de nuanceurs qu’elles utilisent.</span><span class="sxs-lookup"><span data-stu-id="ae97f-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="ae97f-283">Les transformations utilisant des nuanceurs de pixels et/ou vertex doivent implémenter [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), tandis que les transformations utilisant des nuanceurs de calcul doivent implémenter [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span><span class="sxs-lookup"><span data-stu-id="ae97f-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="ae97f-284">Ces interfaces héritent toutes deux de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="ae97f-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="ae97f-285">Cette section se concentre sur l’implémentation des fonctionnalités communes aux deux.</span><span class="sxs-lookup"><span data-stu-id="ae97f-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="ae97f-286">L’interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) a quatre méthodes à implémenter :</span><span class="sxs-lookup"><span data-stu-id="ae97f-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="ae97f-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="ae97f-287">GetInputCount</span></span>

<span data-ttu-id="ae97f-288">Cette méthode retourne un entier représentant le nombre d’entrées pour la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="ae97f-289">MapInputRectsToOutputRect</span><span class="sxs-lookup"><span data-stu-id="ae97f-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="ae97f-290">[Direct2D](./direct2d-portal.md) appelle la méthode [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) chaque fois que la transformation est rendue.</span><span class="sxs-lookup"><span data-stu-id="ae97f-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="ae97f-291">Direct2D passe un rectangle représentant les limites de chacune des entrées à la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="ae97f-292">La transformation est ensuite chargée de calculer les limites de l’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="ae97f-293">La taille des rectangles pour toutes les méthodes sur cette interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) est définie en pixels, et non en DIP.</span><span class="sxs-lookup"><span data-stu-id="ae97f-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="ae97f-294">Cette méthode est également chargée de calculer la région de la sortie opaque en fonction de la logique de son nuanceur et des zones opaques de chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="ae97f-295">Une région opaque d’une image est définie comme étant celle où le canal alpha est « 1 » pour l’intégralité du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ae97f-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="ae97f-296">S’il est impossible de savoir si la sortie d’une transformation est opaque, le rectangle opaque de sortie doit être défini sur (0, 0, 0, 0) comme valeur sûre.</span><span class="sxs-lookup"><span data-stu-id="ae97f-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="ae97f-297">[Direct2D](./direct2d-portal.md) utilise ces informations pour effectuer des optimisations de rendu avec un contenu « opaque » garanti.</span><span class="sxs-lookup"><span data-stu-id="ae97f-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="ae97f-298">Si cette valeur est incorrecte, elle peut entraîner un rendu incorrect.</span><span class="sxs-lookup"><span data-stu-id="ae97f-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="ae97f-299">Vous pouvez modifier le comportement de rendu de la transformation (comme défini dans les sections 6 à 8) au cours de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ae97f-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="ae97f-300">Toutefois, vous ne pouvez pas modifier d’autres transformations dans le graphique de transformation ou la disposition du graphique elle-même ici.</span><span class="sxs-lookup"><span data-stu-id="ae97f-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



<span data-ttu-id="ae97f-301">Pour obtenir un exemple plus complexe, réfléchissez à la façon dont une opération de flou simple serait représentée :</span><span class="sxs-lookup"><span data-stu-id="ae97f-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="ae97f-302">Si une opération de flou utilise un rayon de 5 pixels, la taille du rectangle de sortie doit être développée de 5 pixels, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ae97f-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="ae97f-303">Lors de la modification des coordonnées d’un rectangle, une transformation doit garantir que sa logique ne provoque pas de dépassement de capacité ou de dépassement de capacité dans les coordonnées du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ae97f-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



<span data-ttu-id="ae97f-304">Étant donné que l’image est floue, une zone de l’image opaque peut désormais être partiellement transparente.</span><span class="sxs-lookup"><span data-stu-id="ae97f-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="ae97f-305">Cela est dû au fait que la zone en dehors de l’image est définie par défaut sur le noir transparent et que cette transparence est fusionnée dans l’image autour des bords.</span><span class="sxs-lookup"><span data-stu-id="ae97f-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="ae97f-306">La transformation doit refléter cela dans ses calculs de rectangle opaque de sortie :</span><span class="sxs-lookup"><span data-stu-id="ae97f-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="ae97f-307">Ces calculs sont visualisés ici :</span><span class="sxs-lookup"><span data-stu-id="ae97f-307">These calculations are visualized here:</span></span>

![illustration du calcul du rectangle.](images/custom-effects2.png)

<span data-ttu-id="ae97f-309">Pour plus d’informations sur cette méthode, consultez la page de référence [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="ae97f-310">MapOutputRectToInputRects</span><span class="sxs-lookup"><span data-stu-id="ae97f-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="ae97f-311">[Direct2D](./direct2d-portal.md) appelle la méthode [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) après [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ae97f-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="ae97f-312">La transformation doit calculer la partie de l’image à partir de laquelle elle doit lire afin de restituer correctement la région de sortie demandée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="ae97f-313">Comme précédemment, si un effet mappe strictement les pixels 1-1, il peut passer le rectangle de sortie au rectangle d’entrée :</span><span class="sxs-lookup"><span data-stu-id="ae97f-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



<span data-ttu-id="ae97f-314">De même, si une transformation réduit ou développe une image (comme l’exemple de flou ici), les pixels utilisent souvent des pixels environnants pour calculer leur valeur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="ae97f-315">Avec un flou, la moyenne d’un pixel est calculée avec ses pixels environnants, même s’ils sont en dehors des limites de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="ae97f-316">Ce comportement est reflété dans le calcul.</span><span class="sxs-lookup"><span data-stu-id="ae97f-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="ae97f-317">Comme précédemment, la transformation recherche les dépassements de capacité lors du développement des coordonnées d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="ae97f-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="ae97f-318">Ce schéma visualise le calcul.</span><span class="sxs-lookup"><span data-stu-id="ae97f-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="ae97f-319">[Direct2D](./direct2d-portal.md) échantillonne automatiquement les pixels noirs transparents lorsque l’image d’entrée n’existe pas, ce qui permet une fusion progressive du flou avec le contenu existant à l’écran.</span><span class="sxs-lookup"><span data-stu-id="ae97f-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![illustration d’un effet d’échantillonnage de pixels noirs transparents en dehors d’un rectangle.](images/custom-effects3.png)

<span data-ttu-id="ae97f-321">Si le mappage n’est pas trivial, cette méthode doit définir le rectangle d’entrée sur la zone maximale pour garantir des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="ae97f-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="ae97f-322">Pour ce faire, définissez les bords gauche et supérieur sur INT \_ min, et les bords droits et inférieurs sur int \_ Max.</span><span class="sxs-lookup"><span data-stu-id="ae97f-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="ae97f-323">Pour plus d’informations sur cette méthode, consultez la rubrique [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="ae97f-324">MapInvalidRect</span><span class="sxs-lookup"><span data-stu-id="ae97f-324">MapInvalidRect</span></span>

<span data-ttu-id="ae97f-325">[Direct2D](./direct2d-portal.md) appelle également la méthode [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="ae97f-326">Toutefois, contrairement aux méthodes [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) et [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , Direct2D n’est pas garanti de l’appeler à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="ae97f-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="ae97f-327">Cette méthode détermine de manière conceptuelle la partie de la sortie d’une transformation qui doit être restituée de nouveau en réponse à une partie ou à la totalité de son entrée en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="ae97f-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="ae97f-328">Il existe trois scénarios différents pour lesquels calculer un Rect non valide dans une transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="ae97f-329">Transformations avec mappage de pixels un-à-un</span><span class="sxs-lookup"><span data-stu-id="ae97f-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="ae97f-330">Pour les transformations qui mappent les pixels 1-1, transmettez simplement le rectangle d’entrée non valide à dans le rectangle de sortie non valide :</span><span class="sxs-lookup"><span data-stu-id="ae97f-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="ae97f-331">Transformations avec mappage de pixels plusieurs-à-plusieurs</span><span class="sxs-lookup"><span data-stu-id="ae97f-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="ae97f-332">Lorsque les pixels de sortie d’une transformation dépendent de leur zone environnante, le rectangle d’entrée non valide doit être développé en conséquence.</span><span class="sxs-lookup"><span data-stu-id="ae97f-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="ae97f-333">Cela permet de tenir compte du fait que les pixels entourant le rectangle d’entrée non valide seront également affectés et deviendront non valides.</span><span class="sxs-lookup"><span data-stu-id="ae97f-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="ae97f-334">Par exemple, un flou de cinq pixels utilise le calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="ae97f-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="ae97f-335">Transformations avec mappage de pixels complexe</span><span class="sxs-lookup"><span data-stu-id="ae97f-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="ae97f-336">Pour les transformations où les pixels d’entrée et de sortie n’ont pas de mappage simple, la totalité de la sortie peut être marquée comme étant non valide.</span><span class="sxs-lookup"><span data-stu-id="ae97f-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="ae97f-337">Par exemple, si une transformation renvoie simplement la couleur moyenne de l’entrée, la totalité de la sortie de la transformation change si même une petite partie de l’entrée est modifiée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="ae97f-338">Dans ce cas, le rectangle de sortie non valide doit être défini sur un rectangle infini logiquement (indiqué ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="ae97f-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="ae97f-339">[Direct2D](./direct2d-portal.md) fixe automatiquement ce à la limite de la sortie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="ae97f-340">Pour plus d’informations sur cette méthode, consultez la rubrique [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="ae97f-341">Une fois que ces méthodes ont été implémentées, l’en-tête de votre transformation contient ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ae97f-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="ae97f-342">Ajout d’un nuanceur de pixels à une transformation personnalisée</span><span class="sxs-lookup"><span data-stu-id="ae97f-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="ae97f-343">Une fois qu’une transformation a été créée, elle doit fournir un nuanceur qui va manipuler les pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="ae97f-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="ae97f-344">Cette section décrit les étapes d’utilisation d’un nuanceur de pixels avec une transformation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="ae97f-345">Implémentation de ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="ae97f-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="ae97f-346">Pour utiliser un nuanceur de pixels, la transformation doit implémenter l’interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , qui hérite de l’interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) décrite dans la section 5.</span><span class="sxs-lookup"><span data-stu-id="ae97f-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="ae97f-347">Cette interface contient une nouvelle méthode à implémenter :</span><span class="sxs-lookup"><span data-stu-id="ae97f-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="ae97f-348">SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)</span><span class="sxs-lookup"><span data-stu-id="ae97f-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="ae97f-349">[Direct2D](./direct2d-portal.md) appelle la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quand la transformation est ajoutée pour la première fois au graphique de transformation d’un effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="ae97f-350">Cette méthode fournit un paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) qui contrôle le mode de rendu de la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="ae97f-351">Consultez la rubrique **ID2D1DrawInfo** pour connaître les méthodes disponibles ici.</span><span class="sxs-lookup"><span data-stu-id="ae97f-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="ae97f-352">Si la transformation choisit de stocker ce paramètre en tant que variable de membre de classe, l’objet *drawInfo* est accessible et modifié à partir d’autres méthodes telles que les accesseurs set de propriété ou [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ae97f-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="ae97f-353">En particulier, il ne peut pas être appelé à partir des méthodes [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) ou [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) sur [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="ae97f-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="ae97f-354">Création d’un GUID pour le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ae97f-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="ae97f-355">Ensuite, la transformation doit définir un GUID unique pour le nuanceur de pixels lui-même.</span><span class="sxs-lookup"><span data-stu-id="ae97f-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="ae97f-356">Cette valeur est utilisée lorsque [Direct2D](./direct2d-portal.md) charge le nuanceur en mémoire, ainsi que lorsque la transformation choisit le nuanceur de pixels à utiliser pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ae97f-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="ae97f-357">Des outils tels que guidgen.exe, qui sont inclus dans Visual Studio, peuvent être utilisés pour générer un GUID aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ae97f-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="ae97f-358">Chargement du nuanceur de pixels avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="ae97f-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="ae97f-359">Un nuanceur de pixels doit être chargé en mémoire avant de pouvoir être utilisé par la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="ae97f-360">Pour charger le nuanceur de pixels en mémoire, la transformation doit lire le code d’octet du nuanceur compilé à partir du. Fichier CSO généré par Visual Studio (consultez la documentation [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pour plus d’informations) dans un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="ae97f-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="ae97f-361">Cette technique est illustrée en détail dans l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ae97f-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ae97f-362">Une fois que les données du nuanceur ont été chargées dans un tableau d’octets, appelez la méthode [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) sur l’objet [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="ae97f-363">[Direct2D](./direct2d-portal.md) ignore les appels à **LoadPixelShader** lorsqu’un shader avec le même GUID a déjà été chargé.</span><span class="sxs-lookup"><span data-stu-id="ae97f-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="ae97f-364">Une fois qu’un nuanceur de pixels a été chargé en mémoire, la transformation doit la sélectionner pour l’exécution en passant son GUID à la méthode [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fourni pendant la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="ae97f-365">Le nuanceur de pixels doit être déjà chargé en mémoire avant d’être sélectionné pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ae97f-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="ae97f-366">Modification de l’opération de nuanceur avec des mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="ae97f-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="ae97f-367">Pour modifier le mode d’exécution d’un nuanceur, une transformation peut passer une mémoire tampon constante au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="ae97f-368">Pour ce faire, une transformation définit un struct qui contient les variables souhaitées dans l’en-tête de classe :</span><span class="sxs-lookup"><span data-stu-id="ae97f-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="ae97f-369">La transformation appelle ensuite la méthode [**ID2D1DrawInfo :: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fourni dans la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) pour passer cette mémoire tampon au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="ae97f-370">Le [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) doit également définir une structure correspondante qui représente la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ae97f-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="ae97f-371">Les variables contenues dans le struct du nuanceur doivent correspondre à celles de la structure de la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="ae97f-372">Une fois la mémoire tampon définie, les valeurs contenues dans peuvent être lues à partir de n’importe où dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="ae97f-373">Écriture d’un nuanceur de pixels pour Direct2D</span><span class="sxs-lookup"><span data-stu-id="ae97f-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="ae97f-374">Les transformations [Direct2D](./direct2d-portal.md) utilisent des nuanceurs créés à l’aide du [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)standard.</span><span class="sxs-lookup"><span data-stu-id="ae97f-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="ae97f-375">Toutefois, il existe quelques concepts clés pour l’écriture d’un nuanceur de pixels qui s’exécute à partir du contexte d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="ae97f-376">Pour obtenir un exemple complet d’un nuanceur de pixels entièrement fonctionnel, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ae97f-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ae97f-377">[Direct2D](./direct2d-portal.md) mappe automatiquement les entrées d’une transformation aux objets [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) dans le langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="ae97f-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="ae97f-378">Le premier **Texture2D** se trouve à l’emplacement de Registre T0 et le premier **SamplerState** se trouve dans le registre S0.</span><span class="sxs-lookup"><span data-stu-id="ae97f-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="ae97f-379">Chaque entrée supplémentaire se trouve dans les registres correspondants suivants (T1 et S1, par exemple).</span><span class="sxs-lookup"><span data-stu-id="ae97f-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="ae97f-380">Les données de pixels d’une entrée particulière peuvent être échantillonnées en appelant l’exemple sur l’objet **Texture2D** et en passant l’objet **SamplerState** correspondant et les coordonnées Texel.</span><span class="sxs-lookup"><span data-stu-id="ae97f-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="ae97f-381">Un nuanceur de pixels personnalisé est exécuté une fois pour chaque pixel rendu.</span><span class="sxs-lookup"><span data-stu-id="ae97f-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="ae97f-382">Chaque fois que le nuanceur est exécuté, [Direct2D](./direct2d-portal.md) fournit automatiquement trois paramètres qui identifient sa position d’exécution actuelle :</span><span class="sxs-lookup"><span data-stu-id="ae97f-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="ae97f-383">Sortie de l’espace de scène : ce paramètre représente la position d’exécution actuelle en termes de la surface cible globale.</span><span class="sxs-lookup"><span data-stu-id="ae97f-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="ae97f-384">Elle est définie en pixels et ses valeurs min/max correspondent aux limites du rectangle retourné par [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ae97f-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="ae97f-385">Sortie d’espace : ce paramètre est utilisé par Direct3D et ne doit pas être utilisé dans le nuanceur de pixels d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="ae97f-386">Texel-entrée d’espace : ce paramètre représente la position d’exécution actuelle dans une texture d’entrée particulière.</span><span class="sxs-lookup"><span data-stu-id="ae97f-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="ae97f-387">Un nuanceur ne doit pas prendre de dépendances quant à la façon dont cette valeur est calculée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="ae97f-388">Elle ne doit l’utiliser que pour échantillonner l’entrée du nuanceur de pixels, comme illustré dans le code ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ae97f-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="ae97f-389">Ajout d’un nuanceur de sommets à une transformation personnalisée</span><span class="sxs-lookup"><span data-stu-id="ae97f-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="ae97f-390">Vous pouvez utiliser des nuanceurs de vertex pour atteindre différents scénarios d’acquisition d’images que les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="ae97f-391">En particulier, les nuanceurs de vertex peuvent exécuter des effets d’images géométriques en transformant des vertex qui composent une image.</span><span class="sxs-lookup"><span data-stu-id="ae97f-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="ae97f-392">Les nuanceurs vertex peuvent être utilisés indépendamment de ou conjointement aux nuanceurs de pixels spécifiés par la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="ae97f-393">Si aucun nuanceur vertex n’est spécifié, [Direct2D](./direct2d-portal.md) remplace un nuanceur de sommets par défaut par le nuanceur de pixels personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ae97f-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="ae97f-394">Le processus d’ajout d’un nuanceur de sommets à une transformation personnalisée est semblable à celui d’un nuanceur de pixels : la transformation implémente l’interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crée un GUID et (éventuellement) passe des mémoires tampons constantes au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="ae97f-395">Toutefois, il existe quelques étapes supplémentaires clés propres aux nuanceurs de vertex :</span><span class="sxs-lookup"><span data-stu-id="ae97f-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="ae97f-396">Création d’une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="ae97f-396">Creating a vertex buffer</span></span>

<span data-ttu-id="ae97f-397">Un nuanceur de sommets par définition s’exécute sur les vertex qui lui sont passés, et non sur des pixels individuels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="ae97f-398">Pour spécifier les vertex sur lesquels le nuanceur doit s’exécuter, une transformation crée une mémoire tampon de vertex à passer au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="ae97f-399">La disposition des mémoires tampons de vertex n’est pas traitée dans ce document.</span><span class="sxs-lookup"><span data-stu-id="ae97f-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="ae97f-400">Pour plus d’informations, consultez la [référence de Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou l’exemple de [Kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour un exemple d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="ae97f-401">Après avoir créé une mémoire tampon de vertex en mémoire, la transformation utilise la méthode [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) sur l’objet [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) de l’effet conteneur pour transmettre ces données au GPU.</span><span class="sxs-lookup"><span data-stu-id="ae97f-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="ae97f-402">Là encore, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour obtenir un exemple d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="ae97f-403">Si aucune mémoire tampon de vertex n’est spécifiée par la transformation, [Direct2D](./direct2d-portal.md) passe une mémoire tampon de vertex par défaut représentant l’emplacement rectangulaire de l’image.</span><span class="sxs-lookup"><span data-stu-id="ae97f-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="ae97f-404">Modification de SetDrawInfo pour utiliser un nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ae97f-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="ae97f-405">Comme avec les nuanceurs de pixels, la transformation doit charger et sélectionner un nuanceur de sommets pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ae97f-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="ae97f-406">Pour charger le nuanceur de sommets, il appelle la méthode [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) sur la méthode [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) reçue dans la méthode Initialize de l’effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="ae97f-407">Pour sélectionner le nuanceur de sommets pour l’exécution, il appelle [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) reçu dans la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) de la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="ae97f-408">Cette méthode accepte un GUID pour un nuanceur de sommets chargé précédemment, ainsi qu’une mémoire tampon de vertex précédemment créée pour le nuanceur à exécuter.</span><span class="sxs-lookup"><span data-stu-id="ae97f-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="ae97f-409">Implémentation d’un nuanceur de sommets Direct2D</span><span class="sxs-lookup"><span data-stu-id="ae97f-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="ae97f-410">Une transformation de dessin peut contenir à la fois un nuanceur de pixels et un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ae97f-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="ae97f-411">Si une transformation définit à la fois un nuanceur de pixels et un nuanceur de sommets, la sortie du nuanceur de sommets est directement donnée au nuanceur de pixels : l’application peut personnaliser la signature de retour du nuanceur de sommets/les paramètres du nuanceur de pixels tant qu’ils sont cohérents.</span><span class="sxs-lookup"><span data-stu-id="ae97f-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="ae97f-412">En revanche, si une transformation contient uniquement un nuanceur de sommets et s’appuie sur le nuanceur de pixels direct de [Direct2D](./direct2d-portal.md)par défaut, elle doit retourner la sortie par défaut suivante :</span><span class="sxs-lookup"><span data-stu-id="ae97f-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="ae97f-413">Un nuanceur de sommets stocke le résultat de ses transformations de vertex dans la variable de sortie d’espace de scène du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="ae97f-414">Pour calculer la sortie d’espace et les variables d’entrée d’espace de Texel, [Direct2D](./direct2d-portal.md) fournit automatiquement des matrices de conversion dans une mémoire tampon constante :</span><span class="sxs-lookup"><span data-stu-id="ae97f-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



<span data-ttu-id="ae97f-415">Vous trouverez ci-dessous un exemple de code de nuanceur de vertex qui utilise les matrices de conversion pour calculer le clip correct et les espaces texels attendus par [Direct2D](./direct2d-portal.md):</span><span class="sxs-lookup"><span data-stu-id="ae97f-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



<span data-ttu-id="ae97f-416">Le code ci-dessus peut être utilisé comme point de départ pour un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ae97f-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="ae97f-417">Elle passe simplement par l’image d’entrée sans effectuer de transformations.</span><span class="sxs-lookup"><span data-stu-id="ae97f-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="ae97f-418">Là encore, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour une transformation entièrement implémentée basée sur un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ae97f-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="ae97f-419">Si aucune mémoire tampon de vertex n’est spécifiée par la transformation, [Direct2D](./direct2d-portal.md) remplace dans une mémoire tampon de vertex par défaut qui représente l’emplacement rectangulaire de l’image.</span><span class="sxs-lookup"><span data-stu-id="ae97f-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="ae97f-420">Les paramètres du nuanceur de sommets sont remplacés par ceux de la sortie du nuanceur par défaut :</span><span class="sxs-lookup"><span data-stu-id="ae97f-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="ae97f-421">Le nuanceur vertex ne peut pas modifier ses paramètres *sceneSpaceOutput* et *clipSpaceOutput* .</span><span class="sxs-lookup"><span data-stu-id="ae97f-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="ae97f-422">Elle doit les retourner inchangées.</span><span class="sxs-lookup"><span data-stu-id="ae97f-422">It must return them unchanged.</span></span> <span data-ttu-id="ae97f-423">Toutefois, il peut modifier le (s) paramètre (s) *texelSpaceInput* pour chaque image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="ae97f-424">Si la transformation contient également un nuanceur de pixels personnalisé, le nuanceur de sommets peut toujours passer des paramètres personnalisés supplémentaires directement au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="ae97f-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="ae97f-425">En outre, la mémoire tampon personnalisée des matrices de conversion *sceneSpace* (B0) n’est plus fournie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="ae97f-426">Ajout d’un nuanceur de calcul à une transformation personnalisée</span><span class="sxs-lookup"><span data-stu-id="ae97f-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="ae97f-427">Enfin, les transformations personnalisées peuvent utiliser des nuanceurs de calcul pour certains scénarios ciblés.</span><span class="sxs-lookup"><span data-stu-id="ae97f-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="ae97f-428">Les nuanceurs de calcul peuvent être utilisés pour implémenter des effets d’images complexes qui nécessitent un accès arbitraire aux mémoires tampons d’images d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae97f-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="ae97f-429">Par exemple, un algorithme d’histogramme de base ne peut pas être implémenté avec un nuanceur de pixels en raison des limitations de l’accès à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ae97f-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="ae97f-430">Étant donné que les nuanceurs de calcul présentent des exigences de niveau de matériel supérieures à celles des nuanceurs de pixels, les nuanceurs de pixels doivent être utilisés dans la mesure du possible pour implémenter un effet donné.</span><span class="sxs-lookup"><span data-stu-id="ae97f-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="ae97f-431">Plus précisément, les nuanceurs de calcul s’exécutent uniquement sur la plupart des cartes de niveau DirectX 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ae97f-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="ae97f-432">Si une transformation choisit d’utiliser un nuanceur de calcul, il doit vérifier la prise en charge matérielle appropriée lors de l’instanciation en plus de l’implémentation de l’interface [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="ae97f-433">Vérification de la prise en charge du nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="ae97f-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="ae97f-434">Si un effet utilise un nuanceur de calcul, il doit vérifier la prise en charge du nuanceur de calcul lors de sa création à l’aide de la méthode [**ID2D1EffectContext :: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="ae97f-435">Si le GPU ne prend pas en charge les nuanceurs de calcul, l’effet doit retourner [**D2DERR \_ \_ \_ fonctionnalités d’appareil insuffisantes**](direct2d-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ae97f-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="ae97f-436">Il existe deux types différents de nuanceurs de calcul qu’une transformation peut utiliser : Shader Model 4 (DirectX 10) et Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="ae97f-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="ae97f-437">Il existe certaines limitations aux nuanceurs du modèle de nuanceur 4.</span><span class="sxs-lookup"><span data-stu-id="ae97f-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="ae97f-438">Pour plus d’informations, consultez la documentation de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="ae97f-439">Les transformations peuvent contenir des types de nuanceurs et peuvent revenir au nuanceur modèle 4 quand cela est nécessaire : consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour une implémentation de ce.</span><span class="sxs-lookup"><span data-stu-id="ae97f-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="ae97f-440">Implémenter ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="ae97f-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="ae97f-441">Cette interface contient deux nouvelles méthodes à implémenter, en plus de celles de [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="ae97f-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="ae97f-442">SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)</span><span class="sxs-lookup"><span data-stu-id="ae97f-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="ae97f-443">Comme avec les nuanceurs de pixels et vertex, [Direct2D](./direct2d-portal.md) appelle la méthode [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quand la transformation est ajoutée pour la première fois au graphique de transformation d’un effet.</span><span class="sxs-lookup"><span data-stu-id="ae97f-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="ae97f-444">Cette méthode fournit un paramètre [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) qui contrôle le mode de rendu de la transformation.</span><span class="sxs-lookup"><span data-stu-id="ae97f-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="ae97f-445">Cela comprend le choix du nuanceur de calcul à exécuter par le biais de la méthode [**ID2D1ComputeInfo :: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="ae97f-446">Si la transformation choisit de stocker ce paramètre en tant que variable de membre de classe, elle est accessible et peut être modifiée à partir d’une méthode de transformation ou d’effet, à l’exception des méthodes [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) et [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ae97f-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="ae97f-447">Consultez la rubrique **ID2D1ComputeInfo** pour connaître les autres méthodes disponibles ici.</span><span class="sxs-lookup"><span data-stu-id="ae97f-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="ae97f-448">CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)</span><span class="sxs-lookup"><span data-stu-id="ae97f-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="ae97f-449">Tandis que les nuanceurs de pixels sont exécutés sur une base par pixel et que les nuanceurs vertex sont exécutés sur une base par vertex, les nuanceurs de calcul sont exécutés sur une base par’threadgroup.</span><span class="sxs-lookup"><span data-stu-id="ae97f-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="ae97f-450">Un ThreadGroup représente un nombre de threads qui s’exécutent simultanément sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="ae97f-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="ae97f-451">Le code HLSL du nuanceur de calcul détermine le nombre de threads qui doivent être exécutés par ThreadGroup.</span><span class="sxs-lookup"><span data-stu-id="ae97f-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="ae97f-452">L’effet met à l’échelle le nombre d’threadgroups afin que le nuanceur exécute le nombre de fois souhaité, en fonction de la logique du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="ae97f-453">La méthode [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permet à la transformation d’indiquer à [Direct2D](./direct2d-portal.md) le nombre de groupes de threads requis, en fonction de la taille de l’image et de la connaissance propre à la transformation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="ae97f-454">Le nombre de fois où le nuanceur de calcul est exécuté est un produit du nombre de ThreadGroup spécifié ici et de l’annotation « numThreads » dans le nuanceur de calcul [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="ae97f-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="ae97f-455">Par exemple, si la transformation définit les dimensions ThreadGroup sur (2, 2, 1) le nuanceur spécifie (3, 3, 1) threads par ThreadGroup, 4 threadgroups seront exécutés, chacun avec 9 threads, pour un total de 36 instances de thread.</span><span class="sxs-lookup"><span data-stu-id="ae97f-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="ae97f-456">Un scénario courant consiste à traiter un pixel de sortie pour chaque instance du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ae97f-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="ae97f-457">Pour calculer le nombre de groupes de threads pour ce scénario, la transformation divise la largeur et la hauteur de l’image par les dimensions x et y respectives de l’annotation « numThreads » dans le [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="ae97f-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="ae97f-458">Important, si cette division est effectuée, le nombre de groupes de threads demandés doit toujours être arrondi à l’entier le plus proche. sinon, les pixels « restants » ne seront pas exécutés sur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="ae97f-459">Si un nuanceur (par exemple) calcule un pixel unique avec chaque thread, le code de la méthode apparaît comme suit.</span><span class="sxs-lookup"><span data-stu-id="ae97f-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



<span data-ttu-id="ae97f-460">Le [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) utilise le code suivant pour spécifier le nombre de threads dans chaque groupe de threads :</span><span class="sxs-lookup"><span data-stu-id="ae97f-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="ae97f-461">Pendant l’exécution, le ThreadGroup actuel et l’index actuel du thread sont passés comme paramètres à la méthode du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ae97f-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a><span data-ttu-id="ae97f-462">Lecture des données de l’image</span><span class="sxs-lookup"><span data-stu-id="ae97f-462">Reading image data</span></span>

<span data-ttu-id="ae97f-463">Les nuanceurs de calcul accèdent à l’image d’entrée de la transformation sous la forme d’une seule texture à deux dimensions :</span><span class="sxs-lookup"><span data-stu-id="ae97f-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="ae97f-464">Toutefois, comme les nuanceurs de pixels, il n’est pas garanti que les données de l’image commencent à (0,0) sur la texture.</span><span class="sxs-lookup"><span data-stu-id="ae97f-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="ae97f-465">Au lieu de cela, [Direct2D](./direct2d-portal.md) fournit des constantes système qui permettent aux nuanceurs de compenser tout décalage :</span><span class="sxs-lookup"><span data-stu-id="ae97f-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



<span data-ttu-id="ae97f-466">Une fois que la méthode de tampon et la méthode d’assistance constantes ci-dessus ont été définies, le nuanceur peut échantillonner des données d’image à l’aide des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ae97f-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a><span data-ttu-id="ae97f-467">Écriture de données d’image</span><span class="sxs-lookup"><span data-stu-id="ae97f-467">Writing image data</span></span>

<span data-ttu-id="ae97f-468">[Direct2D](./direct2d-portal.md) attend qu’un nuanceur définisse une mémoire tampon de sortie pour l’image résultante à placer.</span><span class="sxs-lookup"><span data-stu-id="ae97f-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="ae97f-469">Dans le nuanceur modèle 4 (DirectX 10), il doit s’agir d’une mémoire tampon unidimensionnelle en raison de contraintes de fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="ae97f-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="ae97f-470">La texture de sortie est indexée ligne par ligne pour permettre le stockage de l’image entière.</span><span class="sxs-lookup"><span data-stu-id="ae97f-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="ae97f-471">En revanche, les nuanceurs Shader Model 5 (DirectX 11) peuvent utiliser des textures de sortie à deux dimensions :</span><span class="sxs-lookup"><span data-stu-id="ae97f-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="ae97f-472">Avec les nuanceurs du modèle de nuanceur 5, [Direct2D](./direct2d-portal.md) fournit un paramètre « outputOffset » supplémentaire dans la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="ae97f-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="ae97f-473">La sortie du nuanceur doit être offsetted par cette valeur :</span><span class="sxs-lookup"><span data-stu-id="ae97f-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="ae97f-474">Un nuanceur de calcul de modèle 5 de nuanceur direct terminé est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ae97f-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="ae97f-475">Dans celui-ci, chacun des threads du nuanceur de calcul lit et écrit un seul pixel de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ae97f-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="ae97f-476">Le code ci-dessous montre la version équivalente du nuanceur de nuanceur 4 du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ae97f-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="ae97f-477">Notez que le nuanceur s’affiche désormais dans une mémoire tampon de sortie unidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="ae97f-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a><span data-ttu-id="ae97f-478">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae97f-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae97f-479">Exemple de kit SDK D2DCustomEffects</span><span class="sxs-lookup"><span data-stu-id="ae97f-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 