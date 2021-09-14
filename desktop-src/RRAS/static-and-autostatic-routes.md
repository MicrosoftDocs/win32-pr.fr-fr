---
title: Itinéraires statiques et statiques
description: En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121257"
---
# <a name="static-and-autostatic-routes"></a>Itinéraires statiques et statiques

En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage. Toutefois, l’administrateur peut également *amorcer* la table de routage en fournissant des itinéraires manuellement. Ces itinéraires sont appelés *statiques*. Un itinéraire statique est associé à une interface qui représente le réseau distant. Contrairement aux itinéraires dynamiques, les itinéraires statiques sont conservés même si le routeur est redémarré ou si l’interface est désactivée.

Un itinéraire *autostatique* est obtenu via un protocole de routage, mais une fois obtenu se comporte comme un itinéraire statique. Le processus d’obtention des itinéraires autostatiques est le suivant : le gestionnaire de routeur IPX ou IP émet une demande selon laquelle un protocole de routage met à jour les informations de routage pour une interface spécifique. Les résultats de la mise à jour sont ensuite convertis en itinéraires statiques. Notez que seuls certains protocoles de routage prennent en charge les demandes de mises à jour d’itinéraires autostatiques.

 

 




