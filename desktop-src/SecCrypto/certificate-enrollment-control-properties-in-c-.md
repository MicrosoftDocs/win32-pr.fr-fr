---
description: Retourne un HRESULT. Dans ce HRESULT, la valeur S \_ OK indique que la méthode a été correctement exécutée.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propriétés du contrôle d’inscription de certificat en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771918"
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



 

 



