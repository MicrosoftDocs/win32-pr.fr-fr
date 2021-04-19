---
description: Un contexte de sécurité est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Sémantique du contexte SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535511"
---
# <a name="sspi-context-semantics"></a><span data-ttu-id="5ae74-103">Sémantique du contexte SSPI</span><span class="sxs-lookup"><span data-stu-id="5ae74-103">SSPI Context Semantics</span></span>

<span data-ttu-id="5ae74-104">Un [*contexte de sécurité*](../secgloss/s-gly.md) est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication.</span><span class="sxs-lookup"><span data-stu-id="5ae74-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="5ae74-105">Cela comprend des informations telles que les identités du principal et des informations sur les clés, les chiffrements et les algorithmes utilisés.</span><span class="sxs-lookup"><span data-stu-id="5ae74-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="5ae74-106">Pour l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ), un contexte de sécurité est une structure opaque créée via un échange impliquant la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) et la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="5ae74-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="5ae74-107">Pour plus d’informations sur les attributs de contexte, consultez [spécifications de contexte](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ae74-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="5ae74-108">Le modèle SSPI prend en charge trois types de contextes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5ae74-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ae74-109">Type</span><span class="sxs-lookup"><span data-stu-id="5ae74-109">Type</span></span></th>
<th><span data-ttu-id="5ae74-110">Description</span><span class="sxs-lookup"><span data-stu-id="5ae74-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ae74-111"><a href="connection-oriented-contexts.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="5ae74-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="5ae74-112">Un <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> orienté connexion est le contexte de sécurité le plus courant et le plus simple à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ae74-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="5ae74-113">L’appelant est responsable du format de message global et de l’emplacement des données dans le message.</span><span class="sxs-lookup"><span data-stu-id="5ae74-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="5ae74-114">L’appelant est également responsable de l’emplacement des champs de sécurité concernés dans un message, tels que l’emplacement des données de signature.</span><span class="sxs-lookup"><span data-stu-id="5ae74-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ae74-115"><a href="datagram-contexts.md">Datagramme</a></span><span class="sxs-lookup"><span data-stu-id="5ae74-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="5ae74-116">Un contexte orienté <a href="/windows/desktop/SecGloss/d-gly"><em>datagramme</em></a>a une prise en charge supplémentaire pour la communication des datagrammes de type DCE.</span><span class="sxs-lookup"><span data-stu-id="5ae74-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="5ae74-117">Il peut également être utilisé de façon générique pour une application de transport orientée datagramme.</span><span class="sxs-lookup"><span data-stu-id="5ae74-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="5ae74-118">Le package <a href="microsoft-kerberos.md">Microsoft Kerberos</a> ne prend pas en charge les contextes de datagramme en mode utilisateur à utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ae74-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ae74-119"><a href="stream-contexts.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="5ae74-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="5ae74-120">Un contexte orienté flux est responsable du blocage et de la mise en forme des messages dans le package de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5ae74-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="5ae74-121">L’appelant ne s’intéresse pas à la mise en forme, mais plutôt à un flux de données brut.</span><span class="sxs-lookup"><span data-stu-id="5ae74-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5ae74-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ae74-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae74-123">Exigences de contexte</span><span class="sxs-lookup"><span data-stu-id="5ae74-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="5ae74-124">Contextes orientés connexion</span><span class="sxs-lookup"><span data-stu-id="5ae74-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="5ae74-125">Contextes de datagramme</span><span class="sxs-lookup"><span data-stu-id="5ae74-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="5ae74-126">Contextes de flux</span><span class="sxs-lookup"><span data-stu-id="5ae74-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
