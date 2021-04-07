---
title: Récupération de l’attribut objectClass
description: L’attribut objectClass contient la classe dont l’objet est une instance, ainsi que toutes les classes à partir desquelles cette classe est dérivée.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f237efff1e13c7f3498a51f38588c9885fbab76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671242"
---
# <a name="retrieving-the-objectclass-attribute"></a>Récupération de l’attribut objectClass

L’attribut **objectClass** contient la classe dont l’objet est une instance, ainsi que toutes les classes à partir desquelles cette classe est dérivée. Par exemple, la classe **utilisateur** hérite de **Top**, **Person** et **organizationalPerson**; par conséquent, l’attribut **objectClass** contient les noms de ces classes, ainsi que l’utilisateur. Alors, comment déterminer quelle classe l’objet est une instance ? L’attribut **objectClass** est le seul attribut avec plusieurs valeurs qui ont des valeurs ordonnées. La première valeur est le haut de la hiérarchie de classes, qui est la classe supérieure, et la dernière valeur est la classe la plus dérivée, qui est la classe dont l’objet est une instance.

La fonction suivante accepte un pointeur vers une colonne contenant un attribut **objectClass** et retourne l' **objectClass** instancié de l’objet.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




