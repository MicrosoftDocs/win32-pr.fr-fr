---
description: Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits. Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier.
ms.assetid: f2090018-489f-400c-ae44-a6ad60710196
title: Prise en charge de la réorganisation de la séquence de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e113ac3d32cf731fecd6a22339088883a5e44cd092b752dae3273a719b3b1f6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966838"
---
# <a name="recognizer-stroke-reordering-support"></a>Prise en charge de la réorganisation de la séquence de reconnaissance

Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits.

Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier. Au lieu de cela, les module de reconnaissance ordonnent les traits en interne en fonction des relations spatiales entre les traits. Par exemple, les modules de reconnaissance du script latin prennent en charge le scénario courant dans lequel quelqu’un revient sur une ligne pour écrire une parenthèse ouvrante, « ( » ou pour ajouter des guillemets.

 

 



