---
description: Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits. Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier.
ms.assetid: f2090018-489f-400c-ae44-a6ad60710196
title: Prise en charge de la réorganisation de la séquence de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a563d5962ef80a0f3978a985684f8f85b68eae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952533"
---
# <a name="recognizer-stroke-reordering-support"></a><span data-ttu-id="fa2fa-103">Prise en charge de la réorganisation de la séquence de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="fa2fa-103">Recognizer Stroke Reordering Support</span></span>

<span data-ttu-id="fa2fa-104">Les Microsoft Recognizers du script latin prennent en charge la réorganisation des traits.</span><span class="sxs-lookup"><span data-stu-id="fa2fa-104">The Microsoft recognizers of Latin script support stroke reordering.</span></span>

<span data-ttu-id="fa2fa-105">Les reconnaissance de l’écriture manuscrite Microsoft du script latin ne dépendent pas des traits d’une ligne en cours d’écriture dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="fa2fa-105">The Microsoft handwriting recognizers of Latin script do not depend upon the strokes in a line being written in a particular order.</span></span> <span data-ttu-id="fa2fa-106">Au lieu de cela, les module de reconnaissance ordonnent les traits en interne en fonction des relations spatiales entre les traits.</span><span class="sxs-lookup"><span data-stu-id="fa2fa-106">Instead, the recognizers order the strokes internally based upon spatial relationships between the strokes.</span></span> <span data-ttu-id="fa2fa-107">Par exemple, les modules de reconnaissance du script latin prennent en charge le scénario courant dans lequel quelqu’un revient sur une ligne pour écrire une parenthèse ouvrante, « ( » ou pour ajouter des guillemets.</span><span class="sxs-lookup"><span data-stu-id="fa2fa-107">For example, the recognizers of Latin script support the common scenario in which someone goes back on a line to write a left parenthesis, "(", or to add quotation marks.</span></span>

 

 



