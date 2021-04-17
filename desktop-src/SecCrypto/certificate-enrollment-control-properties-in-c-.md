---
description: Retourne un HRESULT. Dans ce HRESULT, la valeur S \_ OK indique que la méthode a été correctement exécutée.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propriétés du contrôle d’inscription de certificat en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525833"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="53efc-104">Propriétés du contrôle d’inscription de certificat en C++</span><span class="sxs-lookup"><span data-stu-id="53efc-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="53efc-105">Lorsque vous définissez ou récupérez une propriété de contrôle d’inscription de certificat en C++, l’appel de méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53efc-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="53efc-106">Dans ce **HRESULT**, la valeur S \_ OK indique que la méthode a été correctement exécutée.</span><span class="sxs-lookup"><span data-stu-id="53efc-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="53efc-107">Les programmes écrits en C++ peuvent récupérer les propriétés du contrôle d’inscription de certificat par appels de méthode sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="53efc-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="53efc-108">Où *PropertyName* spécifie le nom de la propriété faisant l’objet d’un accès, et *pPropValue* est un pointeur vers une variable du type de données approprié.</span><span class="sxs-lookup"><span data-stu-id="53efc-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="53efc-109">Une fois l’exécution de cet appel de méthode terminée, *pPropValue* pointe vers la variable qui contient la valeur de la propriété *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="53efc-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="53efc-110">Par exemple, pour récupérer la valeur de la propriété **RootStoreType** , utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="53efc-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="53efc-111">Les programmes écrits en C++ peuvent définir les propriétés du contrôle d’inscription de certificat en appelant des méthodes sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="53efc-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="53efc-112">Où *PropertyName* spécifie le nom de la propriété faisant l’objet d’un accès, et *PropValue* est une valeur du type de données approprié.</span><span class="sxs-lookup"><span data-stu-id="53efc-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="53efc-113">Une fois l’exécution de cet appel de méthode terminée, la nouvelle valeur de la propriété *PropertyName* sera *PropValue*.</span><span class="sxs-lookup"><span data-stu-id="53efc-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="53efc-114">Par exemple, pour définir la valeur de la propriété pour **RootStoreType**, vous pouvez utiliser le code suivant.</span><span class="sxs-lookup"><span data-stu-id="53efc-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



