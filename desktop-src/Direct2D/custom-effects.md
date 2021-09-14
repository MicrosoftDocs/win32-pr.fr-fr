---
title: Effets personnalisés
description: Montre comment écrire vos propres effets personnalisés à l’aide du langage HLSL standard.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114114"
---
# <a name="custom-effects"></a>Effets personnalisés

[Direct2D](./direct2d-portal.md) est fourni avec une bibliothèque d’effets qui effectuent diverses opérations d’image courantes. Pour obtenir la liste complète des effets, consultez la rubrique [effets intégrés](built-in-effects.md) . Pour les fonctionnalités qui ne peuvent pas être obtenues avec les effets intégrés, Direct2D vous permet d’écrire vos propres effets personnalisés à l’aide du [langage HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)standard. Vous pouvez utiliser ces effets personnalisés avec les effets intégrés fournis avec Direct2D.

Pour obtenir des exemples d’un effet complet de nuanceur de pixels, de vertex et de calcul, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Dans cette rubrique, nous vous montrons les étapes et les concepts dont vous avez besoin pour concevoir et créer un effet personnalisé complet.

## <a name="introduction-what-is-inside-an-effect"></a>Présentation : qu’est-ce qui se trouve à l’intérieur d’un effet ?

![diagramme des effets d’ombre portée.](images/custom-effects1.png)

D’un côté, un effet [Direct2D](./direct2d-portal.md) effectue une tâche de création d’images, telle que la modification de la luminosité, la désaturation d’une image ou, comme illustré ci-dessus, la création d’une ombre portée. Pour l’application, elles sont simples. Ils peuvent accepter zéro ou plusieurs images d’entrée, exposer plusieurs propriétés qui contrôlent leur fonctionnement et générer une seule image de sortie.

Il existe quatre parties différentes d’un effet personnalisé qui est responsable de l’auteur d’un effet :

1.  Interface Effect : l’interface Effect définit de manière conceptuelle comment une application interagit avec un effet personnalisé (comme le nombre d’entrées acceptées par l’effet et les propriétés disponibles). L’interface Effect gère un graphique de transformation, qui contient les opérations de création d’images réelles.
2.  Graphique de transformation : chaque effet crée un graphique de transformation interne constitué de transformations individuelles. Chaque transformation représente une opération d’image unique. L’effet est responsable de la liaison de ces transformations dans un graphique pour effectuer l’effet de création d’images prévu. Un effet permet d’ajouter, de supprimer, de modifier et de réorganiser des transformations en réponse à des modifications apportées aux propriétés externes de l’effet.
3.  Transformation : une transformation représente une opération d’image unique. Son objectif principal est d’héberger les nuanceurs qui sont exécutés pour chaque pixel de sortie. À cette fin, il est responsable du calcul de la nouvelle taille de son image de sortie en fonction de la logique dans ses nuanceurs. Il doit également calculer la zone de son image d’entrée à partir de laquelle les nuanceurs doivent lire pour afficher la région de sortie demandée.
4.  Nuanceur : un nuanceur est exécuté sur l’entrée de la transformation sur le GPU (ou processeur si le rendu logiciel est spécifié lorsque l’application crée l’appareil Direct3D). Les nuanceurs d’effet sont écrits en langage[HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)(High Level Shading Language) et sont compilés en code d’octet pendant la compilation de l’effet, qui est ensuite chargé par l’effet au moment de l’exécution. Ce document de référence décrit comment écrire le langage HLSL conforme à [Direct2D](./direct2d-portal.md). La documentation Direct3D contient une vue d’ensemble du langage HLSL.

## <a name="creating-an-effect-interface"></a>Création d’une interface Effect

L’interface Effect définit la manière dont une application interagit avec l’effet personnalisé. Pour créer une interface Effect, une classe doit implémenter ID2D1EffectImpl, définir des métadonnées qui décrivent l’effet (par exemple son nom, son nombre d’entrées et ses propriétés) et créer des méthodes qui inscrivent l’effet personnalisé à utiliser avec [Direct2D](./direct2d-portal.md).

Une fois que tous les composants d’une interface Effect ont été implémentés, l’en-tête de la classe s’affiche comme suit :


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



### <a name="implement-id2d1effectimpl"></a>Implémenter ID2D1EffectImpl

L’interface [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contient trois méthodes que vous devez implémenter :

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) appelle la méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) après que la méthode [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) a été appelée par l’application. Vous pouvez utiliser cette méthode pour effectuer une initialisation interne ou toute autre opération nécessaire pour l’effet. En outre, vous pouvez l’utiliser pour créer le graphique de transformation initial de l’effet.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>SetGraph (ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) appelle la méthode [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) lorsque le nombre d’entrées à l’effet change. Alors que la plupart des effets ont un nombre constant d’entrées, d’autres comme l' [effet composite](composite.md) prennent en charge un nombre variable d’entrées. Cette méthode permet à ces effets de mettre à jour leur graphique de transformation en réponse à un nombre d’entrées variable. Si un effet ne prend pas en charge un nombre d’entrées de variables, cette méthode peut simplement retourner E \_ NOTIMPL.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>PrepareForRender (D2D1 \_ type de modification \_ ChangeType)

La méthode [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) offre la possibilité d’effectuer des opérations en réponse à des modifications externes. [Direct2D](./direct2d-portal.md) appelle cette méthode juste avant de restituer un effet si au moins l’une d’entre elles est vraie :

-   L’effet a été précédemment initialisé mais pas encore dessiné.
-   Une propriété Effect a changé depuis le dernier appel de dessin.
-   L’état du contexte [Direct2D](./direct2d-portal.md) appelant (comme PPP) a changé depuis le dernier appel de dessin.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Implémenter les méthodes d’inscription et de rappel des effets

Les applications doivent inscrire des effets avec [Direct2D](./direct2d-portal.md) avant de les instancier. Cette inscription est limitée à une instance d’une fabrique Direct2D et doit être répétée chaque fois que l’application est exécutée. Pour activer cette inscription, un effet personnalisé définit un GUID unique, une méthode publique qui enregistre l’effet et une méthode de rappel privée qui retourne une instance de l’effet.

### <a name="define-a-guid"></a>Définir un GUID

Vous devez définir un GUID qui identifie de façon unique l’effet de l’inscription avec [Direct2D](./direct2d-portal.md). L’application utilise le même pour identifier l’effet quand elle appelle [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).

Ce code illustre la définition d’un GUID de ce type pour un effet. Vous devez créer son propre GUID unique à l’aide d’un outil de génération de GUID, tel que guidgen.exe.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Définir une méthode d’inscription publique

Ensuite, définissez une méthode publique pour que l’application appelle pour inscrire l’effet avec [Direct2D](./direct2d-portal.md). Étant donné que l’inscription de l’effet est spécifique à une instance d’une fabrique Direct2D, la méthode accepte une interface [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) comme paramètre. Pour inscrire l’effet, la méthode appelle ensuite l’API [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) sur le paramètre **ID2D1Factory1** .

Cette API accepte une chaîne XML décrivant les métadonnées, les entrées et les propriétés de l’effet. Les métadonnées d’un effet sont fournies à titre d’information uniquement et peuvent être interrogées par l’application par le biais de l’interface [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) . Les données d’entrée et de propriété, en revanche, sont utilisées par [Direct2D](./direct2d-portal.md) et représentent les fonctionnalités de l’effet.

Une chaîne XML pour un exemple d’effet minimal est présentée ici. L’ajout de propriétés personnalisées au XML est traité dans la section Ajout de propriétés personnalisées à un effet.


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



### <a name="define-an-effect-factory-callback-method"></a>Définir une méthode de rappel de la fabrique Effect

L’effet doit également fournir une méthode de rappel privée qui retourne une instance de l’effet via un seul \* \* paramètre IUnknown. Un pointeur vers cette méthode est fourni à [Direct2D](./direct2d-portal.md) lorsque l’effet est inscrit via l’API [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) via le paramètre de [**\_ \_ fabrique d’effets PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .


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



### <a name="implement-the-iunknown-interface"></a>Implémenter l’interface IUnknown

Enfin, l’effet doit implémenter l’interface IUnknown pour la compatibilité avec COM.

## <a name="creating-the-effects-transform-graph"></a>Création du graphique de transformation de l’effet

Un effet peut utiliser plusieurs transformations différentes (opérations d’images individuelles) pour créer l’effet d’image souhaité. Pour contrôler l’ordre dans lequel ces transformations sont appliquées à l’image d’entrée, l’effet les réorganise dans un graphique de transformation. Un graphique de transformation peut utiliser les effets et les transformations inclus dans [Direct2D](./direct2d-portal.md) , ainsi que les transformations personnalisées créées par l’auteur de l’effet.

### <a name="using-transforms-included-with-direct2d"></a>Utilisation des transformations incluses avec Direct2D

Il s’agit des transformations les plus couramment utilisées avec [Direct2D](./direct2d-portal.md).

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): cette transformation fusionne un nombre arbitraire d’entrées en fonction d’une description de Blend, reportez-vous à la rubrique [**d2d1 \_ Blend \_ Description**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) et à l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) pour les exemples de fusion. Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): cette transformation développe la taille de sortie d’une image en fonction [**du \_ \_ mode d’extension d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) spécifié. Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): cette transformation décale (traduit) son entrée par un nombre entier de pixels. Cette transformation est retournée par la méthode [**ID2D1EffectContext :: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .
-   Tout effet existant peut être traité comme une transformation dans le cadre de la création de graphiques de transformation à l’aide de la méthode [**ID2D1EffectContext :: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .

### <a name="creating-a-single-node-transform-graph"></a>Création d’un graphique de transformation à nœud unique

Une fois que vous avez créé une transformation, l’entrée de l’effet doit être connectée à l’entrée de la transformation, et la sortie de la transformation doit être connectée à la sortie de l’effet. Quand un effet ne contient qu’une seule transformation, vous pouvez utiliser la méthode [**ID2D1TransformGraph :: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) pour y parvenir facilement.

Vous pouvez créer ou modifier une transformation dans les méthodes [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) ou [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) de l’effet à l’aide du paramètre ID2D1TransformGraph fourni. Si un effet doit apporter des modifications au graphique de transformation dans une autre méthode où ce paramètre n’est pas disponible, l’effet peut enregistrer le paramètre [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) en tant que variable membre de la classe et y accéder ailleurs, par exemple [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) ou une méthode de rappel de propriété personnalisée.

Un exemple de méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) est illustré ici. Cette méthode crée un graphique de transformation à nœud unique qui décale l’image de 100 pixels sur chaque axe.


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



### <a name="creating-a-multi-node-transform-graph"></a>Création d’un graphique de transformation à plusieurs nœuds

L’ajout de plusieurs transformations au graphique de transformation d’un effet permet aux effets d’effectuer en interne plusieurs opérations d’image présentées à une application sous la forme d’un effet unifié unique.

Comme indiqué ci-dessus, le graphique de transformation de l’effet peut être modifié dans toute méthode d’effet à l’aide du paramètre [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) reçu dans la méthode [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de l’effet. Les API suivantes de cette interface peuvent être utilisées pour créer ou modifier le graphique de transformation d’un effet :

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode)

La méthode [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , en fait, enregistre la transformation avec l’effet et doit être appelée avant que la transformation puisse être utilisée avec l’une des autres méthodes de graphique de transformation.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UInt32 toNodeInputIndex)

La méthode [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) connecte l’entrée d’image de l’effet à l’entrée d’une transformation. La même entrée d’effet peut être connectée à plusieurs transformations.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UInt32 toNodeInputIndex)

La méthode [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) connecte la sortie d’une transformation à l’entrée d’une autre transformation. Une sortie de transformation peut être connectée à plusieurs transformations.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>SetOutputNode (ID2D1TransformNode \* pNode)

La méthode [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) connecte la sortie d’une transformation à la sortie de l’effet. Étant donné qu’un effet n’a qu’une seule sortie, une seule transformation peut être désignée comme « nœud de sortie ».

Ce code utilise deux transformations distinctes pour créer un effet unifié. Dans ce cas, l’effet est une ombre portée convertie.


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



## <a name="adding-custom-properties-to-an-effect"></a>Ajout de propriétés personnalisées à un effet

Les effets peuvent définir des propriétés personnalisées qui permettent à une application de modifier le comportement de l’effet lors de l’exécution. Il existe trois étapes pour définir une propriété pour un effet personnalisé :

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Ajouter les métadonnées de la propriété aux données d’inscription de l’effet

### <a name="add-property-to-registration-xml"></a>Ajouter une propriété au fichier XML d’inscription

Vous devez définir les propriétés d’un effet personnalisé lors de l’inscription initiale de l’effet avec [Direct2D](./direct2d-portal.md). Tout d’abord, vous devez mettre à jour le XML d’inscription de l’effet dans sa méthode d’inscription publique avec la nouvelle propriété :


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



Quand vous définissez une propriété Effect dans XML, elle a besoin d’un nom, d’un type et d’un nom d’affichage. Le nom d’affichage d’une propriété, ainsi que les valeurs de catégorie, d’auteur et de description de l’effet global peuvent et doivent être localisés.

Pour chaque propriété, un effet peut éventuellement spécifier les valeurs par défaut, minimale et maximale. Ces valeurs sont fournies à titre d’information uniquement. Ils ne sont pas appliqués par [Direct2D](./direct2d-portal.md). C’est à vous de mettre en œuvre la logique par défaut/min/max spécifiée dans la classe Effect.

La valeur de type figurant dans le XML pour la propriété doit correspondre au type de données correspondant utilisé par les méthodes getter et setter de la propriété. Les valeurs XML correspondantes pour chaque type de données sont indiquées dans le tableau suivant :



| Type de données                                                                                                                              | Valeur XML correspondante |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| PWSTR                                                                                                                                  | string                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | float                   |
| [**\_Vecteur D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | Vector2                 |
| [**Le \_ vecteur D2D \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**Le \_ vecteur D2D \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**\_Matrice matrice \_ D2D \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**\_4X3 matrice \_ D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**\_Matrice D2D \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**\_5x4 matrice \_ D2D \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| POIDS\[\]                                                                                                                               | objet BLOB                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | colorcontext            |
| CLSID                                                                                                                                  | clsid                   |
| Énumération [**( \_ \_ mode d’interpolation d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Mapper la nouvelle propriété à des méthodes getter et setter

Ensuite, l’effet doit mapper cette nouvelle propriété à des méthodes getter et Setter. Cette opération s’effectue par le biais du tableau de [**\_ \_ liaison de propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) passé dans la méthode [**ID2D1Factory1 :: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .

Le tableau de [**\_ \_ liaison de la propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) se présente comme suit :


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



Une fois que vous avez créé le tableau de liaisons et XML, transmettez-les à la méthode [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



La \_ macro de liaison de type valeur d2d1 \_ \_ requiert que la classe Effect hérite de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) avant toute autre interface.

Les propriétés personnalisées d’un effet sont indexées dans l’ordre dans lequel elles sont déclarées dans le code XML, et une fois créées est accessible par l’application à l’aide des méthodes [**ID2D1Properties :: SetValue**](id2d1properties-setvalue-overload.md) et [**ID2D1Properties :: GetValue**](id2d1properties-getvalue-overload.md) . Pour plus de commodité, vous pouvez créer une énumération publique qui répertorie chaque propriété dans le fichier d’en-tête de l’effet :


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Créer les méthodes getter et setter pour la propriété

L’étape suivante consiste à créer les méthodes getter et setter pour la nouvelle propriété. Les noms des méthodes doivent correspondre à ceux spécifiés dans le tableau de [**\_ \_ liaison de propriété d2d1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) . En outre, le type de propriété spécifié dans le XML de l’effet doit correspondre au type du paramètre de la méthode setter et à la valeur de retour de la méthode d’accesseur Get.


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



### <a name="update-effects-transforms-in-response-to-property-change"></a>Mettre à jour les transformations de l’effet en réponse à une modification de propriété

Pour mettre à jour la sortie d’image d’un effet en réponse à une modification de propriété, l’effet doit modifier ses transformations sous-jacentes. Cette opération s’effectue généralement dans la méthode [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) de l’effet que [Direct2D](./direct2d-portal.md) appelle automatiquement quand l’une des propriétés d’un effet a été modifiée. Toutefois, les transformations peuvent être mises à jour dans n’importe laquelle des méthodes de l’effet : par exemple, Initialize ou les méthodes setter de propriété de l’effet.

Par exemple, si un effet contenait un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) et souhaite modifier sa valeur de décalage en réponse à la propriété offset de l’effet en cours de modification, il ajouterait le code suivant dans [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):


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



## <a name="creating-a-custom-transform"></a>Création d’une transformation personnalisée

Pour implémenter des opérations d’image au-delà de ce qui est fourni dans [Direct2D](./direct2d-portal.md), vous devez implémenter des transformations personnalisées. Les transformations personnalisées peuvent modifier arbitrairement une image d’entrée à l’aide d’un nuanceur HLSL personnalisé.

Les transformations implémentent l’une des deux interfaces différentes selon les types de nuanceurs qu’elles utilisent. Les transformations utilisant des nuanceurs de pixels et/ou vertex doivent implémenter [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), tandis que les transformations utilisant des nuanceurs de calcul doivent implémenter [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform). Ces interfaces héritent toutes deux de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). Cette section se concentre sur l’implémentation des fonctionnalités communes aux deux.

L’interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) a quatre méthodes à implémenter :

### <a name="getinputcount"></a>GetInputCount

Cette méthode retourne un entier représentant le nombre d’entrées pour la transformation.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>MapInputRectsToOutputRect

[Direct2D](./direct2d-portal.md) appelle la méthode [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) chaque fois que la transformation est rendue. Direct2D passe un rectangle représentant les limites de chacune des entrées à la transformation. La transformation est ensuite chargée de calculer les limites de l’image de sortie. La taille des rectangles pour toutes les méthodes sur cette interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) est définie en pixels, et non en DIP.

Cette méthode est également chargée de calculer la région de la sortie opaque en fonction de la logique de son nuanceur et des zones opaques de chaque entrée. Une région opaque d’une image est définie comme étant celle où le canal alpha est « 1 » pour l’intégralité du rectangle. S’il est impossible de savoir si la sortie d’une transformation est opaque, le rectangle opaque de sortie doit être défini sur (0, 0, 0, 0) comme valeur sûre. [Direct2D](./direct2d-portal.md) utilise ces informations pour effectuer des optimisations de rendu avec un contenu « opaque » garanti. Si cette valeur est incorrecte, elle peut entraîner un rendu incorrect.

Vous pouvez modifier le comportement de rendu de la transformation (comme défini dans les sections 6 à 8) au cours de cette méthode. Toutefois, vous ne pouvez pas modifier d’autres transformations dans le graphique de transformation ou la disposition du graphique elle-même ici.


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



Pour obtenir un exemple plus complexe, réfléchissez à la façon dont une opération de flou simple serait représentée :

Si une opération de flou utilise un rayon de 5 pixels, la taille du rectangle de sortie doit être développée de 5 pixels, comme indiqué ci-dessous. Lors de la modification des coordonnées d’un rectangle, une transformation doit garantir que sa logique ne provoque pas de dépassement de capacité ou de dépassement de capacité dans les coordonnées du rectangle.


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



Étant donné que l’image est floue, une zone de l’image opaque peut désormais être partiellement transparente. Cela est dû au fait que la zone en dehors de l’image est définie par défaut sur le noir transparent et que cette transparence est fusionnée dans l’image autour des bords. La transformation doit refléter cela dans ses calculs de rectangle opaque de sortie :


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Ces calculs sont visualisés ici :

![illustration du calcul du rectangle.](images/custom-effects2.png)

Pour plus d’informations sur cette méthode, consultez la page de référence [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>MapOutputRectToInputRects

[Direct2D](./direct2d-portal.md) appelle la méthode [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) après [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). La transformation doit calculer la partie de l’image à partir de laquelle elle doit lire afin de restituer correctement la région de sortie demandée.

Comme précédemment, si un effet mappe strictement les pixels 1-1, il peut passer le rectangle de sortie au rectangle d’entrée :


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



De même, si une transformation réduit ou développe une image (comme l’exemple de flou ici), les pixels utilisent souvent des pixels environnants pour calculer leur valeur. Avec un flou, la moyenne d’un pixel est calculée avec ses pixels environnants, même s’ils sont en dehors des limites de l’image d’entrée. Ce comportement est reflété dans le calcul. Comme précédemment, la transformation recherche les dépassements de capacité lors du développement des coordonnées d’un rectangle.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



Ce schéma visualise le calcul. [Direct2D](./direct2d-portal.md) échantillonne automatiquement les pixels noirs transparents lorsque l’image d’entrée n’existe pas, ce qui permet une fusion progressive du flou avec le contenu existant à l’écran.

![illustration d’un effet d’échantillonnage de pixels noirs transparents en dehors d’un rectangle.](images/custom-effects3.png)

Si le mappage n’est pas trivial, cette méthode doit définir le rectangle d’entrée sur la zone maximale pour garantir des résultats corrects. Pour ce faire, définissez les bords gauche et supérieur sur INT \_ min, et les bords droits et inférieurs sur int \_ Max.

Pour plus d’informations sur cette méthode, consultez la rubrique [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>MapInvalidRect

[Direct2D](./direct2d-portal.md) appelle également la méthode [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Toutefois, contrairement aux méthodes [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) et [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) , Direct2D n’est pas garanti de l’appeler à un moment donné. Cette méthode détermine de manière conceptuelle la partie de la sortie d’une transformation qui doit être restituée de nouveau en réponse à une partie ou à la totalité de son entrée en cours de modification. Il existe trois scénarios différents pour lesquels calculer un Rect non valide dans une transformation.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Transformations avec mappage de pixels un-à-un

Pour les transformations qui mappent les pixels 1-1, transmettez simplement le rectangle d’entrée non valide à dans le rectangle de sortie non valide :


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



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Transformations avec mappage de pixels plusieurs-à-plusieurs

Lorsque les pixels de sortie d’une transformation dépendent de leur zone environnante, le rectangle d’entrée non valide doit être développé en conséquence. Cela permet de tenir compte du fait que les pixels entourant le rectangle d’entrée non valide seront également affectés et deviendront non valides. Par exemple, un flou de cinq pixels utilise le calcul suivant :


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Transformations avec mappage de pixels complexe

Pour les transformations où les pixels d’entrée et de sortie n’ont pas de mappage simple, la totalité de la sortie peut être marquée comme étant non valide. Par exemple, si une transformation renvoie simplement la couleur moyenne de l’entrée, la totalité de la sortie de la transformation change si même une petite partie de l’entrée est modifiée. Dans ce cas, le rectangle de sortie non valide doit être défini sur un rectangle infini logiquement (indiqué ci-dessous). [Direct2D](./direct2d-portal.md) fixe automatiquement ce à la limite de la sortie.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Pour plus d’informations sur cette méthode, consultez la rubrique [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

Une fois que ces méthodes ont été implémentées, l’en-tête de votre transformation contient ce qui suit :


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



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Ajout d’un nuanceur de pixels à une transformation personnalisée

Une fois qu’une transformation a été créée, elle doit fournir un nuanceur qui va manipuler les pixels de l’image. Cette section décrit les étapes d’utilisation d’un nuanceur de pixels avec une transformation personnalisée.

### <a name="implementing-id2d1drawtransform"></a>Implémentation de ID2D1DrawTransform

Pour utiliser un nuanceur de pixels, la transformation doit implémenter l’interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , qui hérite de l’interface [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) décrite dans la section 5. Cette interface contient une nouvelle méthode à implémenter :

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)

[Direct2D](./direct2d-portal.md) appelle la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) quand la transformation est ajoutée pour la première fois au graphique de transformation d’un effet. Cette méthode fournit un paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) qui contrôle le mode de rendu de la transformation. Consultez la rubrique **ID2D1DrawInfo** pour connaître les méthodes disponibles ici.

Si la transformation choisit de stocker ce paramètre en tant que variable de membre de classe, l’objet *drawInfo* est accessible et modifié à partir d’autres méthodes telles que les accesseurs set de propriété ou [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). En particulier, il ne peut pas être appelé à partir des méthodes [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) ou [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) sur [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).

### <a name="creating-a-guid-for-the-pixel-shader"></a>Création d’un GUID pour le nuanceur de pixels

Ensuite, la transformation doit définir un GUID unique pour le nuanceur de pixels lui-même. Cette valeur est utilisée lorsque [Direct2D](./direct2d-portal.md) charge le nuanceur en mémoire, ainsi que lorsque la transformation choisit le nuanceur de pixels à utiliser pour l’exécution. des outils tels que guidgen.exe, inclus avec Visual Studio, peuvent être utilisés pour générer un GUID aléatoire.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Chargement du nuanceur de pixels avec Direct2D

Un nuanceur de pixels doit être chargé en mémoire avant de pouvoir être utilisé par la transformation.

Pour charger le nuanceur de pixels en mémoire, la transformation doit lire le code d’octet du nuanceur compilé à partir du. fichier CSO généré par Visual Studio (consultez la documentation [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pour plus d’informations) dans un tableau d’octets. Cette technique est illustrée en détail dans l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Une fois que les données du nuanceur ont été chargées dans un tableau d’octets, appelez la méthode [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) sur l’objet [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) de l’effet. [Direct2D](./direct2d-portal.md) ignore les appels à **LoadPixelShader** lorsqu’un shader avec le même GUID a déjà été chargé.

Une fois qu’un nuanceur de pixels a été chargé en mémoire, la transformation doit la sélectionner pour l’exécution en passant son GUID à la méthode [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fourni pendant la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) . Le nuanceur de pixels doit être déjà chargé en mémoire avant d’être sélectionné pour l’exécution.

### <a name="changing-shader-operation-with-constant-buffers"></a>Modification de l’opération de nuanceur avec des mémoires tampons constantes

Pour modifier le mode d’exécution d’un nuanceur, une transformation peut passer une mémoire tampon constante au nuanceur de pixels. Pour ce faire, une transformation définit un struct qui contient les variables souhaitées dans l’en-tête de classe :


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



La transformation appelle ensuite la méthode [**ID2D1DrawInfo :: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) fourni dans la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) pour passer cette mémoire tampon au nuanceur.

Le [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) doit également définir une structure correspondante qui représente la mémoire tampon constante. Les variables contenues dans le struct du nuanceur doivent correspondre à celles de la structure de la transformation.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



Une fois la mémoire tampon définie, les valeurs contenues dans peuvent être lues à partir de n’importe où dans le nuanceur de pixels.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Écriture d’un nuanceur de pixels pour Direct2D

Les transformations [Direct2D](./direct2d-portal.md) utilisent des nuanceurs créés à l’aide du [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)standard. Toutefois, il existe quelques concepts clés pour l’écriture d’un nuanceur de pixels qui s’exécute à partir du contexte d’une transformation. Pour obtenir un exemple complet d’un nuanceur de pixels entièrement fonctionnel, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

[Direct2D](./direct2d-portal.md) mappe automatiquement les entrées d’une transformation aux objets [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) dans le langage HLSL. Le premier **Texture2D** se trouve à l’emplacement de Registre T0 et le premier **SamplerState** se trouve dans le registre S0. Chaque entrée supplémentaire se trouve dans les registres correspondants suivants (T1 et S1, par exemple). Les données de pixels d’une entrée particulière peuvent être échantillonnées en appelant l’exemple sur l’objet **Texture2D** et en passant l’objet **SamplerState** correspondant et les coordonnées Texel.

Un nuanceur de pixels personnalisé est exécuté une fois pour chaque pixel rendu. Chaque fois que le nuanceur est exécuté, [Direct2D](./direct2d-portal.md) fournit automatiquement trois paramètres qui identifient sa position d’exécution actuelle :

-   Sortie de l’espace de scène : ce paramètre représente la position d’exécution actuelle en termes de la surface cible globale. Elle est définie en pixels et ses valeurs min/max correspondent aux limites du rectangle retourné par [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).
-   Sortie d’espace : ce paramètre est utilisé par Direct3D et ne doit pas être utilisé dans le nuanceur de pixels d’une transformation.
-   Texel-entrée d’espace : ce paramètre représente la position d’exécution actuelle dans une texture d’entrée particulière. Un nuanceur ne doit pas prendre de dépendances quant à la façon dont cette valeur est calculée. Elle ne doit l’utiliser que pour échantillonner l’entrée du nuanceur de pixels, comme illustré dans le code ci-dessous :


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



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Ajout d’un nuanceur de sommets à une transformation personnalisée

Vous pouvez utiliser des nuanceurs de vertex pour atteindre différents scénarios d’acquisition d’images que les nuanceurs de pixels. En particulier, les nuanceurs de vertex peuvent exécuter des effets d’images géométriques en transformant des vertex qui composent une image. Les nuanceurs vertex peuvent être utilisés indépendamment de ou conjointement aux nuanceurs de pixels spécifiés par la transformation. Si aucun nuanceur vertex n’est spécifié, [Direct2D](./direct2d-portal.md) remplace un nuanceur de sommets par défaut par le nuanceur de pixels personnalisé.

Le processus d’ajout d’un nuanceur de sommets à une transformation personnalisée est semblable à celui d’un nuanceur de pixels : la transformation implémente l’interface [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crée un GUID et (éventuellement) passe des mémoires tampons constantes au nuanceur. Toutefois, il existe quelques étapes supplémentaires clés propres aux nuanceurs de vertex :

### <a name="creating-a-vertex-buffer"></a>Création d’une mémoire tampon de vertex

Un nuanceur de sommets par définition s’exécute sur les vertex qui lui sont passés, et non sur des pixels individuels. Pour spécifier les vertex sur lesquels le nuanceur doit s’exécuter, une transformation crée une mémoire tampon de vertex à passer au nuanceur. La disposition des mémoires tampons de vertex n’est pas traitée dans ce document. Pour plus d’informations, consultez la [référence de Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou l’exemple de [Kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour un exemple d’implémentation.

Après avoir créé une mémoire tampon de vertex en mémoire, la transformation utilise la méthode [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) sur l’objet [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) de l’effet conteneur pour transmettre ces données au GPU. Là encore, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour obtenir un exemple d’implémentation.

Si aucune mémoire tampon de vertex n’est spécifiée par la transformation, [Direct2D](./direct2d-portal.md) passe une mémoire tampon de vertex par défaut représentant l’emplacement rectangulaire de l’image.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Modification de SetDrawInfo pour utiliser un nuanceur de sommets

Comme avec les nuanceurs de pixels, la transformation doit charger et sélectionner un nuanceur de sommets pour l’exécution. Pour charger le nuanceur de sommets, il appelle la méthode [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) sur la méthode [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) reçue dans la méthode Initialize de l’effet. Pour sélectionner le nuanceur de sommets pour l’exécution, il appelle [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) sur le paramètre [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) reçu dans la méthode [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) de la transformation. Cette méthode accepte un GUID pour un nuanceur de sommets chargé précédemment, ainsi qu’une mémoire tampon de vertex précédemment créée pour le nuanceur à exécuter.

### <a name="implementing-a-direct2d-vertex-shader"></a>Implémentation d’un nuanceur de sommets Direct2D

Une transformation de dessin peut contenir à la fois un nuanceur de pixels et un nuanceur de sommets. Si une transformation définit à la fois un nuanceur de pixels et un nuanceur de sommets, la sortie du nuanceur de sommets est directement donnée au nuanceur de pixels : l’application peut personnaliser la signature de retour du nuanceur de sommets/les paramètres du nuanceur de pixels tant qu’ils sont cohérents.

En revanche, si une transformation contient uniquement un nuanceur de sommets et s’appuie sur le nuanceur de pixels direct de [Direct2D](./direct2d-portal.md)par défaut, elle doit retourner la sortie par défaut suivante :


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Un nuanceur de sommets stocke le résultat de ses transformations de vertex dans la variable de sortie d’espace de scène du nuanceur. Pour calculer la sortie d’espace et les variables d’entrée d’espace de Texel, [Direct2D](./direct2d-portal.md) fournit automatiquement des matrices de conversion dans une mémoire tampon constante :


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



Vous trouverez ci-dessous un exemple de code de nuanceur de vertex qui utilise les matrices de conversion pour calculer le clip correct et les espaces texels attendus par [Direct2D](./direct2d-portal.md):


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



Le code ci-dessus peut être utilisé comme point de départ pour un nuanceur de sommets. Elle passe simplement par l’image d’entrée sans effectuer de transformations. Là encore, consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour une transformation entièrement implémentée basée sur un nuanceur de sommets.

Si aucune mémoire tampon de vertex n’est spécifiée par la transformation, [Direct2D](./direct2d-portal.md) remplace dans une mémoire tampon de vertex par défaut qui représente l’emplacement rectangulaire de l’image. Les paramètres du nuanceur de sommets sont remplacés par ceux de la sortie du nuanceur par défaut :


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Le nuanceur vertex ne peut pas modifier ses paramètres *sceneSpaceOutput* et *clipSpaceOutput* . Elle doit les retourner inchangées. Toutefois, il peut modifier le (s) paramètre (s) *texelSpaceInput* pour chaque image d’entrée. Si la transformation contient également un nuanceur de pixels personnalisé, le nuanceur de sommets peut toujours passer des paramètres personnalisés supplémentaires directement au nuanceur de pixels. En outre, la mémoire tampon personnalisée des matrices de conversion *sceneSpace* (B0) n’est plus fournie.

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Ajout d’un nuanceur de calcul à une transformation personnalisée

Enfin, les transformations personnalisées peuvent utiliser des nuanceurs de calcul pour certains scénarios ciblés. Les nuanceurs de calcul peuvent être utilisés pour implémenter des effets d’images complexes qui nécessitent un accès arbitraire aux mémoires tampons d’images d’entrée et de sortie. Par exemple, un algorithme d’histogramme de base ne peut pas être implémenté avec un nuanceur de pixels en raison des limitations de l’accès à la mémoire.

Étant donné que les nuanceurs de calcul présentent des exigences de niveau de matériel supérieures à celles des nuanceurs de pixels, les nuanceurs de pixels doivent être utilisés dans la mesure du possible pour implémenter un effet donné. Plus précisément, les nuanceurs de calcul s’exécutent uniquement sur la plupart des cartes de niveau DirectX 10 et versions ultérieures. Si une transformation choisit d’utiliser un nuanceur de calcul, il doit vérifier la prise en charge matérielle appropriée lors de l’instanciation en plus de l’implémentation de l’interface [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .

### <a name="checking-for-compute-shader-support"></a>Vérification de la prise en charge du nuanceur de calcul

Si un effet utilise un nuanceur de calcul, il doit vérifier la prise en charge du nuanceur de calcul lors de sa création à l’aide de la méthode [**ID2D1EffectContext :: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) . Si le GPU ne prend pas en charge les nuanceurs de calcul, l’effet doit retourner [**D2DERR \_ \_ \_ fonctionnalités d’appareil insuffisantes**](direct2d-error-codes.md).

Il existe deux types différents de nuanceurs de calcul qu’une transformation peut utiliser : Shader Model 4 (DirectX 10) et Shader Model 5 (DirectX 11). Il existe certaines limitations aux nuanceurs du modèle de nuanceur 4. Pour plus d’informations, consultez la documentation de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Les transformations peuvent contenir des types de nuanceurs et peuvent revenir au nuanceur modèle 4 quand cela est nécessaire : consultez l' [exemple du kit de développement logiciel (SDK) D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) pour une implémentation de ce.

### <a name="implement-id2d1computetransform"></a>Implémenter ID2D1ComputeTransform

Cette interface contient deux nouvelles méthodes à implémenter, en plus de celles de [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)

Comme avec les nuanceurs de pixels et vertex, [Direct2D](./direct2d-portal.md) appelle la méthode [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) quand la transformation est ajoutée pour la première fois au graphique de transformation d’un effet. Cette méthode fournit un paramètre [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) qui contrôle le mode de rendu de la transformation. Cela comprend le choix du nuanceur de calcul à exécuter par le biais de la méthode [**ID2D1ComputeInfo :: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) . Si la transformation choisit de stocker ce paramètre en tant que variable de membre de classe, elle est accessible et peut être modifiée à partir d’une méthode de transformation ou d’effet, à l’exception des méthodes [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) et [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Consultez la rubrique **ID2D1ComputeInfo** pour connaître les autres méthodes disponibles ici.

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)

Tandis que les nuanceurs de pixels sont exécutés sur une base par pixel et que les nuanceurs vertex sont exécutés sur une base par vertex, les nuanceurs de calcul sont exécutés sur une base par’threadgroup. Un ThreadGroup représente un nombre de threads qui s’exécutent simultanément sur le GPU. Le code HLSL du nuanceur de calcul détermine le nombre de threads qui doivent être exécutés par ThreadGroup. L’effet met à l’échelle le nombre d’threadgroups afin que le nuanceur exécute le nombre de fois souhaité, en fonction de la logique du nuanceur.

La méthode [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permet à la transformation d’indiquer à [Direct2D](./direct2d-portal.md) le nombre de groupes de threads requis, en fonction de la taille de l’image et de la connaissance propre à la transformation du nuanceur.

Le nombre de fois où le nuanceur de calcul est exécuté est un produit du nombre de ThreadGroup spécifié ici et de l’annotation « numThreads » dans le nuanceur de calcul [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl). Par exemple, si la transformation définit les dimensions ThreadGroup sur (2, 2, 1) le nuanceur spécifie (3, 3, 1) threads par ThreadGroup, 4 threadgroups seront exécutés, chacun avec 9 threads, pour un total de 36 instances de thread.

Un scénario courant consiste à traiter un pixel de sortie pour chaque instance du nuanceur de calcul. Pour calculer le nombre de groupes de threads pour ce scénario, la transformation divise la largeur et la hauteur de l’image par les dimensions x et y respectives de l’annotation « numThreads » dans le [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)du nuanceur de calcul.

Important, si cette division est effectuée, le nombre de groupes de threads demandés doit toujours être arrondi à l’entier le plus proche. sinon, les pixels « restants » ne seront pas exécutés sur. Si un nuanceur (par exemple) calcule un pixel unique avec chaque thread, le code de la méthode apparaît comme suit.


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



Le [langage HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) utilise le code suivant pour spécifier le nombre de threads dans chaque groupe de threads :


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Pendant l’exécution, le ThreadGroup actuel et l’index actuel du thread sont passés comme paramètres à la méthode du nuanceur :


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



### <a name="reading-image-data"></a>Lecture des données de l’image

Les nuanceurs de calcul accèdent à l’image d’entrée de la transformation sous la forme d’une seule texture à deux dimensions :


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



Toutefois, comme les nuanceurs de pixels, il n’est pas garanti que les données de l’image commencent à (0,0) sur la texture. Au lieu de cela, [Direct2D](./direct2d-portal.md) fournit des constantes système qui permettent aux nuanceurs de compenser tout décalage :


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



Une fois que la méthode de tampon et la méthode d’assistance constantes ci-dessus ont été définies, le nuanceur peut échantillonner des données d’image à l’aide des éléments suivants :


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



### <a name="writing-image-data"></a>Écriture de données d’image

[Direct2D](./direct2d-portal.md) attend qu’un nuanceur définisse une mémoire tampon de sortie pour l’image résultante à placer. Dans le nuanceur modèle 4 (DirectX 10), il doit s’agir d’une mémoire tampon unidimensionnelle en raison de contraintes de fonctionnalités :


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



La texture de sortie est indexée ligne par ligne pour permettre le stockage de l’image entière.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



En revanche, les nuanceurs Shader Model 5 (DirectX 11) peuvent utiliser des textures de sortie à deux dimensions :


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



Avec les nuanceurs du modèle de nuanceur 5, [Direct2D](./direct2d-portal.md) fournit un paramètre « outputOffset » supplémentaire dans la mémoire tampon constante. La sortie du nuanceur doit être offsetted par cette valeur :


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



Un nuanceur de calcul de modèle 5 de nuanceur direct terminé est illustré ci-dessous. Dans celui-ci, chacun des threads du nuanceur de calcul lit et écrit un seul pixel de l’image d’entrée.


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



Le code ci-dessous montre la version équivalente du nuanceur de nuanceur 4 du nuanceur. Notez que le nuanceur s’affiche désormais dans une mémoire tampon de sortie unidimensionnelle.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de kit SDK D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 