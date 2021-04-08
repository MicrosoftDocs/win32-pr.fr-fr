---
description: 'Les types de données suivants sont définis dans l’API de cliché instantané des volumes :'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Types de données de l’API de cliché instantané des volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751581"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="a3ed0-103">Types de données de l’API de cliché instantané des volumes</span><span class="sxs-lookup"><span data-stu-id="a3ed0-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="a3ed0-104">Les types de données suivants sont définis dans l’API de cliché instantané des volumes :</span><span class="sxs-lookup"><span data-stu-id="a3ed0-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="a3ed0-105"><span id="VSS_ID"></span><span id="vss_id"></span>\_ID VSS</span><span class="sxs-lookup"><span data-stu-id="a3ed0-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="a3ed0-106">La définition de l' **\_ ID VSS** spécifie le format général de l’identificateur VSS.</span><span class="sxs-lookup"><span data-stu-id="a3ed0-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="a3ed0-107">L' **\_ ID VSS** est un type de données GUID standard.</span><span class="sxs-lookup"><span data-stu-id="a3ed0-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="a3ed0-108">Service **VSS \_ Les ID** s sont utilisés pour identifier les éléments suivants : clichés instantanés, jeux de clichés instantanés, fournisseurs, versions de fournisseur, enregistreurs (identificateur de classe du générateur) et instances de Writers.</span><span class="sxs-lookup"><span data-stu-id="a3ed0-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="a3ed0-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS</span><span class="sxs-lookup"><span data-stu-id="a3ed0-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="a3ed0-110">La définition **VSS \_ PWSZ** spécifie une chaîne de caractères larges se terminant par un caractère null (WCHAR).</span><span class="sxs-lookup"><span data-stu-id="a3ed0-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="a3ed0-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_horodateur VSS</span><span class="sxs-lookup"><span data-stu-id="a3ed0-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="a3ed0-112">La définition d' **\_ horodatage VSS** contient les informations de datage sous la forme d’une valeur entière de 64 bits contenant le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="a3ed0-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="a3ed0-113">Cette définition est interchangeable avec la structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="a3ed0-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
