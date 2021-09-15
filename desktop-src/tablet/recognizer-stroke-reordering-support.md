---
description: Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits. Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier.
ms.assetid: f2090018-489f-400c-ae44-a6ad60710196
title: Prise en charge de la réorganisation de la séquence de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a563d5962ef80a0f3978a985684f8f85b68eae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411449"
---
# <a name="recognizer-stroke-reordering-support"></a>Prise en charge de la réorganisation de la séquence de reconnaissance

Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits.

Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier. Au lieu de cela, les module de reconnaissance ordonnent les traits en interne en fonction des relations spatiales entre les traits. Par exemple, les modules de reconnaissance du script latin prennent en charge le scénario courant dans lequel quelqu’un revient sur une ligne pour écrire une parenthèse ouvrante, « ( » ou pour ajouter des guillemets.

 

 



