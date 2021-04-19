---
title: API WFP
description: L’API WFP (Windows Filtering Platform) est composée des composants suivants.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106509891"
---
# <a name="wfp-api"></a>API WFP

L’API WFP (Windows Filtering Platform) est composée des composants suivants.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Composant</th>
<th>Description</th>
<th>Fichiers d’en-tête</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><a href="/windows-hardware/drivers/ddi/_netvista/">API de légende</a> (FWPS) $ {Remove} $<br />
</td>
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Types de données</a> utilisés par les légendes. <strong>Remarque</strong>  Ces types de données sont documentés dans le kit de développement de pilotes (DDK) Microsoft Windows.<br/></td>
<td><dl> fwpstypes. h<br />
fwpstypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Fonctions</a> et <a href="/windows-hardware/drivers/ddi/_netvista/">types énumérés</a> utilisés pour implémenter des légendes. <strong>Remarque</strong>  Ces fonctions et types énumérés sont documentés dans le DDK.<br/></td>
<td><dl> fwpsu. h<br />
fwpsk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IKE/AuthIP (IKEEXT) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Types énumérés</a> et <a href="fwp-structs.md">structures</a> utilisés pour gérer les associations de sécurité et de stratégie en mode principal IKE et AuthIP.</td>
<td><dl> iketypes. h<br />
iketypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ike-functions.md">Fonctions</a> utilisées pour gérer les associations de sécurité et de stratégie IKE et AuthIP mm.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IPsec (IPSEC) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion des stratégies IPSec et des associations de sécurité.</td>
<td><dl> ipsectypes. h<br />
ipsectypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ipsec-functions.md">Fonctions</a> utilisées pour gérer les stratégies IPSec et les associations de sécurité.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API de gestion (FWPM) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion du moteur de filtre.</td>
<td><dl> fwpmtypes. h<br />
fwpmtypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-mgmt-functions.md">Fonctions</a> utilisées pour gérer le moteur de filtre. Ces fonctions sont utilisées pour effectuer les tâches suivantes :<br/>
<ul>
<li>Définir et interroger des filtres, des fournisseurs et des légendes.</li>
<li>Récupérez les statistiques IPsec.</li>
<li>Configurez la plateforme de filtrage Windows.</li>
</ul></td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td>API partagée (FWP)</td>
<td><a href="fwp-structs.md">Structures</a> et <a href="fwp-enums.md">types énumérés</a> fondamentaux partagés sur la plateforme de filtrage Windows.</td>
<td><dl> fwptypes. h<br />
fwptypes. idl<br />
</dl></td>
</tr>
</tbody>
</table>



 

Les noms des types de données sont tous des majuscules et des traits de soulignement, délimités. Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Les noms de fonction sont en casse mixte et délimités par la casse. Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

La plupart des noms de données et de fonctions se terminent par un numéro de version. Le fichier d’en-tête fwpvi. h mappe des données et des noms de fonction indépendants de la version à la version qui est appropriée pour une utilisation avec un système d’exploitation donné. Pour plus d’informations, consultez [noms de Version-Independent WFP et cibler des versions spécifiques de Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Chaque composant n’est pas autonome. Par exemple, les stratégies en mode principal IKE (MM) sont définies dans le composant IKEEXT, mais elles sont stockées dans un contexte de fournisseur et sont associées à un filtre qui se trouve dans le composant de l’API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>Fichiers d’en-tête publics User-Mode et Kernel-Mode

La plupart des fonctions WFP peuvent être appelées à partir du mode utilisateur ou du mode noyau. Toutefois, les fonctions en mode utilisateur retournent une valeur **DWORD** qui représente un code d’erreur Win32, tandis que les fonctions en mode noyau retournent une valeur **NTSTATUS** qui représente un code d’état NT. Par conséquent, les noms de fonction et la sémantique sont identiques entre le mode utilisateur et le mode noyau, mais pas les signatures de fonction. Cela requiert des en-têtes spécifiques en mode utilisateur et en mode noyau pour les prototypes de fonction. Les noms de fichiers d’en-tête en mode utilisateur se terminent par « u » et les noms de fichiers d’en-tête en mode noyau se terminent par « k ».

Le tableau suivant répertorie les fichiers d’en-tête Win32 qui définissent les fonctions WFP.

| Fichiers d’en-tête | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk. h      | Prototypes de fonction en mode noyau pour les composants FWPM, IPsec et IKEEXT. Disponible uniquement dans le DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu. h      | Prototypes de fonction en mode utilisateur pour les composants FWPM, IPsec et IKEEXT. Disponible uniquement dans le kit de développement logiciel (SDK) Microsoft Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk. h      | Prototypes de fonction en mode noyau et types énumérés pour le composant FWPS. Disponible uniquement dans le DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu. h      | Prototypes de fonction en mode utilisateur et types énumérés pour le composant FWPS. Disponible dans le SDK Windows uniquement. **Remarque**  Les types énumérés FWPS en mode utilisateur sont identiques aux types énumérés FWPS en mode noyau. En conséquence, ces types sont documentés uniquement dans le DDK.<br/> **Remarque**  Les prototypes de fonction FWPS en mode utilisateur sont identiques aux prototypes de fonction FWPS en mode noyau, à l’exception du code de retour. Les fonctions FWPS en mode utilisateur retournent une **valeur DWORD**, tandis que les fonctions FWPS en mode noyau retournent un **NTSTATUS**. En conséquence, ces fonctions sont documentées dans le DDK uniquement.<br/> |



 

Toutes les fonctions en mode utilisateur sont exportées à partir de fwpuclnt.dll. Toutes les fonctions en mode noyau sont exportées à partir de fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Types de données Management (FWPM) et Callout (FWPS)

La plupart des types de données FWPM, qui sont utilisés pour les tâches de gestion telles que l’ajout de filtres ou de légendes à partir d’une application ou d’un pilote, ont des équivalents FWPS. Les types de données FWPS sont utilisés lors du filtrage réel du trafic réseau, dans le contexte d’une routine de légende pour la classification.

Par exemple, pour ajouter un filtre à une certaine couche du moteur de filtrage, le programmeur doit utiliser un type FWPM, comme : `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Pour vérifier la couche à partir de laquelle une légende est appelée, le programmeur doit utiliser le type FWPS correspondant : ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Certains FWPS équivalents aux types de données FWPM développent les types de données FWPM d’origine. Par exemple, pour ajouter une condition de filtre à de nombreuses couches du moteur de filtrage, le programmeur spécifie `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` quelle que soit la couche du moteur de filtrage. Pour rechercher une valeur de condition de filtre, le programmeur spécifie un type FWPS spécifique à la couche, par exemple : `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

Les types de données FWPS sont généralement plus petits que leurs équivalents FWPM. Par exemple, les [**identificateurs de couche de filtrage FWPM**](management-filtering-layer-identifiers-.md) sont des **GUID** s (16 octets) tandis que les [identificateurs de couche de filtrage FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) sont **UINT16** (16 bits). La taille réduite pour les types de données FWPS améliore les performances du système, car les comparaisons de nombres entiers compensent les comparaisons de **GUID** pour le trafic en temps réel. En outre, la mémoire du noyau est utilisée efficacement, car les types FWPS sont utilisés dans le noyau pour gérer les filtres, tandis que les types FWPM sont stockés en mode utilisateur pour gérer les différentes couches.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle objet de l’API WFP](object-model.md)
</dt> <dt>

[Gestion des objets de l’API WFP](object-management.md)
</dt> </dl>

