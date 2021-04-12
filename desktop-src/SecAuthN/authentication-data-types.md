---
description: Répertorie les types de données utilisés par les API d’authentification.
ms.assetid: 1c2f932d-11f4-406f-8874-2f247b53d70f
title: Types de données d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38873b3385817187469466bf67f350a7f0701d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319902"
---
# <a name="authentication-data-types"></a><span data-ttu-id="ba411-103">Types de données d’authentification</span><span class="sxs-lookup"><span data-stu-id="ba411-103">Authentication Data Types</span></span>

## <a name="lsa-data-types"></a><span data-ttu-id="ba411-104">Types de données LSA</span><span class="sxs-lookup"><span data-stu-id="ba411-104">LSA Data Types</span></span>

<span data-ttu-id="ba411-105">L' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) utilise le type de données suivant.</span><span class="sxs-lookup"><span data-stu-id="ba411-105">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) uses the following data type.</span></span>



| <span data-ttu-id="ba411-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="ba411-106">Data type</span></span>                                            | <span data-ttu-id="ba411-107">Description</span><span class="sxs-lookup"><span data-stu-id="ba411-107">Description</span></span>                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba411-108">**\_demande du client PLSA \_**</span><span class="sxs-lookup"><span data-stu-id="ba411-108">**PLSA\_CLIENT\_REQUEST**</span></span>](plsa-client-request.md) | <span data-ttu-id="ba411-109">Type de données opaque utilisé en interne par l’autorité de certification locale pour tenir à jour les informations du client relatives aux demandes individuelles.</span><span class="sxs-lookup"><span data-stu-id="ba411-109">An opaque data type used internally by the LSA to maintain client information related to individual requests.</span></span><br/> |



 

## <a name="sspi-data-types-and-values"></a><span data-ttu-id="ba411-110">Valeurs et types de données SSPI</span><span class="sxs-lookup"><span data-stu-id="ba411-110">SSPI Data Types and Values</span></span>

<span data-ttu-id="ba411-111">[SSPI](sspi.md) utilise les données et les types énumérés suivants.</span><span class="sxs-lookup"><span data-stu-id="ba411-111">[SSPI](sspi.md) uses the following data and enumerated types.</span></span>



| <span data-ttu-id="ba411-112">Type de données ou valeur</span><span class="sxs-lookup"><span data-stu-id="ba411-112">Data type or value</span></span>                         | <span data-ttu-id="ba411-113">Description</span><span class="sxs-lookup"><span data-stu-id="ba411-113">Description</span></span>                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="ba411-114">Handles SSPI</span><span class="sxs-lookup"><span data-stu-id="ba411-114">SSPI Handles</span></span>](sspi-handles.md)           | <span data-ttu-id="ba411-115">Les types de handles SSPI et les pointeurs vers ces handles.</span><span class="sxs-lookup"><span data-stu-id="ba411-115">SSPI handle types and pointers to these handles.</span></span><br/>                      |
| [<span data-ttu-id="ba411-116">Codes d’État SSPI</span><span class="sxs-lookup"><span data-stu-id="ba411-116">SSPI Status Codes</span></span>](sspi-status-codes.md) | <span data-ttu-id="ba411-117">Codes d’État retournés dans les applications SSPI.</span><span class="sxs-lookup"><span data-stu-id="ba411-117">Status codes returned in SSPI applications.</span></span><br/>                           |
| [<span data-ttu-id="ba411-118">Confirmé</span><span class="sxs-lookup"><span data-stu-id="ba411-118">TimeStamp</span></span>](timestamp.md)                 | <span data-ttu-id="ba411-119">Type défini pour contenir des informations sur la validité des jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ba411-119">Defined type to hold information on time validity of security tokens.</span></span><br/> |



 

 

