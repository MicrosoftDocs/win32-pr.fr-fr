---
description: Retourne un HRESULT. Dans ce HRESULT, la valeur S \_ OK indique que la méthode a été correctement exécutée.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propriétés du contrôle d’inscription de certificat en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416497"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Propriétés du contrôle d’inscription de certificat en C++

Lorsque vous définissez ou récupérez une propriété de contrôle d’inscription de certificat en C++, l’appel de méthode retourne un **HRESULT**. Dans ce **HRESULT**, la valeur S \_ OK indique que la méthode a été correctement exécutée.

Les programmes écrits en C++ peuvent récupérer les propriétés du contrôle d’inscription de certificat par appels de méthode sous la forme suivante.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Où *PropertyName* spécifie le nom de la propriété faisant l’objet d’un accès, et *pPropValue* est un pointeur vers une variable du type de données approprié. Une fois l’exécution de cet appel de méthode terminée, *pPropValue* pointe vers la variable qui contient la valeur de la propriété *PropertyName* .

Par exemple, pour récupérer la valeur de la propriété **RootStoreType** , utilisez le code suivant.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



Les programmes écrits en C++ peuvent définir les propriétés du contrôle d’inscription de certificat en appelant des méthodes sous la forme suivante.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Où *PropertyName* spécifie le nom de la propriété faisant l’objet d’un accès, et *PropValue* est une valeur du type de données approprié. Une fois l’exécution de cet appel de méthode terminée, la nouvelle valeur de la propriété *PropertyName* sera *PropValue*.

Par exemple, pour définir la valeur de la propriété pour **RootStoreType**, vous pouvez utiliser le code suivant.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



