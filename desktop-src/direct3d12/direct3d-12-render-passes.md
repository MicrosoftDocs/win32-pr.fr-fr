---
title: Passes de rendu Direct3D 12
description: La fonctionnalité de passes de rendu permet à votre convertisseur d’améliorer l’efficacité du GPU en réduisant le trafic de mémoire vers/à partir de la mémoire hors puce. pour ce faire, il permet à votre application d’identifier plus facilement les exigences de classement de rendu des ressources et les dépendances de données.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: f776729f17ac0017d713c6f37bc71de7302a7c08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216412"
---
# <a name="direct3d-12-render-passes"></a>Passes de rendu Direct3D 12

la fonctionnalité de passes de rendu est une nouveauté pour Windows 10, version 1809 (10,0 ; Build 17763), et introduit le concept d’une passe de rendu Direct3D 12. Une passe de rendu se compose d’un sous-ensemble des commandes que vous enregistrez dans une liste de commandes.

Pour déclarer où chaque passe de rendu commence et se termine, vous imbriquez les commandes appartenant à cette passe dans les appels à [**ID3D12GraphicsCommandList4 :: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) et [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Par conséquent, toute liste de commandes contient zéro, une ou plusieurs passes de rendu.

## <a name="scenarios"></a>Scénarios

Les passes de rendu peuvent améliorer les performances de votre convertisseur s’il est basé sur Tile-Based le rendu différé (TBDR), entre autres techniques. Plus précisément, la technique permet à votre convertisseur d’améliorer l’efficacité du GPU en réduisant le trafic de mémoire vers/à partir de la mémoire hors puce en permettant à votre application d’identifier plus facilement les exigences de classement des ressources et les dépendances de données.

Un pilote d’affichage écrit expressément pour tirer parti de la fonctionnalité de passes de rendu donne les meilleurs résultats. Toutefois, les API de tests de rendu peuvent s’exécuter même sur des pilotes préexistants (mais pas nécessairement avec des améliorations de performances).

Voici les scénarios dans lesquels les passes de rendu sont conçues pour fournir de la valeur.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Autoriser votre application à éviter les chargements/magasins de ressources inutiles de/vers la mémoire principale sur une Tile-Based architecture de rendu différée (TBDR)

L’une des propositions de valeur des passes de rendu est qu’elle vous fournit un emplacement central pour indiquer les dépendances de données de votre application pour un ensemble d’opérations de rendu. Ces dépendances de données permettent au pilote d’affichage d’inspecter ces données au moment de la liaison ou de la barrière, et d’émettre des instructions qui réduisent les chargements/magasins de ressources de/vers la mémoire principale.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Autoriser votre architecture TBDR à associer façon opportuniste des ressources persistantes dans le cache sur puce sur les passes de rendu (même dans des listes de commandes distinctes)

> [!NOTE]
> Plus précisément, ce scénario est limité aux cas où vous écrivez dans les mêmes cibles de rendu sur plusieurs listes de commandes.

Un modèle de rendu courant permet à votre application de s’afficher en série sur les mêmes cibles de rendu sur plusieurs listes de commandes, même si les commandes de rendu sont générées en parallèle. Grâce à l’utilisation des passes de rendu dans ce scénario, ces passes sont combinées de manière à ce que le pilote d’affichage puisse éviter de vider la mémoire principale sur les limites de la liste de commandes, ce qui permet de les combiner.

## <a name="your-applications-responsibilities"></a>Responsabilités de votre application

Même avec la fonctionnalité de passes de rendu, le runtime Direct3D 12 et le pilote d’affichage ne prennent pas la responsabilité de déduire les opportunités de réorganisation et d’éviter les chargements et les magasins. Pour tirer correctement parti de la fonctionnalité de passes de rendu, votre application a ces responsabilités.

- Identifiez correctement les dépendances de classement et de données pour ses opérations.
- Commandez ses soumissions d’une manière qui minimise les vidages (par conséquent, réduisez l’utilisation des indicateurs de **_PRESERVE** ).
- Utilisez correctement les barrières des ressources et suivez l’état des ressources.
- Évitez les copies/effaces inutiles. pour vous aider à les identifier, vous pouvez utiliser les avertissements de performances automatisés à partir de l' [outil PIX sur Windows](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Utilisation de la fonctionnalité de réussite de rendu

### <a name="what-is-a-render-pass"></a>Qu’est-ce qu’une *passe de rendu*?

Une passe de rendu est définie par ces éléments.

- Ensemble de liaisons de sortie qui sont fixes pour la durée de la passe de rendu. Ces liaisons sont vers une ou plusieurs vues de la cible de rendu (RTVs), et/ou vers une vue de stencil de profondeur (DSV).
- Liste des opérations GPU qui ciblent cet ensemble de liaisons de sortie.
- Métadonnées qui décrivent les dépendances de chargement/stockage pour toutes les liaisons de sortie ciblées par la passe de rendu.

### <a name="declare-your-output-bindings"></a>Déclarer vos liaisons de sortie

Au début d’une passe de rendu, vous déclarez des liaisons à vos cibles de rendu et/ou à votre mémoire tampon de stencil/profondeur. Il est facultatif de lier à la ou les cibles de rendu, et il est facultatif de lier à une mémoire tampon de stencil/profondeur. Toutefois, vous devez établir une liaison avec au moins l’un des deux, et dans l’exemple de code ci-dessous, nous créons une liaison vers les deux.

Vous déclarez ces liaisons dans un appel à [**ID3D12GraphicsCommandList4 :: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

Vous définissez le premier champ de la structure [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) sur le handle de descripteur de processeur correspondant à une ou plusieurs vues de la cible de rendu (RTVs). De même, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contient le handle de descripteur de processeur correspondant à une vue de stencil de profondeur (DSV). Ces handles de descripteur de processeur sont les mêmes que ceux que vous transmettez autrement à [**ID3D12GraphicsCommandList :: OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). Et, comme avec **OMSetRenderTargets**, les descripteurs d’UC sont *alignés* à partir de leurs tas (descripteur de processeur) respectifs au moment de l’appel à **BeginRenderPass**.

Les RTVs et DSV ne sont pas hérités dans la passe de rendu. Au lieu de cela, elles doivent être définies. Par ailleurs, les RTVs et DSV déclarés dans **BeginRenderPass** sont propagés à la liste de commandes. Au lieu de cela, ils sont dans un État non défini après la passe de rendu.

### <a name="render-passes-and-workloads"></a>Rendu des passes et des charges de travail

Vous ne pouvez pas imbriquer des passes de rendu et vous ne pouvez pas avoir une passe de rendu sur plusieurs listes de commandes (elles doivent commencer et se terminer lors de l’enregistrement dans une liste de commandes unique). Les optimisations conçues pour permettre une génération multithread efficace de passes de rendu sont présentées dans la section [ indicateurs de réussite de rendu](#render-pass-flags), ci-dessous.

Une écriture que vous effectuez à partir d’une passe de rendu n’est pas *valide* pour la lecture jusqu’à la réussite d’un rendu suivant. Cela exclut certains types de barrières de la passe de rendu &mdash; , par exemple, la barrière de **RENDER_TARGET** à **SHADER_RESOURCE** sur la cible de rendu actuellement liée. Pour plus d’informations, consultez la section [tests de réussite et barrières des ressources](#render-passes-and-resource-barriers), ci-dessous.

La seule exception à la contrainte d’écriture/lecture qui vient d’être mentionnée implique les lectures implicites qui se produisent dans le cadre du test de profondeur et de la fusion de cibles de rendu.
Par conséquent, ces API ne sont pas autorisées dans une passe de rendu (le runtime principal supprime la liste de commandes si l’une d’elles est appelée lors de l’enregistrement).

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList::ClearState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList ::D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList ::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Tests de rendu et barrières des ressources

Vous ne pouvez pas lire ou consommer une écriture qui s’est produite dans la même passe de rendu. Certains obstacles ne sont pas conformes à cette contrainte, par exemple de **D3D12_RESOURCE_STATE_RENDER_TARGET** à **\* _SHADER_RESOURCE** sur la cible de rendu actuellement liée (et la couche de débogage génère une erreur). Toutefois, ce même cloisonnement sur une cible de rendu qui a été écrite *en dehors* de la passe de rendu actuelle est conforme, car les écritures se terminent avant le démarrage de la passe de rendu en cours.
Il peut être utile de connaître certaines optimisations qu’un pilote d’affichage peut effectuer à cet égard. Dans le cas d’une charge de travail conforme, un pilote d’affichage peut déplacer les barrières rencontrées dans votre passe de rendu vers le début de la passe de rendu. À partir de là, ils peuvent être fusionnés (et ne pas interférer avec les opérations de mosaïque/compartimentage). Il s’agit d’une optimisation valide, à condition que toutes vos écritures soient terminées avant le démarrage de la passe de rendu en cours.

Voici un exemple plus complet d’optimisation de pilote, qui suppose que vous disposez d’un moteur de rendu qui a une conception de liaison de ressources de type pré-Direct3D à 12, qui fait &mdash; *des obstacles à la demande* en fonction de la façon dont les ressources sont liées. Lors de l’écriture dans un affichage d’accès non ordonné (UAV) vers la fin d’un frame (à consommer dans le frame suivant), il peut arriver que le moteur laisse la ressource dans l’état **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** à la fin du frame. Dans le frame qui suit, lorsque le moteur se lie à la ressource en tant que vue de ressource de nuanceur (SRV), il détecte que la ressource n’est pas dans l’état correct, et il émet une barrière de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** à **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Si cette barrière se produit au cours de la passe de rendu, le pilote d’affichage est justifié en supposant que toutes les écritures ont déjà eu lieu *en dehors* de cette passe de rendu actuelle. par conséquent, le pilote d’affichage peut *déplacer* le cloisonnement jusqu’au début de la passe de rendu. Là encore, cela est valide, à condition que votre code soit conforme à la contrainte d’écriture/lecture décrite dans cette section et dans la dernière.


Voici des exemples de barrières conformes.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** à **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** à **\* _SHADER_RESOURCE**.

Et il s’agit d’exemples de barrières non conformes.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** à n’importe quel état de lecture sur les RTVs/DSV actuellement liés.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** à n’importe quel état de lecture sur les RTVs/DSV actuellement liés.
- Toute barrière d’alias.
- Barrières de vue d’accès non triée (UAV). 

### <a name="resource-access-declaration"></a>Déclaration d’accès aux ressources

Au moment de la **BeginRenderPass** , ainsi que de la déclaration de toutes les ressources qui servent de RTVs et/ou de DSV dans le cadre de cette étape, vous devez également spécifier leurs caractéristiques d' *accès* de début et de fin. Comme vous pouvez le voir dans l’exemple de code de la section [déclarer vos liaisons de sortie](#declare-your-output-bindings) ci-dessus, vous le faites avec les structures [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) et [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) .

Pour plus d’informations, consultez les structures [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) et [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) , ainsi que les énumérations [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) et [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Indicateurs de passe de rendu

Le dernier paramètre passé à **BeginRenderPass** est un indicateur de passe de rendu (une valeur de l’énumération [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) ).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>UAV écrit dans une passe de rendu

Les écritures de vue d’accès non triée (UAV) sont autorisées dans une passe de rendu, mais vous devez spécifiquement indiquer que vous enverrez des écritures UAV dans la passe de rendu en spécifiant **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, afin que le pilote d’affichage puisse refuser la mosaïque si nécessaire.

Les accès UAV doivent suivre la contrainte d’écriture/lecture décrite ci-dessus (les écritures dans une passe de rendu ne sont pas valides pour la lecture jusqu’à une réussite de rendu ultérieure). Les barrières UAV ne sont pas autorisées dans une passe de rendu.

Les liaisons UAV (via les tables racines ou les descripteurs racine) sont héritées dans les passes de rendu et sont propagées en dehors des passes de rendu.

#### <a name="suspending-passes-and-resuming-passes"></a>Interruption-passe et reprise-passes

Vous pouvez indiquer qu’une réussite de rendu entière est une passe de suspension et/ou une passe de reprise. Une paire d’interruptions suivies d’une pause doit avoir des indicateurs de vues/d’accès identiques entre les passes. et peuvent ne pas avoir d’opérations GPU intervenues (par exemple, des opérations de dessin, de distribution, de suppression, d’effacement, de copie, de mise à jour-vignette-mappage, d’écriture-mémoire tampon, de requêtes, de résolution de requêtes) entre le test de rendu de suspension et la réussite de reprise.

Le cas d’usage prévu est le rendu multithread, où quatre listes de commandes (chacune avec leurs propres passes de rendu) peuvent cibler les mêmes cibles de rendu. Lorsque les passes de rendu sont suspendues/reprises dans les listes de commandes, les listes de commandes doivent être exécutées dans le même appel à [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Une réussite de rendu peut être à la fois reprise et suspendue. Dans l’exemple multithread qui vient d’être donné, les listes de commandes 2 et 3 se reprennent respectivement de 1 et 2. Et, en même temps, 2 et 3 s’interrompent respectivement à 3 et 4.

## <a name="query-for-render-passes-feature-support"></a>Requête de prise en charge des fonctionnalités de réussite de rendu

Vous pouvez appeler [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) pour rechercher dans quelle mesure un pilote de périphérique et/ou le matériel prend en charge efficacement les passes de rendu.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

En raison de la logique de mappage du runtime, les passes de rendu fonctionnent toujours. Toutefois, en fonction de la prise en charge des fonctionnalités, elles ne fournissent pas toujours un avantage. Vous pouvez utiliser du code semblable à l’exemple de code ci-dessus pour déterminer si/à quel moment il vaut mieux émettre des commandes en tant que passes de rendu, et quand il ne s’agit pas vraiment d’un avantage (autrement dit, lorsque le runtime est simplement mappé à la surface d’API existante). L’exécution de cette vérification est particulièrement importante si vous utilisez [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Pour obtenir une description des trois niveaux de prise en charge, consultez l’énumération [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) .
