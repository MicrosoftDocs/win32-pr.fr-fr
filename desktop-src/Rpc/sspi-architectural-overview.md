---
title: Vue d’ensemble de l’architecture SSPI
description: SSPI est une interface logicielle.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031586"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="c54b5-103">Vue d’ensemble de l’architecture SSPI</span><span class="sxs-lookup"><span data-stu-id="c54b5-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="c54b5-104">SSPI est une interface logicielle.</span><span class="sxs-lookup"><span data-stu-id="c54b5-104">SSPI is a software interface.</span></span> <span data-ttu-id="c54b5-105">Les bibliothèques de programmation distribuées telles que RPC peuvent l’utiliser pour les communications authentifiées.</span><span class="sxs-lookup"><span data-stu-id="c54b5-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="c54b5-106">Un ou plusieurs modules logiciels fournissent les fonctionnalités d’authentification réelles.</span><span class="sxs-lookup"><span data-stu-id="c54b5-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="c54b5-107">Chaque module, appelé fournisseur SSP (Security Support Provider), est implémenté en tant que bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="c54b5-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="c54b5-108">Un SSP fournit un ou plusieurs packages de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c54b5-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="c54b5-109">De nombreux SSP et packages sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c54b5-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="c54b5-110">Windows est fourni avec le package de sécurité NTLM et le package de sécurité du protocole Microsoft Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c54b5-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="c54b5-111">En outre, vous pouvez choisir d’installer le package de sécurité SSL (Secure Socket Layer) ou tout autre fournisseur de services partagés compatible SSPI.</span><span class="sxs-lookup"><span data-stu-id="c54b5-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="c54b5-112">L’utilisation de SSPI garantit que, quel que soit le fournisseur de services partagés que vous sélectionnez, votre application accède aux fonctionnalités d’authentification de manière uniforme.</span><span class="sxs-lookup"><span data-stu-id="c54b5-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="c54b5-113">Cette fonctionnalité offre à votre application une plus grande indépendance par rapport à l’implémentation du réseau que celle qui était disponible dans le passé.</span><span class="sxs-lookup"><span data-stu-id="c54b5-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="c54b5-114">Les applications distribuées communiquent par l’intermédiaire de l’interface RPC.</span><span class="sxs-lookup"><span data-stu-id="c54b5-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="c54b5-115">Le logiciel RPC accède à son tour aux fonctionnalités d’authentification d’un fournisseur de services partagés par le biais de l’interface SSPI.</span><span class="sxs-lookup"><span data-stu-id="c54b5-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="c54b5-116">Pour plus d’informations, consultez [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="c54b5-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 