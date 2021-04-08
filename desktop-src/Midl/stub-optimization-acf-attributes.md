---
title: Attributs ACF d’optimisation du stub
description: Ces attributs vous permettent d’optimiser la taille et la vitesse de votre code stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL, attributs, stub-optimisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839766"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="16eab-104">Attributs ACF d’optimisation du stub</span><span class="sxs-lookup"><span data-stu-id="16eab-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="16eab-105">Ces attributs vous permettent d’optimiser la taille et la vitesse de votre code stub.</span><span class="sxs-lookup"><span data-stu-id="16eab-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="16eab-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="16eab-106">Attribute</span></span>                                    | <span data-ttu-id="16eab-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="16eab-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16eab-108">[**code d’erreur**](code.md)[](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="16eab-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="16eab-109">Utilisez les attributs [**code**](code.md) et [**nocode**](nocode.md) conjointement pour éviter de générer du code stub pour les fonctions inutilisées.</span><span class="sxs-lookup"><span data-stu-id="16eab-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="16eab-110">Appliquez l’attribut **nocode** à l’en-tête d’interface et appliquez l’attribut **code** aux procédures que l’application cliente implémentera.</span><span class="sxs-lookup"><span data-stu-id="16eab-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="16eab-111">Le code stub client est généré uniquement pour les procédures sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="16eab-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="16eab-112">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="16eab-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="16eab-113">Vous permet d’affiner le niveau d’optimisation effectué par le compilateur MIDL lors de la génération de code stub, en spécifiant que les données doivent être marshalées soit par la méthode en mode mixte, soit par la méthode interprétée.</span><span class="sxs-lookup"><span data-stu-id="16eab-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="16eab-114">Vous pouvez appliquer l’attribut [**optimize**](optimize.md) à une interface ou à des fonctions sélectionnées dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="16eab-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="16eab-115">Dans les deux cas, son utilisation remplace les optimisations de ligne de commande et les valeurs par défaut préexistantes.</span><span class="sxs-lookup"><span data-stu-id="16eab-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




