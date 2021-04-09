---
description: Composants SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Composants SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034083"
---
# <a name="sid-components"></a><span data-ttu-id="3227c-103">Composants SID</span><span class="sxs-lookup"><span data-stu-id="3227c-103">SID Components</span></span>

<span data-ttu-id="3227c-104">Une valeur SID comprend des composants qui fournissent des informations sur la structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) et les composants qui identifient de manière unique un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="3227c-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="3227c-105">Un SID est constitué des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="3227c-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="3227c-106">Niveau de révision de la structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)</span><span class="sxs-lookup"><span data-stu-id="3227c-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="3227c-107">Valeur d’autorité d’identificateur 48 bits qui identifie l’autorité qui a émis le SID</span><span class="sxs-lookup"><span data-stu-id="3227c-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="3227c-108">Nombre variable de valeurs de sous-autorité ou d' [*identificateur relatif*](/windows/desktop/SecGloss/r-gly) (RID) qui identifient de façon unique le tiers de confiance par rapport à l’autorité qui a émis le SID</span><span class="sxs-lookup"><span data-stu-id="3227c-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="3227c-109">La combinaison de la valeur de l’autorité de l’identificateur et des valeurs de la sous-autorité garantit que deux sid ne sont pas les mêmes, même si deux autorités d’émission de SID différentes émettent la même combinaison de valeurs RID.</span><span class="sxs-lookup"><span data-stu-id="3227c-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="3227c-110">Chaque autorité émettrice de SID émet un RID donné une seule fois.</span><span class="sxs-lookup"><span data-stu-id="3227c-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="3227c-111">Les SID sont stockés au format binaire dans une structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) .</span><span class="sxs-lookup"><span data-stu-id="3227c-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="3227c-112">Pour afficher un SID, vous pouvez appeler la fonction [**ConvertSidToStringSid a**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) pour convertir un SID binaire en format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="3227c-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="3227c-113">Pour convertir une chaîne SID en un SID fonctionnel valide, appelez la fonction [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .</span><span class="sxs-lookup"><span data-stu-id="3227c-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="3227c-114">Ces fonctions utilisent la notation de chaîne standardisée suivante pour les SID, ce qui simplifie la visualisation de leurs composants :</span><span class="sxs-lookup"><span data-stu-id="3227c-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="3227c-115">s-*R* - *I* - *s*...</span><span class="sxs-lookup"><span data-stu-id="3227c-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="3227c-116">Dans cette notation, le caractère littéral « S » identifie la série de chiffres comme un SID, *R* est le niveau de révision, *I* est l’identificateur-valeur de l’autorité et *S*...</span><span class="sxs-lookup"><span data-stu-id="3227c-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="3227c-117">est une ou plusieurs valeurs de sous-autorité.</span><span class="sxs-lookup"><span data-stu-id="3227c-117">is one or more subauthority values.</span></span>

<span data-ttu-id="3227c-118">L’exemple suivant utilise cette notation pour afficher le SID relatif au domaine connu du groupe Administrateurs local :</span><span class="sxs-lookup"><span data-stu-id="3227c-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="3227c-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="3227c-119">S-1-5-32-544</span></span>

<span data-ttu-id="3227c-120">Dans cet exemple, le SID possède les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="3227c-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="3227c-121">Les constantes entre parenthèses sont une autorité d’identificateur connue et des valeurs [*RID*](/windows/desktop/SecGloss/r-gly) définies dans Winnt. h :</span><span class="sxs-lookup"><span data-stu-id="3227c-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="3227c-122">Un niveau de révision de 1</span><span class="sxs-lookup"><span data-stu-id="3227c-122">A revision level of 1</span></span>
-   <span data-ttu-id="3227c-123">Valeur d’autorité d’identificateur 5 (autorité de sécurité \_ NT \_ )</span><span class="sxs-lookup"><span data-stu-id="3227c-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="3227c-124">La première valeur de sous-autorité 32 ( \_ sécurité \_ BuiltIn \_ RID)</span><span class="sxs-lookup"><span data-stu-id="3227c-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="3227c-125">Une deuxième valeur de sous-autorité de 544 ( \_ administrateurs RID d’alias de domaine \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="3227c-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
