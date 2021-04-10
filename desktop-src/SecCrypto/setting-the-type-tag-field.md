---
description: Les variables de type VARIANT ont un champ de balise de type VT qui indique le type de données des données.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Définition du champ de balise de type
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201209"
---
# <a name="setting-the-type-tag-field"></a><span data-ttu-id="16cc6-103">Définition du champ de balise de type</span><span class="sxs-lookup"><span data-stu-id="16cc6-103">Setting the Type Tag Field</span></span>

<span data-ttu-id="16cc6-104">Les variables de type **Variant** ont un champ de balise de type **VT** qui indique le type de données des données.</span><span class="sxs-lookup"><span data-stu-id="16cc6-104">**VARIANT** type variables have a type tag field **vt** that indicates the data type of the data.</span></span> <span data-ttu-id="16cc6-105">Les valeurs de retour de type **Variant** sont retournées par les méthodes avec le champ type tag défini sur le type de données de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="16cc6-105">**VARIANT** type return values are returned by methods with the type tag field set to the data type of the return value.</span></span> <span data-ttu-id="16cc6-106">Les paramètres d’entrée de type **Variant** dans un appel de méthode doivent avoir le champ de balise de type défini par l’application sur l’une des valeurs prises en charge.</span><span class="sxs-lookup"><span data-stu-id="16cc6-106">**VARIANT** type input parameters in a method call must have the type tag field set by the application to one of the supported values.</span></span> <span data-ttu-id="16cc6-107">La correspondance entre les types de paramètres et les types de données est la suivante.</span><span class="sxs-lookup"><span data-stu-id="16cc6-107">The correspondence of parameter types to data types is as follows.</span></span>



| <span data-ttu-id="16cc6-108">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="16cc6-108">Parameter type</span></span>              | <span data-ttu-id="16cc6-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="16cc6-109">Data type</span></span>                                      |
|-----------------------------|------------------------------------------------|
| <span data-ttu-id="16cc6-110">PROPTYPE \_ long</span><span class="sxs-lookup"><span data-stu-id="16cc6-110">PROPTYPE\_LONG</span></span><br/>   | <span data-ttu-id="16cc6-111">VT \_ I2 ou VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="16cc6-111">VT\_I2 or VT\_I4</span></span><br/>                    |
| <span data-ttu-id="16cc6-112">\_Date PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="16cc6-112">PROPTYPE\_DATE</span></span><br/>   | <span data-ttu-id="16cc6-113">\_Date VT</span><span class="sxs-lookup"><span data-stu-id="16cc6-113">VT\_DATE</span></span><br/>                            |
| <span data-ttu-id="16cc6-114">\_binaire PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="16cc6-114">PROPTYPE\_BINARY</span></span><br/> | <span data-ttu-id="16cc6-115">VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="16cc6-115">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |
| <span data-ttu-id="16cc6-116">\_chaîne PROPTYPE</span><span class="sxs-lookup"><span data-stu-id="16cc6-116">PROPTYPE\_STRING</span></span><br/> | <span data-ttu-id="16cc6-117">VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="16cc6-117">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |



 

<span data-ttu-id="16cc6-118">L’exemple suivant montre comment initialiser les types de données variant listés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="16cc6-118">The following example shows how to initialize the variant data types listed above.</span></span>


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




