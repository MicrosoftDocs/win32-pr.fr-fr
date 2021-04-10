---
title: Obtention d’une identité d’encodage
description: Une application qui décode des données encodées peut obtenir l’identité de la routine utilisée pour encoder les données, avant d’appeler une routine pour la décoder. La routine MesInqProcEncodingId fournit cette identité.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Appel de procédure distante RPC, tâches, obtention de l’identité d’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674914"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="42e38-105">Obtention d’une identité d’encodage</span><span class="sxs-lookup"><span data-stu-id="42e38-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="42e38-106">Une application qui décode des données encodées peut obtenir l’identité de la routine utilisée pour encoder les données, avant d’appeler une routine pour la décoder.</span><span class="sxs-lookup"><span data-stu-id="42e38-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="42e38-107">La routine [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fournit cette identité.</span><span class="sxs-lookup"><span data-stu-id="42e38-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="42e38-108">Chaque procédure dans une interface est assignée à un numéro d’identification entier, appelé *identificateur de procédure* ou *ID de processus*, par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="42e38-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="42e38-109">La numérotation commence par zéro.</span><span class="sxs-lookup"><span data-stu-id="42e38-109">Numbering begins with zero.</span></span> <span data-ttu-id="42e38-110">Les bibliothèques Runtime RPC ne sont pas impliquées dans la conversion de l’ID de procédure en appel de procédure réel.</span><span class="sxs-lookup"><span data-stu-id="42e38-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="42e38-111">Dans le cas d’un ID de procédure donné, votre application doit fournir un moyen d’appeler la procédure appropriée.</span><span class="sxs-lookup"><span data-stu-id="42e38-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="42e38-112">En règle générale, les développeurs d’applications utilisent une série d’instructions **If** , ou (lors de l’utilisation de C/C++) une instruction **switch** à cet effet.</span><span class="sxs-lookup"><span data-stu-id="42e38-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




