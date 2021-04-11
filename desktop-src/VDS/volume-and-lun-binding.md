---
description: Liaison de volume et de numéro d’unité logique
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Liaison de volume et de numéro d’unité logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211156"
---
# <a name="volume-and-lun-binding"></a>Liaison de volume et de numéro d’unité logique

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La liaison est la création de volumes ou de numéros d’unités logiques. Les volumes sont constitués d’étendues de disque et les numéros d’unités logiques sont constitués d’étendues de lecteurs. La liaison sélectionne pour un ensemble de mappages aux ressources physiques et se produit dans un sous-système, dans un Pack, ou les deux. Tous les programmes fournisseurs prennent en charge la liaison partiellement dirigée d’un modèle dans lequel l’appelant spécifie uniquement les attributs de liaison présentant un intérêt particulier, et permet au fournisseur de choisir le reste. Les opérations dans VDS pour les volumes de liaison et les numéros d’unités logiques sont similaires, mais pas identiques. Par exemple, les fournisseurs de matériel peuvent offrir des options de liaison supplémentaires.

VDS prend en charge les cinq types de liaison de volume et LUN suivants pour les configurations partiellement dirigées. (Les fournisseurs de matériel peuvent et prennent en charge de nombreuses autres liaisons.)



| Terme                                                                                                                                             | Description                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple<br/>                                                     | Mappage linéaire avec une seule étendue contiguë.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Fractionnés<br/>                                                 | Mappage linéaire avec plusieurs extensions non contiguës sur plusieurs disques ou lecteurs.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Agrégés par bandes<br/>                                                 | Le mappage qui entrelace les extensions de volume contiguës sur plusieurs disques ou lecteurs.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mise en miroir<br/>                                             | Mappage qui gère au moins deux copies de données identiques.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Agrégé par bandes avec parité<br/> | Mappage qui distribue les informations de vérification de parité sur plusieurs disques ou lecteurs.<br/>  |



 

VDS crée des liaisons miroir, agrégées par bandes et agrégées par bandes à partir de plusieurs membres. Par exemple, un miroir bidirectionnel a deux membres. Chaque membre peut occuper des étendues sur plusieurs disques ou lecteurs. VDS concatène les étendues pour former le membre, puis lie le volume ou le numéro d’unité logique sur les membres. Un fournisseur peut prendre en charge tous les types de liaison, ou n’importe quel sous-ensemble. Dans le modèle objet VDS, chaque membre d’un miroir est un objet indépendant appelé Plex.

Là encore, les types de volume et de LUN sont similaires, mais pas exacts. Pour obtenir une description des types de volumes, consultez l' [objet volume](volume-object.md). pour les types de LUN, consultez l' [objet lun](lun-object.md). Les types de liaison n’ont pas de tolérance de panne ou de tolérance de panne.

### <a name="non-fault-tolerant-binding"></a>Liaison non tolérante aux pannes

Les volumes non tolérants aux pannes et les numéros d’unités logiques n’offrent pas de récupération d’urgence. Si l’un des piles qui contribue à un volume ou un numéro d’unité logique non tolérant aux pannes échoue, l’intégralité du volume ou de la LUN échoue. En échange des risques de données, les volumes à tolérance de panne et les LUN offrent des performances d’entrée/sortie qui sont généralement supérieures à celles des volumes à tolérance de pannes et des numéros d’unités logiques. VDS prend en charge les trois types suivants non tolérants aux pannes : simple, fractionné et agrégé par bandes.

Simple

![Diagramme illustrant un type simple à tolérance de pannes avec 2 packs et 2 sous-systèmes.](images/vdssimplelunvol.png)

Réparti

![Diagramme qui montre un type non tolérant aux pannes avec 1 Pack et un sous-système.](images/vdsspanlunvol.png)

Agrégés par bandes

![Diagramme qui montre un type entrelacé non tolérant aux pannes avec 1 Pack et 1 sous-système.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Liaison à tolérance de panne

Les volumes à tolérance de panne et les numéros d’unités logiques suivants offrent une récupération d’urgence. Si l’un des piles qui contribue à un volume à tolérance de panne ou à un numéro d’unité logique (LUN) tombe en panne, les données peuvent être récupérées. Dans Exchange pour la sécurité des données, les performances d’entrée/sortie des volumes à tolérance de pannes et des numéros d’unités logiques sont généralement inférieures à celles des volumes et des numéros d’unités logiques non tolérants aux pannes. VDS prend en charge deux types de tolérance de panne : mis en miroir et agrégé par bandes avec parité.

En miroir (miroir triple)

![Diagramme illustrant un type de tolérance de panne en miroir (miroir 3-Way).](images/vdsmirrorlunvol.png)

Agrégé par bandes avec parité

![Diagramme qui montre un type de tolérance de panne de parité agrégé par bandes.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de la configuration](configuration.md)
</dt> <dt>

[Objet volume](volume-object.md)
</dt> <dt>

[LUN (objet)](lun-object.md)
</dt> </dl>

 

