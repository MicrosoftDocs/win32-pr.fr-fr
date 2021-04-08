---
description: Programmation de DirectX avec COM.
title: Programmation de DirectX avec COM
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: f712e5fed19d6afe2762a77ffcdf8b5977f85901
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "103953285"
---
# <a name="programming-directx-with-com"></a>Programmation de DirectX avec COM

Le modèle COM (Component Object Model) Microsoft est un modèle de programmation orienté objet utilisé par plusieurs technologies, y compris l’essentiel de la surface de l’API DirectX. C’est pourquoi, en tant que développeur DirectX, vous utilisez inévitablement COM lorsque vous programmez DirectX.

> [!NOTE]
> La rubrique [consommer des composants COM avec c++/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) montre comment utiliser des API DirectX (et toute API com, pour cette question) à l’aide de [c++/WinRT](/windows/uwp/cpp-and-winrt-apis/). C’est de loin la technologie la plus pratique et recommandée à utiliser.

Vous pouvez également utiliser le modèle COM brut et c’est ce que cette rubrique concerne. Vous aurez besoin d’une compréhension de base des principes et des techniques de programmation impliqués dans l’utilisation des API COM. Bien que COM offre une réputation difficile et complexe, la programmation COM requise par la plupart des applications DirectX est simple. En partie, cela est dû au fait que vous allez consommer les objets COM fournis par DirectX. Vous n’avez pas besoin de créer vos propres objets COM, ce qui est généralement là où la complexité se produit.

## <a name="com-component-overview"></a>Vue d’ensemble du composant COM

Un objet COM est essentiellement un composant encapsulé de fonctionnalités qui peuvent être utilisées par les applications pour effectuer une ou plusieurs tâches. Pour le déploiement, un ou plusieurs composants COM sont empaquetés dans un fichier binaire appelé serveur COM. plus souvent qu’une DLL.

Une DLL traditionnelle exporte des fonctions gratuites. Un serveur COM peut faire de même. Toutefois, les composants COM au sein du serveur COM exposent des interfaces COM et des méthodes membres appartenant à ces interfaces. Votre application crée des instances de composants COM, récupère des interfaces à partir de celles-ci et appelle des méthodes sur ces interfaces afin de tirer parti des fonctionnalités implémentées dans les composants COM.

Dans la pratique, cela ressemble à l’appel de méthodes sur un objet C++ normal. Toutefois, il existe quelques différences.

- Un objet COM applique l’encapsulation plus stricte qu’un objet C++. Vous ne pouvez pas simplement créer l’objet, puis appeler une méthode publique. Au lieu de cela, les méthodes publiques d’un composant COM sont regroupées dans une ou plusieurs interfaces COM. Pour appeler une méthode, vous devez créer l’objet et récupérer à partir de l’objet l’interface qui implémente la méthode. Une interface implémente généralement un ensemble de méthodes associées qui fournissent l’accès à une fonctionnalité particulière de l’objet. Par exemple, l’interface [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) représente une carte graphique virtuelle et contient des méthodes qui vous permettent de créer des ressources, par exemple, et de nombreuses autres tâches liées à l’adaptateur.
- Un objet COM n’est pas créé de la même façon qu’un objet C++. Il existe plusieurs façons de créer un objet COM, mais elles impliquent toutes des techniques spécifiques à COM. L’API DirectX comprend une variété de fonctions et de méthodes d’assistance qui simplifient la création de la plupart des objets COM DirectX.
- Vous devez utiliser des techniques spécifiques à COM pour contrôler la durée de vie d’un objet COM.
- Le serveur COM (généralement une DLL) n’a pas besoin d’être chargé explicitement. Vous n’êtes pas non plus lié à une bibliothèque statique pour pouvoir utiliser un composant COM. Chaque composant COM possède un identificateur unique inscrit (identificateur global unique, ou GUID), que votre application utilise pour identifier l’objet COM. Votre application identifie le composant, et le runtime COM charge automatiquement la DLL de serveur COM correcte.
- COM est une spécification binaire. Les objets COM peuvent être écrits et accessibles à partir d’un large éventail de langages. Vous n’avez rien à savoir sur le code source de l’objet. Par exemple, Visual Basic applications utilisent régulièrement des objets COM qui ont été écrits en C++.

## <a name="component-object-and-interface"></a>Composant, objet et interface

Il est important de comprendre la distinction entre les composants, les objets et les interfaces. En cas d’utilisation occasionnelle, vous pouvez entendre un composant ou un objet référencé par le nom de son interface principale. Mais les termes ne sont pas interchangeables. Un composant peut implémenter n’importe quel nombre d’interfaces ; et un objet est une instance d’un composant. Par exemple, bien que tous les composants doivent implémenter l' [**interface IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), ils implémentent généralement au moins une interface supplémentaire, et ils peuvent implémenter beaucoup.

Pour utiliser une méthode d’interface particulière, vous ne devez pas instancier un objet, vous devez également obtenir l’interface appropriée.

En outre, plusieurs composants peuvent implémenter la même interface. Une interface est un groupe de méthodes qui effectuent un ensemble d’opérations liées de manière logique. La définition d’interface spécifie uniquement la syntaxe des méthodes et leurs fonctionnalités générales. Tout composant COM qui doit prendre en charge un ensemble d’opérations particulier peut le faire en implémentant une interface appropriée. Certaines interfaces sont hautement spécialisées et sont implémentées uniquement par un seul composant ; d’autres sont utiles dans de nombreuses circonstances et sont implémentées par de nombreux composants.

Si un composant implémente une interface, il doit prendre en charge chaque méthode dans la définition de l’interface. En d’autres termes, vous devez être en mesure d’appeler n’importe quelle méthode et de vous assurer qu’elle existe. Toutefois, les détails de la façon dont une méthode particulière est implémentée peuvent varier d’un composant à un autre. Par exemple, différents composants peuvent utiliser des algorithmes différents pour arriver au résultat final. Il n’y a pas non plus de garantie qu’une méthode ne sera pas prise en charge d’une façon non évidente. Parfois, un composant implémente une interface couramment utilisée, mais il ne doit prendre en charge qu’un sous-ensemble des méthodes. Vous serez toujours en mesure d’appeler correctement les méthodes restantes, mais elles retournent un [**HRESULT**](#hresult-values) (qui est un type com standard représentant un code de résultat) contenant la valeur **E_NOTIMPL**. Vous devez faire référence à sa documentation pour voir comment une interface est implémentée par un composant particulier.

La norme COM exige qu’une définition d’interface ne soit pas modifiée une fois qu’elle a été publiée. L’auteur ne peut pas, par exemple, ajouter une nouvelle méthode à une interface existante. L’auteur doit à la place créer une nouvelle interface. Bien qu’il n’existe aucune restriction sur les méthodes qui doivent être dans cette interface, il est courant de faire en sorte que l’interface de nouvelle génération comprenne toutes les méthodes de l’ancienne interface, ainsi que toutes les nouvelles méthodes.

Il n’est pas rare qu’une interface ait plusieurs générations. En règle générale, toutes les générations effectuent essentiellement la même tâche globale, mais elles sont différentes dans les détails. Souvent, un composant COM implémente chaque génération actuelle et précédente du lignage d’une interface donnée. Cela permet aux anciennes applications de continuer à utiliser les interfaces plus anciennes de l’objet, tandis que les applications plus récentes peuvent tirer parti des fonctionnalités des interfaces les plus récentes. En règle générale, un groupe descendant d’interfaces ont le même nom, plus un entier qui indique la génération. Par exemple, si l’interface d’origine était nommée **IMyInterface** (impliquant la génération 1), les deux générations suivantes seraient appelées **IMyInterface2** et **IMyInterface3**. Dans le cas des interfaces DirectX, les générations successives sont généralement nommées pour le numéro de version de DirectX.

## <a name="guids"></a>GUID

Les GUID sont un élément clé du modèle de programmation COM. Au plus basique, un GUID est une structure 128 bits. Toutefois, les GUID sont créés de manière à garantir que deux GUID ne sont pas identiques. COM utilise largement des GUID pour deux raisons principales.

- Pour identifier de façon unique un composant COM particulier. Un GUID qui est assigné pour identifier un composant COM est appelé identificateur de classe (CLSID) et vous utilisez un CLSID lorsque vous souhaitez créer une instance du composant COM associé.
- Pour identifier de façon unique une interface COM particulière. Un GUID qui est assigné pour identifier une interface COM est appelé un identificateur d’interface (IID) et vous utilisez un IID quand vous demandez une interface particulière à partir d’une instance d’un composant (un objet). L’IID d’une interface sera le même, quel que soit le composant qui implémente l’interface.

Pour plus de commodité, la documentation DirectX fait normalement référence aux composants et aux interfaces par leurs noms descriptifs (par exemple, **ID3D12Device**) plutôt que par leurs GUID. Dans le contexte de la documentation DirectX, il n’y a aucune ambiguïté. Il est techniquement possible pour un tiers de créer une interface avec le nom descriptif **ID3D12Device** (il doit avoir un IID différent pour être valide). Dans un souci de clarté, toutefois, nous ne vous recommandons pas.

Ainsi, la seule manière non ambiguë de faire référence à un objet ou une interface particulier est par son GUID.

Bien qu’un GUID soit une structure, un GUID est souvent exprimé sous la forme d’une chaîne équivalente. Le format général de la forme de chaîne d’un GUID est 32 chiffres hexadécimaux, au format 8-4-4-4-12. Autrement dit, {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, où chaque x correspond à un chiffre hexadécimal. Par exemple, la chaîne de l’IID de l’interface **ID3D12Device** est {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Étant donné que le GUID réel est quelque peu encombrant et facile à utiliser, un nom équivalent est également fourni. Dans votre code, vous pouvez utiliser ce nom au lieu de la structure réelle quand vous appelez des fonctions, par exemple quand vous transmettez un argument pour le `riid` paramètre à [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice). La Convention d’affectation de noms personnalisée consiste à ajouter IID_ ou CLSID_ au nom descriptif de l’interface ou de l’objet, respectivement. Par exemple, le nom de l’IID de l’interface **ID3D12Device** est IID_ID3D12Device.

> [!NOTE]
> Les applications DirectX doivent établir une liaison avec ``dxguid.lib`` et ``uuid.lib`` pour fournir des définitions pour les différents GUID d’interface et de classe. Visual C++ et d’autres compilateurs prennent en charge l’extension de langage d’opérateur **__uuidof** , mais la liaison de style C explicite avec ces bibliothèques de liens est également prise en charge et entièrement portable.

## <a name="hresult-values"></a>Valeurs HRESULT

La plupart des méthodes COM retournent un entier 32 bits appelé **HRESULT**. Avec la plupart des méthodes, HRESULT est essentiellement une structure qui contient deux informations principales.
- Indique si la méthode a réussi ou échoué.
- Informations plus détaillées sur le résultat de l’opération effectuée par la méthode.

Certaines méthodes retournent une valeur **HRESULT** à partir de l’ensemble standard défini dans `Winerror.h` . Toutefois, une méthode est libre de retourner une valeur **HRESULT** personnalisée avec des informations plus spécialisées. Ces valeurs sont généralement documentées sur la page de référence de la méthode.

La liste des valeurs **HRESULT** que vous trouvez dans la page de référence d’une méthode est souvent uniquement un sous-ensemble des valeurs possibles qui peuvent être retournées. En général, la liste couvre uniquement les valeurs qui sont spécifiques à la méthode, ainsi que les valeurs standard qui ont une signification spécifique à la méthode. Vous devez supposer qu’une méthode peut retourner une variété de valeurs **HRESULT** standard, même si elles ne sont pas explicitement documentées.

Alors que les valeurs **HRESULT** sont souvent utilisées pour retourner les informations d’erreur, vous ne devez pas les considérer comme des codes d’erreur. Le fait que le bit qui indique la réussite ou l’échec est stocké séparément des bits qui contiennent les informations détaillées permet aux valeurs **HRESULT** d’avoir un nombre quelconque de codes de réussite et d’échec. Par Convention, les noms des codes de réussite sont préfixés par les codes d’S_ et d’échec en E_. Par exemple, les deux codes les plus couramment utilisés sont S_OK et E_FAIL, qui indiquent respectivement une réussite ou un échec simple.

Le fait que les méthodes COM puissent retourner une variété de codes de réussite ou d’échec signifie que vous devez faire attention à la façon dont vous testez la valeur **HRESULT** . Par exemple, considérez une méthode hypothétique avec des valeurs de retour documentées de S_OK en cas de réussite et E_FAIL dans le cas contraire. Toutefois, n’oubliez pas que la méthode peut également retourner d’autres codes d’échec ou de réussite. Le fragment de code suivant illustre le risque d’utiliser un test simple, où `hr` contient la valeur **HRESULT** retournée par la méthode.

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Tant que, en cas d’échec, cette méthode ne retourne jamais E_FAIL (et pas un autre code d’échec), alors ce test fonctionne. Toutefois, il est plus réaliste qu’une méthode donnée soit implémentée pour retourner un ensemble de codes d’erreur spécifiques, peut-être E_NOTIMPL ou E_INVALIDARG. Avec le code ci-dessus, ces valeurs ne sont pas interprétées correctement comme un succès.

Si vous avez besoin d’informations détaillées sur le résultat de l’appel de la méthode, vous devez tester chaque valeur **HRESULT** pertinente. Toutefois, vous pouvez être intéressé uniquement par le fait que la méthode a réussi ou échoué. Un moyen fiable de tester si une valeur **HRESULT** indique la réussite ou l’échec consiste à passer la valeur à l’une des macros suivantes, définie dans Winerror. h.

- La `SUCCEEDED` macro retourne la valeur true pour un code de réussite et la valeur false pour un code d’échec.
- La `FAILED` macro retourne la valeur true pour un code d’échec et la valeur false pour un code de réussite.

Par conséquent, vous pouvez corriger le fragment de code précédent à l’aide de la `FAILED` macro, comme indiqué dans le code suivant.

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Ce fragment de code corrigé traite correctement les E_NOTIMPL et les E_INVALIDARG comme des échecs.

Bien que la plupart des méthodes COM retournent des valeurs **HRESULT** structurées, un petit nombre utilise la valeur **HRESULT** pour retourner un entier simple. Implicitement, ces méthodes aboutissent toujours. Si vous transmettez un **HRESULT** de ce tri à la macro SUCCEEDED, la macro retourne toujours true. Un exemple de méthode communément appelée qui ne retourne pas de valeur **HRESULT** est la méthode **IUnknown :: Release** , qui retourne un ulong. Cette méthode décrémente le décompte de références d’un objet et retourne le décompte de références actuel. Consultez Gestion de la durée de vie d’un [objet com](#managing-a-com-objects-lifetime) pour une discussion sur le décompte de références.

## <a name="the-address-of-a-pointer"></a>Adresse d’un pointeur

Si vous affichez quelques pages de référence de méthode COM, vous risquez de rencontrer ce qui suit.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Bien qu’un pointeur normal soit tout à fait familier à un développeur C/C++, COM utilise souvent un niveau supplémentaire d’indirection. Ce deuxième niveau d’indirection est indiqué par deux astérisques, `**` , à la suite de la déclaration de type, et le nom de la variable a généralement un préfixe `pp` . Pour la fonction ci-dessus, le `ppDevice` paramètre est généralement désigné comme l’adresse d’un pointeur vers un void. Dans la pratique, dans cet exemple, `ppDevice` est l’adresse d’un pointeur vers une interface **ID3D12Device** .

Contrairement à un objet C++, vous n’accédez pas directement aux méthodes d’un objet COM. Au lieu de cela, vous devez obtenir un pointeur vers une interface qui expose la méthode. Pour appeler la méthode, vous utilisez essentiellement la même syntaxe que pour appeler un pointeur vers une méthode C++. Par exemple, pour appeler la méthode **IMyInterface ::D osomething** , vous devez utiliser la syntaxe suivante.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

Le besoin d’un deuxième niveau d’indirection provient du fait que vous ne créez pas directement de pointeurs d’interface. Vous devez appeler l’une des différentes méthodes, telles que la méthode **D3D12CreateDevice** indiquée ci-dessus. Pour utiliser une telle méthode pour obtenir un pointeur d’interface, vous déclarez une variable en tant que pointeur vers l’interface souhaitée, puis vous transmettez l’adresse de cette variable à la méthode. En d’autres termes, vous transmettez l’adresse d’un pointeur vers la méthode. Lorsque la méthode est retournée, la variable pointe vers l’interface demandée et vous pouvez utiliser ce pointeur pour appeler l’une des méthodes de l’interface.

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>Création d’un objet COM

Il existe plusieurs façons de créer un objet COM. Ce sont les deux les plus couramment utilisés dans la programmation DirectX.

- Indirectement, en appelant une méthode ou une fonction DirectX qui crée l’objet pour vous. La méthode crée l’objet et retourne une interface sur l’objet. Lorsque vous créez un objet de cette manière, vous pouvez parfois spécifier l’interface qui doit être retournée, d’autres fois que l’interface est impliquée. L’exemple de code ci-dessus montre comment créer indirectement un objet COM d’appareil Direct3D 12.
- Directement, en passant le CLSID de l’objet à la [**fonction CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). La fonction crée une instance de l’objet et retourne un pointeur vers une interface que vous spécifiez.

Une fois, avant de créer des objets COM, vous devez initialiser COM en appelant la [**fonction CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Si vous créez des objets indirectement, la méthode de création d’objet gère cette tâche. Toutefois, si vous devez créer un objet avec **CoCreateInstance**, vous devez appeler **CoInitializeEx** explicitement. Lorsque vous avez terminé, COM doit être non initialisé en appelant [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Si vous effectuez un appel à **CoInitializeEx** , vous devez le faire correspondre avec un appel à **CoUninitialize**. En règle générale, les applications qui doivent initialiser explicitement COM le font dans leur routine de démarrage, et elles n’initialisent pas COM dans leur routine de nettoyage.

Pour créer une nouvelle instance d’un objet COM avec **CoCreateInstance**, vous devez avoir le CLSID de l’objet. Si ce CLSID est disponible publiquement, vous le trouverez dans la documentation de référence ou dans le fichier d’en-tête approprié. Si le CLSID n’est pas disponible publiquement, vous ne pouvez pas créer l’objet directement.

La fonction **CoCreateInstance** a cinq paramètres. Pour les objets COM que vous allez utiliser avec DirectX, vous pouvez normalement définir les paramètres comme suit.

*rclsid* Définissez cette valeur sur le CLSID de l’objet que vous souhaitez créer.

*pUnkOuter* Affectez à la valeur `nullptr` . Ce paramètre est utilisé uniquement si vous regroupez des objets. La description de l’agrégation COM n’entre pas dans le cadre de cette rubrique.

*dwClsContext* Définissez sur CLSCTX_INPROC_SERVER. Ce paramètre indique que l’objet est implémenté en tant que DLL et s’exécute dans le cadre du processus de votre application.

*riid* Définissez sur l’IID de l’interface que vous souhaitez retourner. La fonction crée l’objet et retourne le pointeur d’interface demandé dans le paramètre PPV.

*PPV* Affectez-lui l’adresse d’un pointeur qui sera défini sur l’interface spécifiée par `riid` lorsque la fonction retourne. Cette variable doit être déclarée comme un pointeur vers l’interface demandée, et la référence au pointeur dans la liste de paramètres doit être castée en (LPVOID *).

La création d’un objet indirectement est généralement nettement plus simple, comme nous l’avons vu dans l’exemple de code ci-dessus. Vous transmettez à la méthode de création d’objet l’adresse d’un pointeur d’interface, et la méthode crée ensuite l’objet et retourne un pointeur d’interface. Lorsque vous créez un objet indirectement, même si vous ne pouvez pas choisir l’interface retournée par la méthode, vous pouvez souvent spécifier un certain nombre de choses sur la façon dont l’objet doit être créé.

Par exemple, vous pouvez passer à **D3D12CreateDevice** une valeur spécifiant le niveau de fonctionnalité D3D minimal que l’appareil retourné doit prendre en charge, comme indiqué dans l’exemple de code ci-dessus.

## <a name="using-com-interfaces"></a>Utilisation des interfaces COM

Lorsque vous créez un objet COM, la méthode de création retourne un pointeur d’interface. Vous pouvez ensuite utiliser ce pointeur pour accéder à n’importe quelle méthode de l’interface. La syntaxe est identique à celle utilisée avec un pointeur vers une méthode C++.

## <a name="requesting-additional-interfaces"></a>Demande d’interfaces supplémentaires

Dans de nombreux cas, le pointeur d’interface que vous recevez de la méthode de création peut être le seul dont vous avez besoin. En fait, il est relativement courant pour un objet d’exporter une seule interface autre que **IUnknown**. Toutefois, de nombreux objets exportent plusieurs interfaces et vous pouvez avoir besoin de pointeurs vers plusieurs d’entre eux. Si vous avez besoin de davantage d’interfaces que celles retournées par la méthode de création, il n’est pas nécessaire de créer un nouvel objet. Au lieu de cela, demandez un autre pointeur d’interface à l’aide de la [**méthode IUnknown :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))de l’objet.

Si vous créez votre objet avec **CoCreateInstance**, vous pouvez demander un pointeur d’interface **IUnknown** , puis appeler **IUnknown :: QueryInterface** pour demander chaque interface dont vous avez besoin. Toutefois, cette approche est peu commode si vous n’avez besoin que d’une seule interface et qu’elle ne fonctionne pas du tout si vous utilisez une méthode de création d’objet qui ne vous permet pas de spécifier le pointeur d’interface qui doit être retourné. Dans la pratique, vous n’avez généralement pas besoin d’obtenir un pointeur **IUnknown** explicite, car toutes les interfaces com étendent l’interface **IUnknown** .

L’extension d’une interface est conceptuellement similaire à l’héritage d’une classe C++. L’interface enfant expose toutes les méthodes de l’interface parent, ainsi qu’une ou plusieurs de ses propres méthodes. En fait, vous verrez souvent « Inherits from » utilisé à la place de « extends ». Vous devez vous souvenir que l’héritage est interne à l’objet. Votre application ne peut pas hériter de l’interface d’un objet ou l’étendre. Toutefois, vous pouvez utiliser l’interface enfant pour appeler l’une des méthodes de l’enfant ou du parent.

Étant donné que toutes les interfaces sont des enfants de **IUnknown**, vous pouvez appeler **QueryInterface** sur l’un des pointeurs d’interface que vous avez déjà pour l’objet. Dans ce cas, vous devez fournir l’IID de l’interface que vous demandez et l’adresse d’un pointeur qui contiendra le pointeur d’interface lorsque la méthode est retournée.

Par exemple, le fragment de code suivant appelle **IDXGIFactory2 :: CreateSwapChainForHwnd** pour créer un objet de chaîne de permutation principale. Cet objet expose plusieurs interfaces. La méthode **CreateSwapChainForHwnd** retourne une interface **IDXGISwapChain1** . Le code suivant utilise ensuite l’interface **IDXGISwapChain1** pour appeler **QueryInterface** afin de demander une interface **IDXGISwapChain3** .

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> En C++, vous pouvez utiliser la ``IID_PPV_ARGS`` macro plutôt que l’IID explicite et le pointeur Cast : ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Cela est souvent utilisé pour les méthodes de création, ainsi que pour **QueryInterface**. Pour plus d’informations, consultez [combaseapi. h](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args) .

## <a name="managing-a-com-objects-lifetime"></a>Gestion de la durée de vie d’un objet COM

Lorsqu’un objet est créé, le système alloue les ressources mémoire nécessaires. Lorsqu’un objet n’est plus nécessaire, il doit être détruit. Le système peut utiliser cette mémoire à d’autres fins. Avec les objets C++, vous pouvez contrôler la durée de vie de l’objet directement avec les `new` `delete` opérateurs et dans les cas où vous travaillez à ce niveau, ou simplement à l’aide de la pile et de la durée de vie de la portée. COM ne vous permet pas de créer ou de détruire directement des objets. La raison de cette conception est que le même objet peut être utilisé par plusieurs parties de votre application ou, dans certains cas, par plusieurs applications. Si l’une de ces références était de détruire l’objet, les autres références deviendront non valides. Au lieu de cela, COM utilise un système de décompte de références pour contrôler la durée de vie d’un objet.

Le nombre de références d’un objet est le nombre de fois que l’une de ses interfaces a été demandée. Chaque fois qu’une interface est demandée, le nombre de références est incrémenté. Une application libère une interface lorsque cette interface n’est plus nécessaire, ce qui décrémente le nombre de références. Tant que le nombre de références est supérieur à zéro, l’objet reste en mémoire. Lorsque le nombre de références atteint zéro, l’objet se détruit lui-même. Vous n’avez rien à savoir sur le décompte de références d’un objet. À condition que vous obteniez et libériez correctement les interfaces d’un objet, l’objet aura la durée de vie appropriée.

La gestion correcte du décompte de références est un élément essentiel de la programmation COM. Dans le cas contraire, vous risquez de créer facilement une fuite de mémoire ou un incident. L’une des erreurs les plus courantes effectuées par les programmeurs COM est l’échec de la libération d’une interface. Dans ce cas, le nombre de références n’atteint jamais la valeur zéro et l’objet reste en mémoire indéfiniment.

> [!NOTE]
> Direct3D 10 ou une version ultérieure a des règles de durée de vie légèrement modifiées pour les objets. En particulier, les objets dérivés de **ID3DxxDeviceChild** ne survivent jamais leur appareil parent (autrement dit, si le **ID3DxxDevice** propriétaire atteint un refcount 0, tous les objets enfants sont également immédiatement non valides). En outre, lorsque vous utilisez des méthodes **Set** pour lier des objets au pipeline de rendu, ces références n’augmentent pas le nombre de références (autrement dit, il s’agit de références faibles). Dans la pratique, cette méthode est mieux gérée en vous assurant que vous libérez entièrement tous les objets enfants de l’appareil avant de libérer l’appareil.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Incrémentation et décrémentation du décompte de références

Chaque fois que vous obtenez un nouveau pointeur d’interface, le décompte de références doit être incrémenté par un appel à [**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref). Toutefois, votre application n’a généralement pas besoin d’appeler cette méthode. Si vous obtenez un pointeur d’interface en appelant une méthode de création d’objet, ou en appelant **IUnknown :: QueryInterface**, l’objet incrémente automatiquement le nombre de références. Toutefois, si vous créez un pointeur d’interface d’une autre façon, telle que la copie d’un pointeur existant, vous devez appeler explicitement **IUnknown :: AddRef**. Dans le cas contraire, quand vous relâchez le pointeur d’interface d’origine, l’objet peut être détruit même si vous devez toujours utiliser la copie du pointeur.

Vous devez libérer tous les pointeurs d’interface, que vous ou l’objet incrémentiez ou non le nombre de références. Quand vous n’avez plus besoin d’un pointeur d’interface, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) pour décrémenter le décompte de références. Une pratique courante consiste à initialiser tous les pointeurs d’interface à `nullptr` , puis à les rétablir `nullptr` lorsqu’ils sont libérés. Cette Convention vous permet de tester tous les pointeurs d’interface dans votre code de nettoyage. Ceux qui ne sont pas `nullptr` toujours actifs et vous devez les libérer avant de mettre fin à l’application.

Le fragment de code suivant étend l’exemple indiqué plus haut pour illustrer comment gérer le décompte de références.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>Pointeurs intelligents COM

Le code jusqu’à présent a explicitement appelé ``Release`` et ``AddRef`` à conserver les décomptes de références à l’aide de méthodes **IUnknown** . Ce modèle nécessite que le programmeur soit à l’œuvre d’une mise à jour correcte pour gérer correctement le nombre dans tous les chemins possibles. Cela peut entraîner une gestion complexe des erreurs, et la gestion des exceptions C++ activée peut être particulièrement difficile à implémenter. Une meilleure solution avec C++ consiste à utiliser un [pointeur intelligent](/cpp/cpp/smart-pointers-modern-cpp).

* **WinRT :: com_ptr** est un pointeur intelligent fourni par les [projections de langage C++/WinRT](/uwp/cpp-ref-for-winrt/com-ptr). Il s’agit du pointeur intelligent COM recommandé à utiliser pour les applications UWP. Notez que C++/WinRT requiert C++ 17.

* **Microsoft :: WRL :: ComPtr** est un pointeur intelligent fourni par le [Windows Runtime C++ Template Library (WRL)](/cpp/cppcx/wrl/comptr-class). Cette bibliothèque est « pure » C++ et peut donc être utilisée pour les applications Windows Runtime (via C++/CX ou C++/WinRT), ainsi que pour les applications de bureau Win32 classiques. Ce pointeur intelligent fonctionne également sur les versions antérieures de Windows qui ne prennent pas en charge les API Windows Runtime. Pour les applications de bureau Win32, vous pouvez utiliser ``#include <wrl/client.h>`` pour inclure uniquement cette classe et éventuellement définir également le symbole de préprocesseur ``__WRL_CLASSIC_COM_STRICT__`` . Pour plus d’informations, consultez [pointeurs intelligents com revisités](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited).

* **CComPtr** est un pointeur intelligent fourni par le [Active Template Library (ATL)](/cpp/atl/reference/ccomptr-class). **Microsoft :: WRL :: ComPtr** est une version plus récente de cette implémentation qui résout plusieurs problèmes d’utilisation subtils. l’utilisation de ce pointeur intelligent n’est donc pas recommandée pour les nouveaux projets. Pour plus d’informations, consultez [How to Create and use CComPtr and CComQIPtr](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances).


## <a name="using-atl-with-directx-9"></a>Utilisation d’ATL avec DirectX 9

Pour utiliser la Active Template Library (ATL) avec DirectX 9, vous devez redéfinir les interfaces pour la compatibilité ATL. Cela vous permet d’utiliser correctement la classe **CComQIPtr** pour obtenir un pointeur vers une interface.

Vous saurez si vous ne redéfinissez pas les interfaces pour ATL, car le message d’erreur suivant s’affiche.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

L’exemple de code suivant montre comment définir l’interface IDirectXFileData.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Après avoir redéfini l’interface, vous devez utiliser la méthode **Attach** pour attacher l’interface au pointeur d’interface retourné par **::D irect3dcreate9**. Si ce n’est pas le cas, l’interface **IDirect3D9** ne sera pas correctement libérée par la classe de pointeur intelligent.

La classe **CComPtr** appelle en interne **IUnknown :: AddRef** sur le pointeur d’interface lorsque l’objet est créé et lorsqu’une interface est assignée à la classe **CComPtr** . Pour éviter la fuite du pointeur d’interface, n’appelez pas * * IUnknown :: AddRef sur l’interface retournée à partir de **::D irect3dcreate9**.

Le code suivant libère correctement l’interface sans appeler **IUnknown :: AddRef**.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Utilisez le code précédent. N’utilisez pas le code suivant, qui appelle **IUnknown :: AddRef** suivi de **IUnknown :: Release**, et qui ne libère pas la référence ajoutée par **::D irect3dcreate9**.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Notez qu’il s’agit du seul emplacement dans Direct3D 9 où vous devrez utiliser la méthode **Attach** de cette manière.

Pour plus d’informations sur les classes **CComPTR** et **CComQIPtr** , consultez leurs définitions dans le `Atlbase.h` fichier d’en-tête.
