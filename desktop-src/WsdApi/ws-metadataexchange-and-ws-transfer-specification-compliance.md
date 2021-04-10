---
description: Avant le 2006 août, WS-MetadataExchange défini sa propre méthode d’échange de métadonnées, utilisée par le profil de périphériques pour les services Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Conformité à la spécification WS-MetadataExchange et WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114839"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="2a5e1-103">Conformité à la spécification WS-MetadataExchange et WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="2a5e1-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="2a5e1-104">Avant le 2006 août, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) définissait [sa propre méthode](get--metadata-exchange--http-request-and-message.md) d’échange de métadonnées, qui était utilisée par le [profil de périphériques pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="2a5e1-105">La version 1,1 de la spécification de WS-MetadataExchange a remplacé cette méthode par la méthode d’extraction définie dans la spécification WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="2a5e1-106">Dans le modèle actuel, WS-Transfer fournit la méthode d' [extraction](get--metadata-exchange--http-request-and-message.md) et ne fait pas référence au type du corps.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="2a5e1-107">WS-MetadataExchange décrit le format du corps et un mécanisme pour l’empaquetage de plusieurs éléments de métadonnées dans une réponse unique, et DPWS décrit des éléments de métadonnées spécifiques qu’un service doit inclure dans une réponse de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="2a5e1-108">WSDAPI ne prend pas entièrement en charge la spécification WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="2a5e1-109">Étant donné que seule la méthode d' [extraction](get--metadata-exchange--http-request-and-message.md) est requise pour les appareils, aucune autre partie de WS-Transfer n’a été implémentée.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="2a5e1-110">En outre, WSDAPI n’implémente pas la méthode GetMetadata facultative décrite dans WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



