---
description: Représentation des fonctionnalités
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Représentation des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866505"
---
# <a name="representing-functionality"></a>Représentation des fonctionnalités

Il existe des objets fonctionnels permettant d’identifier ou de regrouper logiquement les fonctionnalités d’un appareil. Par exemple, une application peut voir qu’un appareil prend en charge SMS en recherchant l’objet fonctionnel SMS. De même, l’application peut voir qu’un appareil possède des fonctionnalités d’appareil photo en recherchant l’objet fonctionnel de capture d’image continue.

Cette représentation d’objet flexible facilite la prise en charge des appareils avec des fonctionnalités multifonction. Les pilotes peuvent simplement exposer les objets fonctionnels qui représentent leur appareil, ce qui est plus granulaire que l’utilisation des classes de périphériques traditionnelles. La représentation d’objet permet également d’isoler les éléments fonctionnels qui se chevauchent. par exemple, certains téléphones peuvent avoir deux caméras ou quatre stockages.

Dans le système d’exploitation Windows 7, les services étendent les objets fonctionnels en fournissant des requêtes riches de fonctionnalités et un regroupement abstrait de contenu. Les applications peuvent utiliser des services pour découvrir des fonctionnalités d’appareil et interagir avec le contenu de manière plus efficace. Par exemple, une application peut voir qu’un appareil prend en charge les fonctionnalités de synchronisation des contacts en recherchant un objet de service de contacts et peut trouver tous les contacts en tant qu’objets enfants de l’objet de service, sans avoir à effectuer une recherche récursive dans la hiérarchie de stockage.

Les services permettent également aux applications de découvrir et d’appeler un comportement personnalisé sur un appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> </dl>

 

 



