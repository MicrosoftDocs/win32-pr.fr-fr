---
description: Les services de certificats prennent en charge les hiérarchies d’autorité de certification.
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hiérarchies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522144"
---
# <a name="hierarchies"></a><span data-ttu-id="53a55-103">Hiérarchies</span><span class="sxs-lookup"><span data-stu-id="53a55-103">Hierarchies</span></span>

<span data-ttu-id="53a55-104">Les services de certificats prennent en charge les hiérarchies d' [*autorité de certification*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="53a55-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="53a55-105">Une [*hiérarchie d’autorité de certification*](../secgloss/c-gly.md) se compose d’une autorité de certification de niveau supérieur (appelée autorité de certification racine) avec une ou plusieurs autorités de certification secondaires pour lesquelles des certificats ont été émis par l’autorité de certification racine.</span><span class="sxs-lookup"><span data-stu-id="53a55-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="53a55-106">Un scénario de hiérarchie d’autorité de certification possible se trouve dans une organisation avec une autorité de certification racine, qui a été utilisée pour émettre des certificats pour plusieurs autorités de certification secondaires.</span><span class="sxs-lookup"><span data-stu-id="53a55-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="53a55-107">Les autorités de certification secondaires peuvent ensuite émettre des certificats d’entité finale, tels que des certificats émis pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53a55-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="53a55-108">Le certificat de l’utilisateur contient un chemin d’approbation pour la hiérarchie d’autorité de certification, dans ce cas, y compris le certificat pour l’autorité de certification secondaire émettrice, ainsi que pour l’autorité de certification racine.</span><span class="sxs-lookup"><span data-stu-id="53a55-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
