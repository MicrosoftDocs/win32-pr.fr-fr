---
title: Fonctions d’acquisition de clé
description: Par défaut, le fournisseur de services partagés fournit des clés de chiffrement aux programmes serveur qui les demandent. Chaque fournisseur de services partagés implémente son propre système de génération de clés. Le format des clés générées par le fournisseur de services partagés est spécifique au fournisseur de services partagés.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840630"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="4089a-105">Fonctions d’acquisition de clé</span><span class="sxs-lookup"><span data-stu-id="4089a-105">Key Acquisition Functions</span></span>

<span data-ttu-id="4089a-106">Par défaut, le fournisseur de services partagés fournit des clés de chiffrement aux programmes serveur qui les demandent.</span><span class="sxs-lookup"><span data-stu-id="4089a-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="4089a-107">Chaque fournisseur de services partagés implémente son propre système de génération de clés.</span><span class="sxs-lookup"><span data-stu-id="4089a-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="4089a-108">Le format des clés générées par le fournisseur de services partagés est spécifique au fournisseur de services partagés.</span><span class="sxs-lookup"><span data-stu-id="4089a-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="4089a-109">RPC vous permet de remplacer la méthode par défaut de génération de clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4089a-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="4089a-110">Votre application peut appeler la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) et lui passer un pointeur vers une fonction d’acquisition de clé.</span><span class="sxs-lookup"><span data-stu-id="4089a-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="4089a-111">Vous pouvez écrire la fonction d’acquisition de clé afin qu’elle génère des clés à l’aide de n’importe quelle méthode de votre choix.</span><span class="sxs-lookup"><span data-stu-id="4089a-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="4089a-112">Toutefois, la clé qu’elle transmet au programme serveur doit correspondre au format requis par le fournisseur de services partagés.</span><span class="sxs-lookup"><span data-stu-id="4089a-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="4089a-113">La plupart des applications n’ont pas besoin d’utiliser les fonctions d’acquisition de clé et peuvent simplement fournir la **valeur null** à tous les paramètres où une fonction d’acquisition de clé est demandée.</span><span class="sxs-lookup"><span data-stu-id="4089a-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




