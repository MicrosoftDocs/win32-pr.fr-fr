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
# <a name="retrieving-the-objectclass-attribute"></a><span data-ttu-id="997b1-103">Récupération de l’attribut objectClass</span><span class="sxs-lookup"><span data-stu-id="997b1-103">Retrieving the objectClass Attribute</span></span>

<span data-ttu-id="997b1-104">L’attribut **objectClass** contient la classe dont l’objet est une instance, ainsi que toutes les classes à partir desquelles cette classe est dérivée.</span><span class="sxs-lookup"><span data-stu-id="997b1-104">The **objectClass** attribute contains the class of which the object is an instance, as well as all classes from which that class is derived.</span></span> <span data-ttu-id="997b1-105">Par exemple, la classe **utilisateur** hérite de **Top**, **Person** et **organizationalPerson**; par conséquent, l’attribut **objectClass** contient les noms de ces classes, ainsi que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="997b1-105">For example, the **user** class inherits from **top**, **person**, and **organizationalPerson**; therefore, the **objectClass** attribute contains the names of those classes, as well as user.</span></span> <span data-ttu-id="997b1-106">Alors, comment déterminer quelle classe l’objet est une instance ?</span><span class="sxs-lookup"><span data-stu-id="997b1-106">So, how do you find out what class the object is an instance of?</span></span> <span data-ttu-id="997b1-107">L’attribut **objectClass** est le seul attribut avec plusieurs valeurs qui ont des valeurs ordonnées.</span><span class="sxs-lookup"><span data-stu-id="997b1-107">The **objectClass** attribute is the only attribute with multiple values that has ordered values.</span></span> <span data-ttu-id="997b1-108">La première valeur est le haut de la hiérarchie de classes, qui est la classe supérieure, et la dernière valeur est la classe la plus dérivée, qui est la classe dont l’objet est une instance.</span><span class="sxs-lookup"><span data-stu-id="997b1-108">The first value is the top of the class hierarchy, which is the top class, and the last value is the most derived class, which is the class that the object is an instance of.</span></span>

<span data-ttu-id="997b1-109">La fonction suivante accepte un pointeur vers une colonne contenant un attribut **objectClass** et retourne l' **objectClass** instancié de l’objet.</span><span class="sxs-lookup"><span data-stu-id="997b1-109">The following function takes a pointer to a column containing an **objectClass** attribute and returns the instantiated **objectClass** of the object.</span></span>


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



 

 




