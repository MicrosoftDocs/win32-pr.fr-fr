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
# <a name="volume-shadow-copy-api-data-types"></a>Types de données de l’API de cliché instantané des volumes

Les types de données suivants sont définis dans l’API de cliché instantané des volumes :

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>\_ID VSS
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

La définition de l' **\_ ID VSS** spécifie le format général de l’identificateur VSS. L' **\_ ID VSS** est un type de données GUID standard.

Service **VSS \_ Les ID** s sont utilisés pour identifier les éléments suivants : clichés instantanés, jeux de clichés instantanés, fournisseurs, versions de fournisseur, enregistreurs (identificateur de classe du générateur) et instances de Writers.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

La définition **VSS \_ PWSZ** spécifie une chaîne de caractères larges se terminant par un caractère null (WCHAR).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_horodateur VSS
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

La définition d' **\_ horodatage VSS** contient les informations de datage sous la forme d’une valeur entière de 64 bits contenant le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). Cette définition est interchangeable avec la structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> </dl>

 

 
