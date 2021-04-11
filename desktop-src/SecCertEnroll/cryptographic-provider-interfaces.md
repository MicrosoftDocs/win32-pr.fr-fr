---
description: Les interfaces suivantes peuvent être utilisées pour récupérer des informations sur les fournisseurs de chiffrement.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfaces du fournisseur de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113771"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="d3fd2-103">Interfaces du fournisseur de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="d3fd2-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="d3fd2-104">Les interfaces suivantes peuvent être utilisées pour récupérer des informations sur les fournisseurs de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3fd2-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="d3fd2-105">Interface</span><span class="sxs-lookup"><span data-stu-id="d3fd2-105">Interface</span></span>                                    | <span data-ttu-id="d3fd2-106">Description</span><span class="sxs-lookup"><span data-stu-id="d3fd2-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="d3fd2-107">**ICspAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="d3fd2-108">Représente un algorithme implémenté par un fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3fd2-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="d3fd2-109">**ICspAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="d3fd2-110">Gère une collection d’objets [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="d3fd2-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="d3fd2-111">**ICspInformation**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="d3fd2-112">Donne accès à des informations générales sur un fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3fd2-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="d3fd2-113">**ICspInformations**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="d3fd2-114">Gère une collection d’objets [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .</span><span class="sxs-lookup"><span data-stu-id="d3fd2-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="d3fd2-115">**ICspStatus**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="d3fd2-116">Contient des informations sur une paire fournisseur/algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3fd2-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="d3fd2-117">**ICspStatuses**</span><span class="sxs-lookup"><span data-stu-id="d3fd2-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="d3fd2-118">Gère une collection d’objets [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .</span><span class="sxs-lookup"><span data-stu-id="d3fd2-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="d3fd2-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3fd2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fd2-120">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="d3fd2-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



