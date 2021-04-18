---
description: Exemples de limitations de programme
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Exemples de limitations de programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520654"
---
# <a name="example-program-limitations"></a><span data-ttu-id="51f50-103">Exemples de limitations de programme</span><span class="sxs-lookup"><span data-stu-id="51f50-103">Example Program Limitations</span></span>

<span data-ttu-id="51f50-104">Les principes de bonnes pratiques de programmation ne sont pas toujours suivis dans ces exemples de programmes afin de fournir un code plus concis et plus lisible.</span><span class="sxs-lookup"><span data-stu-id="51f50-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="51f50-105">En particulier :</span><span class="sxs-lookup"><span data-stu-id="51f50-105">In particular:</span></span>

-   <span data-ttu-id="51f50-106">Seules les réponses d’erreur limitées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="51f50-106">Only limited error responses are shown.</span></span> <span data-ttu-id="51f50-107">Les programmes de travail doivent toujours vérifier les codes d’erreur renvoyés et effectuer les actions appropriées lorsqu’une erreur est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="51f50-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="51f50-108">Seule la gestion de la mémoire et des ressources est limitée.</span><span class="sxs-lookup"><span data-stu-id="51f50-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="51f50-109">Dans les programmes de travail, toutes les clés et tous les [*hachages*](../secgloss/h-gly.md) doivent être détruits, toute la mémoire allouée doit être libérée, tous les fichiers doivent être fermés et tous les descripteurs doivent être libérés.</span><span class="sxs-lookup"><span data-stu-id="51f50-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="51f50-110">Ces exemples de programmes fournissent uniquement des démonstrations limitées de l’utilisation des fonctions qui effectuent ces tâches.</span><span class="sxs-lookup"><span data-stu-id="51f50-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="51f50-111">Ces exemples de programmes n’effectuent aucune tâche de gestion de la mémoire ou des ressources en cas d’arrêt du programme en raison d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="51f50-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
