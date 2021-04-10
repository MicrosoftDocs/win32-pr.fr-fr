---
title: Support In-Process
description: L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309514"
---
# <a name="in-process-support"></a><span data-ttu-id="f0b43-103">Support In-Process</span><span class="sxs-lookup"><span data-stu-id="f0b43-103">In-Process Support</span></span>

<span data-ttu-id="f0b43-104">L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f0b43-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="f0b43-105">Il n’est pas possible pour un processus d’annoter les éléments d’interface utilisateur d’un autre processus.</span><span class="sxs-lookup"><span data-stu-id="f0b43-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="f0b43-106">Notez que cela affecte uniquement l’acte de définition d’une annotation. Il n’interfère pas avec la capacité des clients à accéder aux propriétés (annotées ou autres) des éléments d’interface utilisateur dans d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="f0b43-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




