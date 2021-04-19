---
description: ELS prend en charge les fonctions définies dans le tableau suivant.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Fonctions de services linguistiques étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541833"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="be104-103">Fonctions de services linguistiques étendues</span><span class="sxs-lookup"><span data-stu-id="be104-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="be104-104">ELS prend en charge les fonctions définies dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="be104-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="be104-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="be104-105">Function</span></span>                                                 | <span data-ttu-id="be104-106">Description</span><span class="sxs-lookup"><span data-stu-id="be104-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be104-107">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="be104-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="be104-108">Fonction de rappel définie par l’application qui traite de façon asynchrone les données produites par la fonction **MappingRecognizeText** .</span><span class="sxs-lookup"><span data-stu-id="be104-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="be104-109">**MappingDoAction**</span><span class="sxs-lookup"><span data-stu-id="be104-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="be104-110">Fait en sorte qu’un service ELS effectue une action après la reconnaissance du texte.</span><span class="sxs-lookup"><span data-stu-id="be104-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="be104-111">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="be104-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="be104-112">Libère de la mémoire et des ressources allouées pendant une opération de reconnaissance de texte ELS.</span><span class="sxs-lookup"><span data-stu-id="be104-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="be104-113">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="be104-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="be104-114">Libère de la mémoire et des ressources allouées pour que l’application interagisse avec un ou plusieurs services ELS.</span><span class="sxs-lookup"><span data-stu-id="be104-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="be104-115">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="be104-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="be104-116">Récupère la liste des services pris en charge par la plateforme ELS disponibles, ainsi que les informations associées, en fonction des critères spécifiés par l’application.</span><span class="sxs-lookup"><span data-stu-id="be104-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="be104-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="be104-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="be104-118">Appelle sur un service ELS pour reconnaître du texte.</span><span class="sxs-lookup"><span data-stu-id="be104-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



