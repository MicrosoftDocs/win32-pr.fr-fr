---
description: Certains packages de sécurité prennent en charge des messages d’erreur étendus qui permettent aux côtés d’un lien de communication de communiquer toute raison de défaillance.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informations d’erreur étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542949"
---
# <a name="extended-error-information"></a><span data-ttu-id="e7d50-103">Informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="e7d50-103">Extended Error Information</span></span>

<span data-ttu-id="e7d50-104">Certains [*packages de sécurité*](/windows/desktop/SecGloss/s-gly) prennent en charge des messages d’erreur étendus qui permettent aux côtés d’un lien de communication de communiquer toute raison de défaillance.</span><span class="sxs-lookup"><span data-stu-id="e7d50-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="e7d50-105">Par exemple, le [*protocole Kerberos*](/windows/desktop/SecGloss/k-gly) peut échouer en raison d’une différence de temps entre l’heure de la demande d’un ticket Kerberos et le moment où le ticket a été émis.</span><span class="sxs-lookup"><span data-stu-id="e7d50-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="e7d50-106">Avec les informations des informations d’erreur étendues retournées, un client peut resynchroniser son horloge et générer un nouveau message de connexion.</span><span class="sxs-lookup"><span data-stu-id="e7d50-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="e7d50-107">Un package de sécurité définissant l’indicateur d' \_ \_ erreur étendue SECPKG \_ dans le membre **FCapabilities** d’une structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indique que le package de sécurité prend en charge les messages d’erreur étendus.</span><span class="sxs-lookup"><span data-stu-id="e7d50-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="e7d50-108">Les applications clientes qui requièrent des messages d’erreur étendus spécifient l' \_ indicateur d’erreur étendu d’ISC req \_ \_ lors de l’appel de la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="e7d50-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="e7d50-109">Les applications serveur qui requièrent des messages d’erreur étendus définissent l' \_ \_ indicateur d’erreur étendue ASC req \_ lors de l’appel [**de AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="e7d50-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
