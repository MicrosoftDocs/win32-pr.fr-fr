---
description: Le système d’exploitation Windows prend en charge l’authentification à l’aide de packages de sécurité qui fonctionnent comme des fournisseurs de support de sécurité et comme des packages d’authentification.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Fournisseur de support de sécurité/packages d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517825"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="3387b-103">Fournisseur de support de sécurité/packages d’authentification</span><span class="sxs-lookup"><span data-stu-id="3387b-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="3387b-104">Le système d’exploitation Windows prend en charge l’authentification à l’aide de [*packages de sécurité*](../secgloss/s-gly.md) qui fonctionnent comme des fournisseurs de [*support de sécurité*](../secgloss/s-gly.md) et comme des [*packages d’authentification*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3387b-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="3387b-105">Les packages de sécurité fournissent les services de prise en charge du processus d’ouverture de session d’un package d’authentification Windows et fournissent également des services d’authentification aux applications en implémentant un ensemble de fonctions mappées à l’interface SSPI ( [Security Support Provider Interface](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="3387b-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="3387b-106">Un package de sécurité qui fonctionne comme un package d’authentification et implémente les fonctionnalités requises par l' [*interface SSPI*](../secgloss/s-gly.md) est appelé fournisseur de support de sécurité/package d’authentification (SSP/AP).</span><span class="sxs-lookup"><span data-stu-id="3387b-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="3387b-107">Pour plus d’informations sur les packages de sécurité, consultez [packages SSP fournis par Microsoft](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="3387b-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="3387b-108">Pour plus d’informations sur le développement d’un fournisseur SSP/APs personnalisé, consultez [packages de sécurité personnalisés](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="3387b-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
