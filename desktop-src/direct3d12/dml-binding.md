---
title: Liaison dans DirectML
description: Dans DirectML, la liaison fait référence à l’attachement des ressources au pipeline que le GPU doit utiliser pendant l’initialisation et l’exécution de vos opérateurs Machine Learning.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104548542"
---
# <a name="binding-in-directml"></a>Liaison dans DirectML

Dans DirectML, la *liaison* fait référence à l’attachement des ressources au pipeline que le GPU doit utiliser pendant l’initialisation et l’exécution de vos opérateurs machine learning. Ces ressources peuvent être des dizaines d’entrée et de sortie, par exemple, ainsi que toutes les ressources temporaires ou persistantes dont l’opérateur a besoin.

Cette rubrique traite des détails conceptuels et procédurals de la liaison. Nous vous recommandons également de lire entièrement la documentation des API que vous appelez, y compris les paramètres et les notes.

## <a name="important-ideas-in-binding"></a>Idées importantes en matière de liaison

La liste des étapes ci-dessous contient une description détaillée des tâches liées à la liaison. Vous devez suivre ces étapes chaque fois que vous exécutez un [répartiteur](/windows/desktop/api/directml/nn-directml-idmldispatchable) &mdash; un répartiteur est un initialiseur d’opérateur ou un opérateur compilé. Ces étapes présentent les idées, structures et méthodes importantes impliquées dans la liaison DirectML.

Les sections suivantes de cette rubrique décrivent plus en détail ces tâches de liaison, ainsi que des extraits de code supplémentaires tirés de l’exemple de code d' [application DirectML minimal](dml-min-app.md) .

- Appelez [**IDMLDispatchable :: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) sur le répartiteur pour déterminer le nombre de descripteurs dont il a besoin, ainsi que ses besoins en ressources temporaires/persistantes.
- Créez un tas de descripteur Direct3D 12 suffisamment grand pour les descripteurs et liez-le au pipeline.
- Appelez [**IDMLDevice :: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) pour créer une table de liaison DirectML afin de représenter les ressources liées au pipeline. Utilisez la structure [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) pour décrire votre table de liaison, y compris le sous-ensemble des descripteurs vers lequel elle pointe dans le tas du descripteur.
- Créez des ressources temporaires/persistantes en tant que ressources de tampon Direct3D 12, décrivez-les avec des structures [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) et [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) , puis ajoutez-les à la table de liaison.
- Si le répartiteur est un opérateur compilé, créez une mémoire tampon d’éléments tenseur en tant que ressource de mémoire tampon Direct3D 12. Remplissez/chargez-le, décrivez-le avec les structures **DML_BUFFER_BINDING** et **DML_BINDING_DESC** , puis ajoutez-le à la table de liaison.
- Transmettez votre table de liaison en tant que paramètre lorsque vous appelez [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>Récupérer les propriétés de liaison d’un répartiteur

La structure [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties) décrit les besoins de liaison d’un répartiteur (initialiseur d’opérateur ou opérateur compilé). Ces propriétés liées à la liaison incluent le nombre de descripteurs que vous devez lier au répartiteur, ainsi que la taille en octets des ressources temporaires et/ou persistantes dont il a besoin.

> [!NOTE]
> Même pour plusieurs opérateurs du même type, ne faites pas d’hypothèses à leur sujet avec les mêmes exigences de liaison. Interrogez les propriétés de liaison pour chaque initialiseur et opérateur que vous créez.

Appelez [**IDMLDispatchable :: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) pour récupérer un **DML_BINDING_PROPERTIES**.

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

La `descriptorCount` valeur que vous récupérez ici détermine la taille (minimale) du tas du descripteur et de la table de liaison que vous créez au cours des deux étapes suivantes.

**DML_BINDING_PROPERTIES** contient également un `TemporaryResourceSize` membre, qui est la taille minimale, en octets, de la ressource temporaire qui doit être liée à la table de liaison pour cet objet pouvant être distribué. La valeur zéro signifie qu’une ressource temporaire n’est pas requise.

Et un `PersistentResourceSize` membre, qui est la taille minimale, en octets, de la ressource persistante qui doit être liée à la table de liaison pour cet objet pouvant être distribué. La valeur zéro signifie qu’une ressource persistante n’est pas requise. Une ressource persistante, si nécessaire, doit être fournie pendant l’initialisation d’un opérateur compilé (où elle est liée en tant que sortie de l’initialiseur d’opérateur), ainsi que pendant l’exécution. Vous y découvrirez plus loin dans cette rubrique. Seuls les opérateurs compilés ont des ressources persistantes : les initialiseurs d’opérateur retournent toujours la valeur 0 pour ce membre.

Si vous appelez **IDMLDispatchable :: GetBindingProperties** sur un initialiseur d’opérateur à la fois avant et après un appel à [**IDMLOperatorInitializer :: Reset**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset), il n’est pas garanti que les deux ensembles de propriétés de liaison récupérés soient identiques.

## <a name="describe-create-and-bind-a-descriptor-heap"></a>Décrire, créer et lier un tas de descripteur

En termes de descripteurs, votre responsabilité commence et se termine par le tas du descripteur lui-même. DirectML prend en charge la création et la gestion des descripteurs à l’intérieur du tas que vous fournissez.

Par conséquent, utilisez une structure [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) pour décrire un tas suffisamment grand pour le nombre de descripteurs dont le répartiteur est nécessaire. Ensuite, créez-le avec [**ID3D12Device :: CreateDescriptorHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap). Enfin, appelez [**ID3D12GraphicsCommandList :: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) pour lier le tas du descripteur au pipeline.

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>Décrire et créer une table de liaison

Une table de liaison DirectML représente les ressources que vous liez au pipeline pour un répartiteur à utiliser. Ces ressources peuvent être des dizaines d’entrée et de sortie (ou d’autres paramètres) pour un opérateur, ou il peut s’agir de diverses ressources persistantes et temporaires avec lesquelles un répartiteur fonctionne.

Utilisez la structure [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) pour décrire votre table de liaison, y compris le répartiteur pour lequel la table de liaison représente les liaisons, et la plage de descripteurs (à partir du tas de descripteur que vous venez de créer) à laquelle vous souhaitez que la table de liaison fasse référence (et dans quels DirectML peuvent écrire des descripteurs). La `descriptorCount` valeur (l’une des propriétés de liaison que nous avons récupérées à la première étape) nous indique la taille minimale, en descripteurs, de la table de liaison requise pour l’objet pouvant être distribué. Ici, nous utilisons cette valeur pour indiquer le nombre maximal de descripteurs que DirectML est autorisé à écrire dans notre segment, à partir du début des handles de descripteur de processeur et GPU fournis.

Appelez ensuite [**IDMLDevice :: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) pour créer la table de liaison DirectML. Dans les étapes ultérieures, après avoir créé d’autres ressources pour le répartiteur, nous ajouterons ces ressources à la table de liaison.

Au lieu de passer un **DML_BINDING_TABLE_DESC** à cet appel, vous pouvez passer `nullptr` , indiquant une table de liaison vide.

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

L’ordre dans lequel DirectML écrit les descripteurs dans le tas n’est pas spécifié. votre application doit donc veiller à ne pas remplacer les descripteurs encapsulés par la table de liaison. Les handles de descripteur du processeur et du GPU fournis peuvent provenir de différents tas. Toutefois, il est de votre application de s’assurer que la plage de descripteurs entière référencée par le handle de descripteur de l’UC est copiée dans la plage référencée par le handle du descripteur GPU avant l’exécution à l’aide de cette table de liaison. Le tas de descripteur à partir duquel les handles sont fournis doit avoir un type **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV**. En outre, le tas référencé par `GPUDescriptorHandle` doit être un tas de descripteur visible par le nuanceur.

Vous pouvez réinitialiser une table de liaison pour supprimer toutes les ressources que vous y avez ajoutées, tout en modifiant la propriété que vous avez définie sur son **DML_BINDING_TABLE_DESC** initial (pour encapsuler une nouvelle plage de descripteurs ou pour la réutiliser pour un autre répartiteur). Apportez simplement les modifications à la structure de la description et appelez [**IDMLBindingTable :: Reset**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset).

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>Décrire et lier des ressources temporaires/persistantes

La structure **DML_BINDING_PROPERTIES** que nous avons renseignée lorsque nous avons [récupéré les propriétés de liaison](#retrieve-the-binding-properties-of-a-dispatchable) de notre répartiteur contient la taille en octets des ressources temporaires et/ou persistantes dont le répartiteur a besoin. Si l’une de ces tailles est différente de zéro, créez une ressource de mémoire tampon Direct3D 12 et ajoutez-la à la table de liaison.

Dans l’exemple de code ci-dessous, nous créons une ressource temporaire ( `temporaryResourceSize` octets en taille) pour le répartiteur. Nous décrivons la façon dont nous souhaitons lier la ressource, puis nous ajoutons cette liaison à la table de liaison.

Puisque nous créons une liaison avec une seule ressource de mémoire tampon, nous décrivons notre liaison avec une structure de [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) . Dans cette structure, nous spécifions la ressource de mémoire tampon Direct3D 12 (la ressource doit avoir une dimension [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)), ainsi qu’un décalage et une taille dans la mémoire tampon. Il est également possible de décrire une liaison pour un tableau de mémoires tampons (plutôt que pour une seule mémoire tampon), et la structure [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) existe à cet effet.

Pour soustraire la distinction entre une liaison de mémoire tampon et une liaison de tableau de mémoires tampons, nous utilisons la structure  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) . Vous pouvez définir le `Type` membre du **DML_BINDING_DESC** sur [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) ou **DML_BINDING_TYPE_BUFFER_ARRAY**. Vous pouvez ensuite définir le membre de façon à ce qu’il `Desc` pointe vers un **DML_BUFFER_BINDING** ou vers un **DML_BUFFER_ARRAY_BINDING**, en fonction de `Type` .

Nous nous contenterons de la ressource temporaire dans cet exemple, nous l’ajoutons donc à la table de liaison avec un appel à [**IDMLBindingTable :: BindTemporaryResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource).

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

Une ressource temporaire (si nécessaire) est une mémoire de travail qui est utilisée en interne lors de l’exécution de l’opérateur. vous n’avez donc pas à vous soucier de son contenu. Vous n’avez pas non plus besoin de le garder à l’issue de l’appel de [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) sur le GPU. Cela signifie que votre application peut libérer ou remplacer la ressource temporaire entre les distributions de l’opérateur compilé. Le décalage de début de la plage de mémoire tampon fournie pour la ressource temporaire doit être aligné sur [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). Le type du tas sous-jacent à la mémoire tampon doit être **D3D12_HEAP_TYPE_DEFAULT**.

Toutefois, si le répartiteur signale une taille différente de zéro pour sa ressource persistante à long terme, la procédure est légèrement différente. Vous devez créer une mémoire tampon et décrire une liaison à la suite du même modèle, comme indiqué ci-dessus. Toutefois, ajoutez-le à la table de liaison de l’initialiseur d’opérateur à l’aide d’un appel à [**IDMLBindingTable :: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs), car il s’agit du travail de l’initialiseur d’opérateur pour initialiser la ressource persistante. Ensuite, ajoutez-le à la table de liaison de votre opérateur compilé à l’aide d’un appel à [**IDMLBindingTable :: BindPersistentResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource). Consultez l’exemple de code d' [application DirectML minimal](dml-min-app.md) pour voir ce flux de travail en action. Le contenu et la durée de vie de la ressource persistante doivent persister tant que l’opérateur compilé en a la valeur. Autrement dit, si un opérateur requiert une ressource persistante, votre application doit le fournir au cours de l’initialisation et la fournir ensuite à toutes les exécutions ultérieures de l’opérateur sans modifier son contenu. La ressource persistante est généralement utilisée par DirectML pour stocker des tables de recherche ou d’autres données de longue durée qui sont calculées pendant l’initialisation d’un opérateur et réutilisées lors des exécutions ultérieures de cet opérateur. L’offset de début de la plage de mémoire tampon fournie à lier en tant que mémoire tampon persistante doit être aligné sur [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). Le type du tas sous-jacent à la mémoire tampon doit être **D3D12_HEAP_TYPE_DEFAULT**.

## <a name="describe-and-bind-any-tensors"></a>Décrire et lier des dizaines

Si vous travaillez avec un opérateur compilé (plutôt qu’avec un initialiseur d’opérateur), vous devez lier les ressources d’entrée et de sortie (pour les dizaines et les autres paramètres) à la table de liaison de l’opérateur. Le nombre de liaisons doit correspondre exactement au nombre d’entrées de l’opérateur, y compris les dizaines facultatifs. Les dizaines de temps d’entrée et de sortie et les autres paramètres qu’un opérateur prend sont documentés dans la rubrique de cet opérateur (par exemple, [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)).

Une ressource tenseur est une mémoire tampon qui contient les valeurs d’élément individuelles du tenseur. Vous téléchargez et lisez ce type de mémoire tampon vers/à partir du GPU à l’aide des techniques Direct3D 12 standard ([charger des ressources](/windows/desktop/direct3d12/uploading-resources) et [lire des données via une mémoire tampon](/windows/desktop/direct3d12/readback-data-using-heaps)). Consultez l’exemple de code d' [application DirectML minimal](dml-min-app.md) pour voir ces techniques en action.

Enfin, décrivez vos liaisons de ressource d’entrée et de sortie avec des structures **DML_BUFFER_BINDING** et **DML_BINDING_DESC** , puis ajoutez-les à la table de liaison de l’opérateur compilé avec des appels à [**IDMLBindingTable :: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) et [**IDMLBindingTable :: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs). Quand vous appelez une méthode **IDMLBindingTable :: \* Bind* _, DirectML écrit un ou plusieurs descripteurs dans la plage de descripteurs de l’UC.

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

L’une des étapes de la création d’un opérateur DirectML (consultez [_ *IDMLDevice :: CreateOperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) consiste à déclarer une ou plusieurs structures [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) pour décrire les mémoires tampons de données tenseur que l’opérateur prend et retourne. Ainsi que le type et la taille de la mémoire tampon tenseur, vous pouvez éventuellement spécifier l’indicateur [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) .

**DML_TENSOR_FLAG_OWNED_BY_DML** indique que les données tenseur doivent être détenues et gérées par DirectML. DirectML effectue une copie des données tenseur pendant l’initialisation de l’opérateur et les stocke dans la ressource persistante. Cela permet à DirectML d’effectuer un reformatage des données tenseur dans d’autres formes plus efficaces. La définition de cet indicateur peut améliorer les performances, mais elle est généralement utile uniquement pour les dizaines de dizaines dont les données ne changent pas pendant la durée de vie de l’opérateur (par exemple, des dizaines de poids). Et l’indicateur ne peut être utilisé que sur des dizaines d’entrées. Lorsque l’indicateur est défini sur une description de tenseur particulière, le tenseur correspondant doit être lié à la table de liaison pendant l’initialisation de l’opérateur, et non lors de l’exécution (ce qui génère une erreur). C’est l’inverse du comportement par défaut (comportement sans l’indicateur DML_TENSOR_FLAG_OWNED_BY_DML), où le tenseur est supposé être lié pendant l’exécution, et non pendant l’initialisation. Lorsque vous fournissez les données tenseur à un initialiseur d’opérateur, il est légal de lier un téléchargement plutôt qu’un segment de mémoire par défaut, car DirectML effectue une copie des données. Dans tous les autres cas, toutes les ressources liées à DirectML doivent être des ressources de tas par défaut.

Pour plus d’informations, consultez [**IDMLBindingTable :: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) et [**IDMLBindingTable :: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs).

## <a name="execute-the-dispatchable"></a>Exécuter le répartiteur

Transmettez votre table de liaison en tant que paramètre lorsque vous appelez [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

Lorsque vous utilisez la table de liaison pendant un appel à **IDMLCommandRecorder :: RecordDispatch**, DirectML lie les descripteurs GPU correspondants au pipeline. Les handles de descripteur du processeur et du GPU ne sont pas requis pour pointer vers les mêmes entrées dans un tas de descripteur. Toutefois, il est alors que votre application est chargée de s’assurer que l’intégralité de la plage de descripteur référencée par le handle de descripteur de processeur est copiée dans la plage référencée par le handle de descripteur

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

Enfin, fermez votre liste de commandes Direct3D 12, puis soumettez-la en vue de son exécution, comme vous le feriez pour toute autre liste de commandes.

Avant l’exécution de **RecordDispatch** sur le GPU, vous devez faire passer toutes les ressources liées à l’état **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** ou à un État pouvant être promu implicitement en **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, tel que **D3D12_RESOURCE_STATE_COMMON**. Une fois cet appel terminé, les ressources restent à l’état **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . La seule exception à cela concerne les tas de chargement liés lors de l’exécution d’un initialiseur d’opérateur et lorsqu’un ou plusieurs dizaines ont l’indicateur **DML_TENSOR_FLAG_OWNED_BY_DML** défini. Dans ce cas, tous les tas de chargement liés à l’entrée doivent être dans l’état **D3D12_RESOURCE_STATE_GENERIC_READ** et sont conservés dans cet État, comme requis par tous les tas de chargement. Si **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** n’a pas été défini lors de la compilation de l’opérateur, toutes les liaisons doivent être définies sur la table de liaison avant l’appel de **RecordDispatch** ; sinon, le comportement n’est pas défini. Dans le cas contraire, si un opérateur prend en charge la [liaison tardive](#optionally-specify-late-bound-operator-bindings), la liaison de ressources peut être différée jusqu’à ce que la liste de commandes Direct3D 12 soit envoyée à la file d’attente de commandes pour être exécutée.

**RecordDispatch** agit logiquement comme un appel à [**ID3D12GraphicsCommandList ::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch). Ainsi, les barrières de vue d’accès non ordonnées (UAV) sont nécessaires pour garantir un classement correct s’il existe des dépendances de données entre les distributions. Cette méthode n’insère pas de barrières UAV sur les ressources d’entrée ou de sortie. Votre application doit s’assurer que les barrières UAV correctes sont effectuées sur toutes les entrées si leur contenu dépend d’une distribution en amont, et sur toutes les sorties si des distributions en aval dépendent de ces sorties.

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>Durée de vie et synchronisation des descripteurs et de la table de liaison

Un bon modèle mental de liaison dans DirectML est que, en arrière-plan, la table de liaison DirectML crée et gère des descripteurs de vue d’accès non ordonnés (UAV) à l’intérieur du tas de descripteur que vous fournissez. Ainsi, toutes les règles Direct3D 12 habituelles s’appliquent autour de la synchronisation de l’accès à ce tas et à ses descripteurs. Il est de la responsabilité de votre application d’effectuer une synchronisation correcte entre le processeur et le travail GPU qui utilise une table de liaison.

Une table de liaison ne peut pas remplacer un descripteur pendant que le descripteur est en cours d’utilisation (par exemple, par une trame antérieure). Par conséquent, si vous souhaitez réutiliser un tas de descripteur déjà lié (par exemple, en appelant à nouveau bind * sur une table de liaison qui pointe vers celui-ci, ou en remplaçant manuellement le tas du descripteur), vous devez attendre que le répartiteur qui utilise actuellement le tas du descripteur termine l’exécution sur le GPU. Une table de liaison ne conservera pas une référence forte sur le tas de descripteur dans lequel elle écrit. vous ne doit pas donc la libération du tas de descripteur visible par le nuanceur de sauvegarde jusqu’à ce que tout le travail qui utilise cette table de liaison ait terminé l’exécution sur le GPU.

En revanche, si une table de liaison spécifie et gère un tas de descripteur, la table ne *contient* pas elle-même de mémoire. Ainsi, vous pouvez publier ou réinitialiser une table de liaison à tout moment après avoir appelé [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) (vous n’avez pas besoin d’attendre que cet appel se termine sur le GPU, tant que les descripteurs sous-jacents restent valides).

La table de liaison ne conserve pas de références fortes sur les ressources liées à l’aide de cette dernière &mdash; . votre application doit s’assurer que les ressources ne sont pas supprimées pendant qu’elle est en cours d’utilisation par le GPU. En outre, une table de liaison n’est pas thread-safe. &mdash; votre application ne doit pas appeler des méthodes sur une table de liaison simultanément à partir de différents threads sans synchronisation.

Et considérez que dans tous les cas, la reliaison est nécessaire uniquement lorsque vous modifiez les ressources liées. Si vous n’avez pas besoin de modifier les ressources liées, vous pouvez lier une seule fois au démarrage et transmettre la même table de liaison chaque fois que vous appelez **RecordDispatch**.

Pour entrelacer les charges de travail de Machine Learning et de rendu, assurez-vous simplement que les tables de liaison de chaque frame pointent vers des plages du tas de descripteurs qui ne sont pas déjà utilisées sur le GPU.

## <a name="optionally-specify-late-bound-operator-bindings"></a>Spécifier éventuellement des liaisons d’opérateur à liaison tardive

Si vous travaillez avec un opérateur compilé (plutôt qu’avec un initialiseur d’opérateur), vous avez la possibilité de spécifier la liaison tardive pour l’opérateur. Sans liaison tardive, vous devez définir toutes les liaisons sur la table de liaison avant d’enregistrer un opérateur dans une liste de commandes. Avec la liaison tardive, vous pouvez définir (ou modifier) des liaisons sur les opérateurs que vous avez déjà enregistrés dans une liste de commandes avant qu’elle ait été envoyée à la file d’attente de commandes.

Pour spécifier la liaison tardive, appelez [**IDMLDevice :: CompileOperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) avec un `flags` argument de [**DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE**](/windows/desktop/api/directml/ne-directml-dml_execution_flags).