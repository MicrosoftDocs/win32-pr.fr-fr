---
title: Itinéraires statiques et statiques
description: En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127829"
---
# <a name="static-and-autostatic-routes"></a>Itinéraires statiques et statiques

En règle générale, les itinéraires vers des réseaux distants sont obtenus de manière dynamique via des protocoles de routage. Toutefois, l’administrateur peut également *amorcer* la table de routage en fournissant des itinéraires manuellement. Ces itinéraires sont appelés *statiques*. Un itinéraire statique est associé à une interface qui représente le réseau distant. Contrairement aux itinéraires dynamiques, les itinéraires statiques sont conservés même si le routeur est redémarré ou si l’interface est désactivée.

Un itinéraire *autostatique* est obtenu via un protocole de routage, mais une fois obtenu se comporte comme un itinéraire statique. Le processus d’obtention des itinéraires autostatiques est le suivant : le gestionnaire de routeur IPX ou IP émet une demande selon laquelle un protocole de routage met à jour les informations de routage pour une interface spécifique. Les résultats de la mise à jour sont ensuite convertis en itinéraires statiques. Notez que seuls certains protocoles de routage prennent en charge les demandes de mises à jour d’itinéraires autostatiques.

 

 




