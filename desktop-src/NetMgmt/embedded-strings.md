---
title: Chaînes incorporées
description: Les structures d’informations ne contiennent pas de chaînes incorporées. Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673918"
---
# <a name="embedded-strings"></a><span data-ttu-id="9d301-104">Chaînes incorporées</span><span class="sxs-lookup"><span data-stu-id="9d301-104">Embedded Strings</span></span>

<span data-ttu-id="9d301-105">Les structures d’informations ne contiennent pas de chaînes incorporées.</span><span class="sxs-lookup"><span data-stu-id="9d301-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="9d301-106">Cela améliore l’alignement des structures d’informations et permet la flexibilité OEM dans les fonctions principales.</span><span class="sxs-lookup"><span data-stu-id="9d301-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="9d301-107">Tout champ d’information retourné dans un appel d’énumération qui peut être utilisé par la suite comme clé pour l’appel à une fonction de gestion réseau GetInfo est toujours présent dans la mémoire tampon d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9d301-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="9d301-108">Si la chaîne d’informations de longueur variable qui spécifie la valeur du champ clé ne peut pas être contenue, l’intégralité de la structure de longueur fixe de l’entrée n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="9d301-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="9d301-109">D’autres champs de longueur variable sont retournés en tant que pointeur **null** pour le cas dans lequel la chaîne ne tient pas.</span><span class="sxs-lookup"><span data-stu-id="9d301-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




