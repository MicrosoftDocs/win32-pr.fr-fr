---
description: Le modèle CMSPArray implémente un tableau intelligent qui s’agrandit à la demande.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952097"
---
# <a name="cmsparray"></a>CMSPArray

Le modèle CMSPArray implémente un tableau intelligent qui s’agrandit à la demande. Il est conçu pour contenir des tableaux de petite taille avec des types de données simples. Elle n’a pas de section critique. Ses seules dépendances sont **realloc** et **memmove**. Il est utilisé en interne pour conserver les listes de pointeurs d’objets. Elle est similaire à l’implémentation **CSimpleArray** d’ATL, mais elle est plus efficace pour les allocations initiales.

Ce modèle est défini dans MSPutils. h.

 

 



