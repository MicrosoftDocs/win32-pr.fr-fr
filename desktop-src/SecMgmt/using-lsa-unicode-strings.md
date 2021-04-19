---
description: Plusieurs fonctions de stratégie LSA utilisent la structure de \_ chaîne LSA Unicode \_ pour stocker les informations de chaîne. Cette structure stocke la chaîne et ses informations de longueur.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Utilisation de chaînes Unicode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515428"
---
# <a name="using-lsa-unicode-strings"></a><span data-ttu-id="0bdde-104">Utilisation de chaînes Unicode LSA</span><span class="sxs-lookup"><span data-stu-id="0bdde-104">Using LSA Unicode Strings</span></span>

<span data-ttu-id="0bdde-105">Plusieurs fonctions de stratégie LSA utilisent la structure [**de \_ \_ chaîne LSA Unicode**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) pour stocker les informations de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0bdde-105">Several of the LSA Policy functions use the [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure to store string information.</span></span> <span data-ttu-id="0bdde-106">Cette structure stocke la chaîne et ses informations de longueur.</span><span class="sxs-lookup"><span data-stu-id="0bdde-106">This structure stores the string and its length information.</span></span>

<span data-ttu-id="0bdde-107">Le code suivant implémente une fonction qui convertit les données de **LPWStr** en structures de [**\_ \_ chaînes Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) :</span><span class="sxs-lookup"><span data-stu-id="0bdde-107">The following code implements a function that converts **LPWSTR** data to [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures:</span></span>


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



