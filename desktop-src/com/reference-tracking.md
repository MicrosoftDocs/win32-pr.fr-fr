---
title: Suivi des références
description: Suivi des références
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463742"
---
# <a name="reference-tracking"></a><span data-ttu-id="8f35e-103">Suivi des références</span><span class="sxs-lookup"><span data-stu-id="8f35e-103">Reference Tracking</span></span>

<span data-ttu-id="8f35e-104">Le suivi de référence peut empêcher la version antérieure involontaire ou malveillante d’objets.</span><span class="sxs-lookup"><span data-stu-id="8f35e-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="8f35e-105">Lorsque vous activez le suivi des références, vous demandez que les appels de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribués soient authentifiés par com.</span><span class="sxs-lookup"><span data-stu-id="8f35e-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="8f35e-106">Lorsque le suivi de référence est activé, COM effectue le suivi du nombre de références par utilisateur afin qu’un utilisateur puisse appeler **Release** uniquement sur les objets sur lesquels l’utilisateur a précédemment appelé **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="8f35e-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="8f35e-107">Bien que le suivi de référence puisse réduire les performances, il garantit que, quel que soit le nombre de fois où un utilisateur donné appelle **Release**, les objets et les stubs existent toujours si une autre personne y fait référence.</span><span class="sxs-lookup"><span data-stu-id="8f35e-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="8f35e-108">Le client peut définir le suivi de référence pour un processus en passant l' \_ indicateur de fonctionnalité EOAC Secure \_ REFS dans un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="8f35e-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="8f35e-109">Vous pouvez également activer ou désactiver le suivi des références pour toutes les applications sur un ordinateur à l’aide de Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="8f35e-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="8f35e-110">Si le suivi de référence est activé, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) utilise toujours les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f35e-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="8f35e-111">Dans ce cas, les appels à [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) sur **IUnknown** échouent.</span><span class="sxs-lookup"><span data-stu-id="8f35e-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 