---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Microsoft Message Queuing (MSMQ)-SHA 2 est l’algorithme de hachage par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb62f55f07565e76cefb5463a095d11ae789f379
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314962"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="4d143-103">Microsoft Message Queuing (MSMQ)-SHA 2 est l’algorithme de hachage par défaut</span><span class="sxs-lookup"><span data-stu-id="4d143-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4d143-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="4d143-104">Affected Platforms</span></span>

 <span data-ttu-id="4d143-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d143-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="4d143-106">**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d143-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="4d143-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4d143-107">Feature Impact</span></span>

 <span data-ttu-id="4d143-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="4d143-108">**Severity** - Low</span></span>  
<span data-ttu-id="4d143-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="4d143-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="4d143-110">Description</span><span class="sxs-lookup"><span data-stu-id="4d143-110">Description</span></span>

<span data-ttu-id="4d143-111">Dans Windows 7, MSMQ utilise SHA-2 comme valeur par défaut lors de la signature d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="4d143-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="4d143-112">En outre, tous les messages entrants doivent être signés avec SHA-2.</span><span class="sxs-lookup"><span data-stu-id="4d143-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="4d143-113">Vous pouvez activer la prise en charge d’un algorithme de chiffrement inférieur via une clé de Registre accessible par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4d143-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4d143-114">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="4d143-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="4d143-115">MSMQ dans Windows 2003 ou versions antérieures n’acceptera pas les messages signés provenant de MSMQ dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d143-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="4d143-116">MSMQ dans Windows 7 n’accepte pas les messages signés provenant de Windows 2008 ou des versions antérieures</span><span class="sxs-lookup"><span data-stu-id="4d143-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="4d143-117">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="4d143-117">Mitigation</span></span>

<span data-ttu-id="4d143-118">Les utilisateurs doivent envisager une mise à niveau vers Windows 7 pour tirer parti de l’algorithme de signature plus fort.</span><span class="sxs-lookup"><span data-stu-id="4d143-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="4d143-119">Pour activer l’échange de messages signés de manière transparente entre Windows 7 et tout système d’exploitation de niveau supérieur, l’administrateur doit ajouter des exceptions appropriées sur les ordinateurs MSMQ.</span><span class="sxs-lookup"><span data-stu-id="4d143-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



