---
title: État du canal
description: Sur le serveur, le compilateur MIDL crée une variable d’État qui coordonne les procédures push, pull et Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101945"
---
# <a name="the-pipe-state"></a><span data-ttu-id="54f3a-103">État du canal</span><span class="sxs-lookup"><span data-stu-id="54f3a-103">The Pipe State</span></span>

<span data-ttu-id="54f3a-104">Sur le serveur, le compilateur MIDL crée une variable d' *État* qui coordonne les procédures push, pull et Alloc.</span><span class="sxs-lookup"><span data-stu-id="54f3a-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="54f3a-105">Côté client, le développeur doit créer la variable d' *État* .</span><span class="sxs-lookup"><span data-stu-id="54f3a-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="54f3a-106">Par conséquent, la variable d' *État* est locale des deux côtés, c’est-à-dire que le client et le serveur conservent chacun leur propre état de canal.</span><span class="sxs-lookup"><span data-stu-id="54f3a-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="54f3a-107">Le code stub du serveur conserve la variable d’État sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="54f3a-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="54f3a-108">Vous ne devez pas essayer de modifier directement son contenu.</span><span class="sxs-lookup"><span data-stu-id="54f3a-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="54f3a-109">Le client doit initialiser les champs dans la structure de contrôle du canal et conserver sa variable d' *État* .</span><span class="sxs-lookup"><span data-stu-id="54f3a-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="54f3a-110">Elle utilise la variable d' *État* pour identifier où localiser ou placer des données.</span><span class="sxs-lookup"><span data-stu-id="54f3a-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="54f3a-111">La variable d' *État* du client peut être aussi simple qu’un descripteur de fichier, si vous transférez des données d’un fichier vers un autre.</span><span class="sxs-lookup"><span data-stu-id="54f3a-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="54f3a-112">Il peut également s’agir d’un entier qui pointe vers un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="54f3a-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="54f3a-113">Vous pouvez aussi définir une structure d’État assez complexe pour effectuer des tâches supplémentaires, telles que la coordination des routines push et pull sur un \[ paramètre [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="54f3a-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 