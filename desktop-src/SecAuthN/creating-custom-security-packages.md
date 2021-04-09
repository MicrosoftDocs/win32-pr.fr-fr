---
description: Explique comment créer un package de sécurité personnalisé.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Création de packages de sécurité personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866017"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="fd0d5-103">Création de packages de sécurité personnalisés</span><span class="sxs-lookup"><span data-stu-id="fd0d5-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="fd0d5-104">Packages de sécurité SSP</span><span class="sxs-lookup"><span data-stu-id="fd0d5-104">SSP Security Packages</span></span>

<span data-ttu-id="fd0d5-105">Si un package de sécurité SSP (Security Support Provider) personnalisé est utilisé exclusivement pour la prise en charge de la sécurité client/serveur, il peut implémenter l' [interface du fournisseur de support de sécurité](sspi.md)Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="fd0d5-106">L’exemple SampSSP fourni avec le kit de développement logiciel (SDK) de plateforme contient un exemple d’implémentation de package de sécurité SSP.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="fd0d5-107">Packages de sécurité SSP/AP</span><span class="sxs-lookup"><span data-stu-id="fd0d5-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="fd0d5-108">Les [](/windows/desktop/SecGloss/s-gly) / [*packages d’authentification*](/windows/desktop/SecGloss/a-gly) du fournisseur de support de sécurité personnalisés (SSP/APS) contiennent des packages de sécurité qui fonctionnent comme des packages d’authentification (APS) et des fournisseurs de support de sécurité (SSP).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="fd0d5-109">Ces packages implémentent des API distinctes pour prendre en charge chaque rôle.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="fd0d5-110">Étant donné qu’il fonctionne comme un point d’accès, un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) SSP/AP personnalisé doit fournir des implémentations pour toutes les [fonctions implémentées par les packages d’authentification](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="fd0d5-111">Pour assurer la prise en charge de la sécurité intégrée, un package de sécurité SSP/AP personnalisé doit fournir des implémentations pour les [fonctions implémentées par le fournisseur SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="fd0d5-112">Les [fonctions LSA appelées par SSP/APS](authentication-functions.md) décrivent les fonctions de prise en charge disponibles pour les développeurs SSP/AP qui souhaitent interagir avec l’autorité LSA.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="fd0d5-113">Les packages de sécurité SSP/AP, afin d’être exécutés à la fois comme un point d’accès et un SSP, peuvent s’exécuter dans le cadre du système d’exploitation et dans le cadre d’une application utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="fd0d5-114">Ces deux modes d’exécution sont appelés le mode LSA et le mode utilisateur, respectivement.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="fd0d5-115">Pour plus d’informations sur les packages de sécurité personnalisés en mode LSA, consultez [initialisation du mode LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="fd0d5-116">Pour plus d’informations sur le mode utilisateur, consultez [initialisation du mode utilisateur](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="fd0d5-117">Si un package de sécurité SSP/AP personnalisé offre des services pour les applications client/serveur, il doit fournir des implémentations pour les fonctions décrites dans [fonctions implémentées par SSP/APS en mode utilisateur](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="fd0d5-118">Les [fonctions LSA appelées par SSP/APS en mode utilisateur](authentication-functions.md) décrivent les fonctions de prise en charge disponibles pour l’exécution d’un fournisseur SSP/AP dans un processus client ou serveur.</span><span class="sxs-lookup"><span data-stu-id="fd0d5-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="fd0d5-119">Pour plus d’informations sur l’inscription d’une DLL SSP/AP, consultez [inscription de dll SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="fd0d5-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd0d5-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd0d5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd0d5-121">Restrictions concernant l’inscription et l’installation d’un package de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd0d5-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
