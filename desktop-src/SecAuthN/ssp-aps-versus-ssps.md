---
description: Explique les différences entre les fournisseurs de services partagés/APs et les SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs et SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952633"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="76838-103">SSP/APs et SSP</span><span class="sxs-lookup"><span data-stu-id="76838-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="76838-104">Les [*packages de sécurité*](../secgloss/s-gly.md) sont déployés dans l’un des types de bibliothèques de liens dynamiques (dll) suivants :</span><span class="sxs-lookup"><span data-stu-id="76838-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="76838-105">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="76838-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="76838-106">SSP</span><span class="sxs-lookup"><span data-stu-id="76838-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="76838-107">Le fait qu’un package de sécurité se trouve dans un [*package d’authentification*](../secgloss/a-gly.md) /fournisseur de support de sécurité (SSP/AP) ou une dll SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) est déterminé par les types de services de sécurité qu’il fournit et dans quelle mesure il doit être intégré à l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA).</span><span class="sxs-lookup"><span data-stu-id="76838-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="76838-108">Ces différences déterminent également l’API implémentée dans un package de sécurité personnalisé.</span><span class="sxs-lookup"><span data-stu-id="76838-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="76838-109">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="76838-109">SSP/APs</span></span>

<span data-ttu-id="76838-110">Un fournisseur de services partagés/AP est une DLL qui contient un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md) et peut fonctionner en tant que fournisseur de services partagés pour les applications client/serveur et comme [package d’authentification](authentication-packages.md) pour les applications d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="76838-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="76838-111">Pour fonctionner dans ces deux rôles, les services SSP/APs sont chargés dans l’espace de processus LSA au démarrage du système et peuvent également être chargés dans des processus d’application client/serveur.</span><span class="sxs-lookup"><span data-stu-id="76838-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="76838-112">Les packages de sécurité SSP/AP personnalisés doivent implémenter les [fonctions implémentées par le SSP/APS en mode utilisateur](authentication-functions.md)et les [fonctions implémentées par SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="76838-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="76838-113">Ces implémentations de fonction peuvent utiliser les fonctions de prise en charge LSA pour offrir des fonctionnalités de sécurité avancées telles que la création de jetons, la prise en charge des [*informations d’identification supplémentaires*](../secgloss/s-gly.md) et l’authentification directe.</span><span class="sxs-lookup"><span data-stu-id="76838-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="76838-114">Si un package de sécurité SSP/AP personnalisé fournit la gamme complète des fonctions d' [*intégrité*](../secgloss/i-gly.md) et de confidentialité des messages, il implémente également les [fonctions implémentées par le SSP/APS en mode utilisateur](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="76838-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="76838-115">SSP</span><span class="sxs-lookup"><span data-stu-id="76838-115">SSPs</span></span>

<span data-ttu-id="76838-116">Un SSP est une DLL qui contient un ou plusieurs packages de sécurité fournissant une connexion authentifiée, une intégrité de message et des services de chiffrement de message aux applications client/serveur.</span><span class="sxs-lookup"><span data-stu-id="76838-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="76838-117">Les SSP implémentent des fonctions SSPI ( [Security Support Provider Interface](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="76838-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="76838-118">Les applications peuvent accéder aux packages de sécurité dans un SSP en appelant directement les fonctions SSPI.</span><span class="sxs-lookup"><span data-stu-id="76838-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="76838-119">Les SSP sont chargés dans les processus client et serveur. ils ne sont pas intégrés à l’autorité LSA.</span><span class="sxs-lookup"><span data-stu-id="76838-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
