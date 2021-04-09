---
title: Énumération des groupes qui contiennent de nombreux membres
description: Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé member.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Énumération des groupes qui contiennent de nombreux membres Active Directory
- groupes Active Directory, énumération de groupes avec de nombreux membres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101453"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="3051e-105">Énumération des groupes qui contiennent de nombreux membres</span><span class="sxs-lookup"><span data-stu-id="3051e-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="3051e-106">Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé **member**.</span><span class="sxs-lookup"><span data-stu-id="3051e-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="3051e-107">L’attribut **member** peut contenir un grand nombre de valeurs.</span><span class="sxs-lookup"><span data-stu-id="3051e-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="3051e-108">L’énumération des membres peut être inefficace lorsque le nombre de valeurs dans un attribut à valeurs multiples devient important.</span><span class="sxs-lookup"><span data-stu-id="3051e-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="3051e-109">Le serveur limite également le nombre maximal de valeurs qui peuvent être extraites dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3051e-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="3051e-110">Cela signifie que si un groupe peut avoir plus de membres que ce qui peut être fourni par le serveur, la seule façon d’énumérer tous les membres est d’utiliser la récupération incrémentielle des données, appelée *récupération de plage*.</span><span class="sxs-lookup"><span data-stu-id="3051e-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="3051e-111">La récupération de plage implique de demander un nombre limité de valeurs d’attribut dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3051e-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="3051e-112">Le nombre de valeurs demandé doit être inférieur ou égal au nombre maximal de valeurs prises en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="3051e-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="3051e-113">Pour réduire le nombre de fois que la requête doit contacter le serveur, le nombre de valeurs demandé doit être aussi proche que possible de cette valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="3051e-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="3051e-114">Pour permettre à une application de fonctionner correctement avec tous les serveurs, vous devez utiliser un nombre maximal de 1000.</span><span class="sxs-lookup"><span data-stu-id="3051e-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="3051e-115">La version du serveur qui fournit les données demandées détermine le nombre maximal de valeurs qui peuvent être récupérées dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3051e-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="3051e-116">Le tableau suivant répertorie la version du serveur et le nombre maximal de valeurs qui peuvent être récupérées dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3051e-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="3051e-117">Version du système d’exploitation du serveur</span><span class="sxs-lookup"><span data-stu-id="3051e-117">Server operating system version</span></span> | <span data-ttu-id="3051e-118">Valeurs maximales récupérées</span><span class="sxs-lookup"><span data-stu-id="3051e-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="3051e-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3051e-119">Windows 2000</span></span>                    | <span data-ttu-id="3051e-120">1 000</span><span class="sxs-lookup"><span data-stu-id="3051e-120">1000</span></span>                     |
| <span data-ttu-id="3051e-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3051e-121">Windows Server 2003</span></span>             | <span data-ttu-id="3051e-122">1500</span><span class="sxs-lookup"><span data-stu-id="3051e-122">1500</span></span>                     |



 

<span data-ttu-id="3051e-123">Pour plus d’informations sur la récupération de plages de valeurs d’attribut avec ADSI, consultez [récupération de plage d’attributs](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="3051e-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="3051e-124">Pour plus d’informations sur la récupération de plages de valeurs d’attribut avec [System. DirectoryServices](/dotnet/api/system.directoryservices), consultez [énumération de membres dans un grand groupe](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="3051e-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 