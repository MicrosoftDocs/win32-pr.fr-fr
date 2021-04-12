---
title: Fonctions de l’API de stockage structuré
description: Certaines des fonctions d’API pour le stockage structuré sont des fonctions d’assistance qui exécutent une séquence d’appels à d’autres fonctions d’API et méthodes d’interface. Vous pouvez utiliser ces fonctions d’assistance comme raccourcis.
ms.assetid: 99ac66bc-db73-4811-9a39-fc49bb90ada8
keywords:
- Stockage structuré Strctd STG, notions de base, fonctions d’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df87e8c5910c6da23ca518d05541a69e7070f8bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309421"
---
# <a name="structured-storage-api-functions"></a><span data-ttu-id="037ca-105">Fonctions de l’API de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="037ca-105">Structured Storage API Functions</span></span>

<span data-ttu-id="037ca-106">Certaines des fonctions d’API pour le stockage structuré sont des fonctions d’assistance qui exécutent une séquence d’appels à d’autres fonctions d’API et méthodes d’interface.</span><span class="sxs-lookup"><span data-stu-id="037ca-106">Some of the API functions for structured storage are helper functions that perform a sequence of calls to other API functions and interface methods.</span></span> <span data-ttu-id="037ca-107">Vous pouvez utiliser ces fonctions d’assistance comme raccourcis.</span><span class="sxs-lookup"><span data-stu-id="037ca-107">You can use these helper functions as short cuts.</span></span>

<span data-ttu-id="037ca-108">D’autres fonctions API permettent d’accéder à l’implémentation COM du stockage structuré, des fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="037ca-108">Other API functions provide access to COM's implementation of structured storage, Compound Files.</span></span>

<span data-ttu-id="037ca-109">Toutefois, un autre ensemble de fonctions d’API vous permet de convertir des objets OLE 1 en stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="037ca-109">Still another set of API functions enable you to convert OLE 1 objects to structured storage.</span></span> <span data-ttu-id="037ca-110">Vous pouvez utiliser ces fonctions pour déterminer si une classe d’objet provient d’OLE 1 et pour convertir des objets entre des formats OLE 1 et de stockage COM actuel.</span><span class="sxs-lookup"><span data-stu-id="037ca-110">You can use these functions to determine whether an object class is from OLE 1 and to convert objects between OLE 1 and current COM storage formats.</span></span>

<span data-ttu-id="037ca-111">Enfin, il existe des fonctions d’API pour la conversion et l’émulation d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="037ca-111">Finally, there are API functions for converting and emulating other objects.</span></span> <span data-ttu-id="037ca-112">Ces fonctions fournissent des services permettant à une application serveur de travailler avec des données provenant d’une autre application.</span><span class="sxs-lookup"><span data-stu-id="037ca-112">These functions provide services for one server application to work with data from another application.</span></span> <span data-ttu-id="037ca-113">Les données peuvent être converties au format natif de l’application serveur en lisant les données à partir de leur format d’origine, mais en les écrivant dans le format natif de l’application objet.</span><span class="sxs-lookup"><span data-stu-id="037ca-113">The data can be converted to the native format of the server application by reading the data from its original format but writing it in the native format of the object application.</span></span> <span data-ttu-id="037ca-114">Ou bien, les données peuvent rester dans leur format d’origine, tandis que l’application serveur lit et écrit les données dans leur format d’origine.</span><span class="sxs-lookup"><span data-stu-id="037ca-114">Or the data can remain in its original format while the server application both reads and writes the data in its original format.</span></span>

<span data-ttu-id="037ca-115">Pour plus d’informations, consultez la section ci-dessous [modes d’accès structurés au stockage](structured-storage-access-modes.md).</span><span class="sxs-lookup"><span data-stu-id="037ca-115">For more information, see the following section [Structured Storage Access Modes](structured-storage-access-modes.md).</span></span>

 

 




