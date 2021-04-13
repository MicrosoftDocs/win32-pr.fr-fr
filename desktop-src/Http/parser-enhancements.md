---
title: Améliorations de l’analyseur
description: Améliorations de l’analyseur
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Améliorations de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380125"
---
# <a name="parser-enhancements"></a><span data-ttu-id="b324d-104">Améliorations de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="b324d-104">Parser Enhancements</span></span>

<span data-ttu-id="b324d-105">Dans Windows Server 2003 avec Service Pack 1 (SP1), l’API du serveur HTTP autorise les requêtes suivantes des clients HTTP.</span><span class="sxs-lookup"><span data-stu-id="b324d-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="b324d-106">Demandes qui utilisent un saut de ligne (LF) comme marque de fin de ligne.</span><span class="sxs-lookup"><span data-stu-id="b324d-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="b324d-107">Les demandes qui contiennent des espaces linéaires (LWS) entre la ligne de requête HTTP et le début des en-têtes.</span><span class="sxs-lookup"><span data-stu-id="b324d-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="b324d-108">Ces comportements sont activés par défaut et ne sont pas contrôlés par les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="b324d-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




