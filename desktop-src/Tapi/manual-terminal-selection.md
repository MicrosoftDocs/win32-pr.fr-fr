---
description: Si les règles de sélection par défaut ne répondent pas aux besoins de l’application, l’application a la possibilité de sélectionner le terminal manuellement.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Sélection manuelle des terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755116"
---
# <a name="manual-terminal-selection"></a><span data-ttu-id="a3b7c-103">Sélection manuelle des terminaux</span><span class="sxs-lookup"><span data-stu-id="a3b7c-103">Manual Terminal Selection</span></span>

<span data-ttu-id="a3b7c-104">Si les règles de la sélection par défaut ne répondent pas aux besoins de l’application, l’application a la possibilité de sélectionner le terminal tel qu’il a toujours : autrement dit, il peut utiliser [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) pour énumérer les flux présents sur l’appel et sélectionner le terminal sur les flux appropriés (ou, dans le cas des terminaux multipiste, créer des pistes pour les flux et sélectionner des pistes créées sur les flux</span><span class="sxs-lookup"><span data-stu-id="a3b7c-104">If the rules of Default selection do not meet the needs of the application, the application has the option of selecting the terminal as it always has: that is, it can use [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) to enumerate the streams present on the call and select the terminal on the appropriate streams (or, in case of multitrack terminals, create tracks for the streams and select created tracks on the streams).</span></span>

 

 
