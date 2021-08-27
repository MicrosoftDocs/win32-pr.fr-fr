---
title: API WFP
description: l’API de la plateforme de filtrage des Windows (WFP) est composée des composants suivants.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eadbb3fb6383999b2bb8ef14c99ecb8beab3f88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470146"
---
# <a name="wfp-api"></a>API WFP

l’API de la plateforme de filtrage des Windows (WFP) est composée des composants suivants.




| Composant | Description | Fichiers d’en-tête | 
|-----------|-------------|--------------|
| <a href="/windows-hardware/drivers/ddi/_netvista/">API de légende</a> (FWPS) $ {Remove} $<br /> | <a href="/windows-hardware/drivers/ddi/_netvista/">Types de données</a> utilisés par les légendes. <strong>Remarque</strong>  ces types de données sont documentés dans Microsoft Windows Driver Development Kit (DDK).<br /> | <dl> fwpstypes. h<br />fwpstypes. idl<br /></dl> | 
| <a href="/windows-hardware/drivers/ddi/_netvista/">Fonctions</a> et <a href="/windows-hardware/drivers/ddi/_netvista/">types énumérés</a> utilisés pour implémenter des légendes. <strong>Remarque</strong>  Ces fonctions et types énumérés sont documentés dans le DDK.<br /> | <dl> fwpsu. h<br />fwpsk. h<br /></dl> | 
| API IKE/AuthIP (IKEEXT) $ {REMOVE} $<br /> | <a href="fwp-enums.md">Types énumérés</a> et <a href="fwp-structs.md">structures</a> utilisés pour gérer les associations de sécurité et de stratégie en mode principal IKE et AuthIP. | <dl> iketypes. h<br />iketypes. idl<br /></dl> | 
| <a href="fwp-ike-functions.md">Fonctions</a> utilisées pour gérer les associations de sécurité et de stratégie IKE et AuthIP mm. | <dl> fwpmu. h<br />fwpmk. h<br /></dl> | 
| API IPsec (IPSEC) $ {REMOVE} $<br /> | <a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion des stratégies IPSec et des associations de sécurité. | <dl> ipsectypes. h<br />ipsectypes. idl<br /></dl> | 
| <a href="fwp-ipsec-functions.md">Fonctions</a> utilisées pour gérer les stratégies IPSec et les associations de sécurité. | <dl> fwpmu. h<br />fwpmk. h<br /></dl> | 
| API de gestion (FWPM) $ {REMOVE} $<br /> | <a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion du moteur de filtre. | <dl> fwpmtypes. h<br />fwpmtypes. idl<br /></dl> | 
| <a href="fwp-mgmt-functions.md">Fonctions</a> utilisées pour gérer le moteur de filtre. Ces fonctions sont utilisées pour effectuer les tâches suivantes :<br /><ul><li>Définir et interroger des filtres, des fournisseurs et des légendes.</li><li>Récupérez les statistiques IPsec.</li><li>configurez la plateforme de filtrage Windows.</li></ul> | <dl> fwpmu. h<br />fwpmk. h<br /></dl> | 
| API partagée (FWP) | <a href="fwp-structs.md">structures</a> et <a href="fwp-enums.md">types énumérés</a> fondamentaux partagés sur la plateforme de filtrage Windows. | <dl> fwptypes. h<br />fwptypes. idl<br /></dl> | 




 

Les noms des types de données sont tous des majuscules et des traits de soulignement, délimités. Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Les noms de fonction sont en casse mixte et délimités par la casse. Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

La plupart des noms de données et de fonctions se terminent par un numéro de version. Le fichier d’en-tête fwpvi. h mappe des données et des noms de fonction indépendants de la version à la version qui est appropriée pour une utilisation avec un système d’exploitation donné. Pour plus d’informations, consultez [noms de Version-Independent WFP et ciblage de versions spécifiques de Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Chaque composant n’est pas autonome. Par exemple, les stratégies en mode principal IKE (MM) sont définies dans le composant IKEEXT, mais elles sont stockées dans un contexte de fournisseur et sont associées à un filtre qui se trouve dans le composant de l’API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>Fichiers d’en-tête publics User-Mode et Kernel-Mode

La plupart des fonctions WFP peuvent être appelées à partir du mode utilisateur ou du mode noyau. Toutefois, les fonctions en mode utilisateur retournent une valeur **DWORD** qui représente un code d’erreur Win32, tandis que les fonctions en mode noyau retournent une valeur **NTSTATUS** qui représente un code d’état NT. Par conséquent, les noms de fonction et la sémantique sont identiques entre le mode utilisateur et le mode noyau, mais pas les signatures de fonction. Cela requiert des en-têtes spécifiques en mode utilisateur et en mode noyau pour les prototypes de fonction. Les noms de fichiers d’en-tête en mode utilisateur se terminent par « u » et les noms de fichiers d’en-tête en mode noyau se terminent par « k ».

Le tableau suivant répertorie les fichiers d’en-tête Win32 qui définissent les fonctions WFP.

| Fichiers d’en-tête | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk. h      | Prototypes de fonction en mode noyau pour les composants FWPM, IPsec et IKEEXT. Disponible uniquement dans le DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu. h      | Prototypes de fonction en mode utilisateur pour les composants FWPM, IPsec et IKEEXT. disponible uniquement dans le kit de développement logiciel (SDK) de Microsoft Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk. h      | Prototypes de fonction en mode noyau et types énumérés pour le composant FWPS. Disponible uniquement dans le DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu. h      | Prototypes de fonction en mode utilisateur et types énumérés pour le composant FWPS. disponible dans le SDK Windows uniquement. **Remarque**  Les types énumérés FWPS en mode utilisateur sont identiques aux types énumérés FWPS en mode noyau. En conséquence, ces types sont documentés uniquement dans le DDK.<br/> **Remarque**  Les prototypes de fonction FWPS en mode utilisateur sont identiques aux prototypes de fonction FWPS en mode noyau, à l’exception du code de retour. Les fonctions FWPS en mode utilisateur retournent une **valeur DWORD**, tandis que les fonctions FWPS en mode noyau retournent un **NTSTATUS**. En conséquence, ces fonctions sont documentées dans le DDK uniquement.<br/> |



 

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

