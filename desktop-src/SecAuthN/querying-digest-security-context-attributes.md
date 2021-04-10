---
description: La fonction QueryContextAttributes (Digest) fournit des informations sur les paramètres actuels d’un contexte de sécurité.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Interrogation des attributs de contexte de sécurité Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951892"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="9faaf-103">Interrogation des attributs de contexte de sécurité Digest</span><span class="sxs-lookup"><span data-stu-id="9faaf-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="9faaf-104">La fonction [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fournit des informations sur les paramètres actuels d’un [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9faaf-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="9faaf-105">Microsoft Digest prend en charge l’interrogation des attributs de contexte de sécurité suivants.</span><span class="sxs-lookup"><span data-stu-id="9faaf-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="9faaf-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="9faaf-106">Attribute</span></span>                   | <span data-ttu-id="9faaf-107">Description</span><span class="sxs-lookup"><span data-stu-id="9faaf-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9faaf-108">informations de clé d’SECPKG \_ attr \_ \_</span><span class="sxs-lookup"><span data-stu-id="9faaf-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="9faaf-109">Informations relatives aux algorithmes de signature et de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="9faaf-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="9faaf-110">\_ \_ informations sur le package attr SECPKG \_</span><span class="sxs-lookup"><span data-stu-id="9faaf-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="9faaf-111">Informations générales relatives à Microsoft Digest, telles que la taille de jeton maximale autorisée par le [*package de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9faaf-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="9faaf-112">\_tailles d’attr SECPKG \_</span><span class="sxs-lookup"><span data-stu-id="9faaf-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="9faaf-113">Tailles maximales autorisées pour les données liées aux messages telles que les signatures.</span><span class="sxs-lookup"><span data-stu-id="9faaf-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
