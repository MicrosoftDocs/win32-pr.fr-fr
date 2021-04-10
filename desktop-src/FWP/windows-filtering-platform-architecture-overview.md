---
title: Architecture WFP
description: Cette section fournit une brève vue d’ensemble de l’architecture de la plateforme de filtrage Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104199193"
---
# <a name="wfp-architecture"></a>Architecture WFP

L’illustration suivante montre l’architecture de base de la plateforme de filtrage Windows (WFP).

![architecture de base du diagramme de plateforme de filtrage Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a>Moteur de filtre

Le moteur de filtre contient un composant en mode utilisateur et un composant en mode noyau, qui ensemble effectuent toutes les opérations de filtrage sur les données réseau. Le moteur de filtre contient plusieurs couches de filtrage qui sont mappées librement aux couches de la pile de mise en réseau du système d’exploitation. Les couches du moteur de filtre sont divisées en couches en mode utilisateur et en couches en mode noyau, en fonction du composant moteur de filtre qui les possède.

Le composant de mode utilisateur effectue le filtrage RPC et IPsec. Le moteur de filtre contient environ 10 couches de filtrage en mode utilisateur.

Le composant en mode noyau effectue le filtrage au niveau du réseau et des couches de transport de la pile TC/IP. Ce composant appelle également les fonctions de légende disponibles pendant le processus de [classification](basic-operation.md) . Le moteur de filtre contient environ 50 couches de filtrage en mode noyau.

Pour obtenir une description de chacune des couches du moteur de filtre, consultez [**filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md) .

## <a name="base-filtering-engine"></a>Moteur de filtrage de base

Le moteur de filtrage de base (BFE) est un service en mode utilisateur (bfe.dll s’exécutant dans un processus de svchost.exe) qui coordonne les composants WFP. Les principales tâches effectuées par BFE sont l’ajout et la suppression de filtres du système, le stockage de la configuration du filtre et l’application de la sécurité de la configuration WFP. Les applications communiquent avec BFE par le biais des [fonctions de gestion WFP](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Pilotes de légende

Les pilotes de légende offrent des fonctionnalités de filtrage supplémentaires en ajoutant des fonctions de légende personnalisées au moteur de filtre à une ou plusieurs couches de filtrage en mode noyau. Les légendes prennent en charge l’inspection détaillée et les paquets, ainsi que la modification de flux. Une fois qu’un pilote Callout a ajouté ses fonctions de légende au moteur de filtre, les filtres qui spécifient la fonction de légende d’un pilote donné peuvent être ajoutés au processus de filtrage. Ces filtres peuvent être ajoutés soit par une application de gestion en mode utilisateur, soit par le pilote de légende lui-même. L’interface en mode noyau, fournie dans le kit de développement Windows, ne doit être utilisée qu’en cas de besoin et non en remplacement de l’API en mode utilisateur.

> [!Note]  
> Pour plus d’informations sur les pilotes de légende, consultez la section plateforme de filtrage Windows du [Kit de développement Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

La plateforme de filtrage Windows comprend un certain nombre de fonctions de légende intégrées qui peuvent être utilisées pour la communication sécurisée des données IPsec, les paramètres de filtrage avec état et le filtrage en mode furtif. Pour obtenir la liste complète des fonctions de légende intégrées, consultez [**identificateurs de légende intégrés**](built-in-callout-identifiers.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle objet](object-model.md)
</dt> <dt>

[Opération WFP](basic-operation.md)
</dt> <dt>

[Pilotes de la plateforme de filtrage Windows-Guide de conception](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Pilotes de la légende de la plateforme de filtrage Windows-référence](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 