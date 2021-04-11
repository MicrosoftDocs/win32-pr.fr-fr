---
title: Format du pilote installable
description: Format du pilote installable
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- pilotes installables, formats
- pilotes installables, fonction DriverProc
- pilotes installables, messages
- messages du pilote
- formats de pilote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314957"
---
# <a name="installable-driver-format"></a><span data-ttu-id="92f9a-108">Format du pilote installable</span><span class="sxs-lookup"><span data-stu-id="92f9a-108">Installable Driver Format</span></span>

<span data-ttu-id="92f9a-109">Chaque pilote installable exporte une fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) .</span><span class="sxs-lookup"><span data-stu-id="92f9a-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="92f9a-110">Cette fonction de point d’entrée courante reçoit des *messages de pilote* du système qui indiquent au pilote d’effectuer des actions ou de fournir des informations.</span><span class="sxs-lookup"><span data-stu-id="92f9a-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="92f9a-111">Le système envoie des messages de pilote à la fonction **DriverProc** lorsqu’une application ou une dll ouvre ou ferme le pilote ou demande qu’un message soit envoyé au pilote.</span><span class="sxs-lookup"><span data-stu-id="92f9a-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="92f9a-112">La fonction **DriverProc** traite le message ou le transmet au gestionnaire de messages par défaut, à savoir la fonction [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="92f9a-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="92f9a-113">Dans les deux cas, **DriverProc** doit retourner une valeur indiquant si l’action demandée a réussi.</span><span class="sxs-lookup"><span data-stu-id="92f9a-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 