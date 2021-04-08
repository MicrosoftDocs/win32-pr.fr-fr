---
description: Fournit des informations spécifiques à Schannel sur un contexte de sécurité.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Interrogation des attributs d’un contexte Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112167"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a><span data-ttu-id="2b834-103">Interrogation des attributs d’un contexte Schannel</span><span class="sxs-lookup"><span data-stu-id="2b834-103">Querying the Attributes of an Schannel Context</span></span>

<span data-ttu-id="2b834-104">La fonction [**QueryContextAttributes (SChannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fournit des informations spécifiques à Schannel sur un [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b834-104">The [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) function provides Schannel-specific information about a [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="2b834-105">La plupart des informations sont spécifiées à l’origine lors de la création du contexte à l’aide de la fonction client [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou Server [**AcceptSecurityContext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="2b834-105">Most of the information is originally specified when the context is created by using the client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) or server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="2b834-106">Certaines informations sont spécifiées lors de l’obtention d’un descripteur des informations d’identification utilisées pour créer le contexte.</span><span class="sxs-lookup"><span data-stu-id="2b834-106">Some information is specified when obtaining a handle to the credential used to create the context.</span></span> <span data-ttu-id="2b834-107">Pour plus d’informations, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="2b834-107">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
