---
description: Génère des représentations XML des objets.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Représentation d’objets en XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518397"
---
# <a name="representing-objects-in-xml"></a><span data-ttu-id="c2d5a-103">Représentation d’objets en XML</span><span class="sxs-lookup"><span data-stu-id="c2d5a-103">Representing Objects in XML</span></span>

<span data-ttu-id="c2d5a-104">Le composant XML encoder dans WMI génère des représentations XML des objets.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="c2d5a-105">En C++, vous pouvez démarrer l’encodeur XML avec un appel à la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , en spécifiant l’objet à représenter en XML et le format texte à utiliser dans la représentation.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="c2d5a-106">Pour plus d’informations et pour obtenir un exemple de code, consultez pour encoder un objet en XML à l’aide de C/C++.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="c2d5a-107">Dans VBScript ou Visual Basic, pour encoder les données d’une instance XML, appelez [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="c2d5a-108">Pour plus d’informations et pour obtenir un exemple de code, consultez pour encoder un objet en XML à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="c2d5a-109">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="c2d5a-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c2d5a-110">Encoder un objet à l’aide de C ou C++</span><span class="sxs-lookup"><span data-stu-id="c2d5a-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="c2d5a-111">Encoder un objet à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="c2d5a-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="c2d5a-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2d5a-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="c2d5a-113">Encoder un objet à l’aide de C ou C++</span><span class="sxs-lookup"><span data-stu-id="c2d5a-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="c2d5a-114">La procédure suivante décrit comment encoder un objet en XML à l’aide de C ou C++.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="c2d5a-115">**Pour encoder un objet en XML à l’aide de C ou C++**</span><span class="sxs-lookup"><span data-stu-id="c2d5a-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="c2d5a-116">Configurez votre programme pour accéder aux données WMI.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="c2d5a-117">Étant donné que WMI est basé sur la technologie COM, vous devez effectuer les appels requis aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accéder à WMI.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="c2d5a-118">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="c2d5a-119">Si vous le souhaitez, créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) et initialisez-le.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="c2d5a-120">Vous n’avez pas besoin de créer l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , sauf si vous devez modifier l’opération par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="c2d5a-121">L’objet de contexte est utilisé par l’encodeur XML pour contrôler la quantité d’informations incluses dans la représentation XML de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="c2d5a-122">Le tableau suivant répertorie les valeurs facultatives qui peuvent être spécifiées pour l’objet de contexte.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c2d5a-123">Valeur/type</span><span class="sxs-lookup"><span data-stu-id="c2d5a-123">Value/type</span></span></th>
    <th><span data-ttu-id="c2d5a-124">Signification</span><span class="sxs-lookup"><span data-stu-id="c2d5a-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c2d5a-125">&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</span><span class="sxs-lookup"><span data-stu-id="c2d5a-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="c2d5a-126">Lorsque la <strong>valeur est true</strong>, seules les propriétés et les méthodes définies localement dans la classe sont présentes dans le XML résultant.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="c2d5a-127">La valeur par défaut est <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c2d5a-128">&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="c2d5a-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="c2d5a-129">Quand la <strong>valeur est true</strong>, la classe, l’instance, les propriétés et les qualificateurs de méthode sont inclus dans le XML résultant.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="c2d5a-130">La valeur par défaut est <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c2d5a-131">&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="c2d5a-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="c2d5a-132">Si la <strong>valeur est true</strong>, les propriétés système WMI sont filtrées en dehors de la sortie.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="c2d5a-133">La valeur par défaut est <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c2d5a-134">&quot;PathLevel &quot; <strong>VT_I4</strong></span><span class="sxs-lookup"><span data-stu-id="c2d5a-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="c2d5a-135">0 = un <CLASS> <INSTANCE> élément ou est généré.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="c2d5a-136">1 = un <VALUE.NAMEDOBJECT> élément est généré.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="c2d5a-137">2 = un <VALUE.OBJECTWITHLOCALPATH> élément est généré.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="c2d5a-138">3 = une <VALUE.OBJECTWITHPATH> est générée.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="c2d5a-139">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="c2d5a-140">L’exemple de code suivant montre comment l’objet de contexte est initialisé pour inclure des qualificateurs et exclure des propriétés système.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  <span data-ttu-id="c2d5a-141">Obtient une référence à la classe ou à l’instance à encoder en XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="c2d5a-142">Une fois que vous avez initialisé COM et que vous êtes connecté à WMI, appelez [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer une référence à la classe ou à l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="c2d5a-143">Si vous avez utilisé un BSTR pour spécifier la classe ou l’instance, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée par [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="c2d5a-144">L’exemple de code suivant récupère une référence à une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c2d5a-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  <span data-ttu-id="c2d5a-145">Créez un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .</span><span class="sxs-lookup"><span data-stu-id="c2d5a-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="c2d5a-146">Une fois que vous avez une référence à un objet, vous devez créer l’objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) à l’aide d’un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="c2d5a-147">L’objet **IWbemObjectTextSrc** est utilisé pour générer le texte XML réel.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="c2d5a-148">L’exemple de code suivant montre comment créer un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  <span data-ttu-id="c2d5a-149">Appelez la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) pour récupérer une représentation XML d’un objet.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="c2d5a-150">Après avoir défini le contexte de la représentation de l’objet, obtenu une référence à l’objet et créé un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , vous êtes prêt à générer une représentation XML de l’objet spécifié en appelant la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="c2d5a-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="c2d5a-151">L’exemple de code C++ suivant génère une représentation XML de l’objet référencé par *pclass*.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="c2d5a-152">La représentation XML est retournée dans *strText*.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="c2d5a-153">Le troisième paramètre de [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) spécifie le format de texte à utiliser pour le code XML. il doit s’agir du texte \_ \_ DTD WMI \_ CIM \_ DTD \_ 2 \_ 0 (0x1) ou du \_ texte obj WMI \_ \_ \_ DTD WMI \_ 2 \_ 0 (0X2).</span><span class="sxs-lookup"><span data-stu-id="c2d5a-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="c2d5a-154">Pour plus d’informations sur ces valeurs, consultez valeurs des paramètres [**IWbemObjectTextSrc :: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="c2d5a-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

<span data-ttu-id="c2d5a-155">L’exemple de code C++ suivant inclut toutes les étapes de la procédure précédente et encode la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, y compris les qualificateurs de classe, de propriété et de méthode, et en excluant les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="c2d5a-156">Encoder un objet à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="c2d5a-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="c2d5a-157">La procédure suivante décrit comment encoder un objet en XML à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="c2d5a-158">**Pour encoder un objet en XML à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="c2d5a-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="c2d5a-159">Si vous le souhaitez, créez un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) et initialisez-le afin de définir les valeurs de contexte requises pour la représentation XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="c2d5a-160">L’exemple de code suivant montre comment les valeurs indiquent à l’encodeur XML de générer une valeur <. OBJECTWITHLOCALPATH> élément, y compris tous les qualificateurs et exclusion des propriétés système lorsqu’il construit la représentation XML de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="c2d5a-161">Récupérez une instance de l’objet ou de la classe à représenter en XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="c2d5a-162">L’exemple de code suivant récupère une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="c2d5a-163">Appelez la [**méthode \_ gettext**](swbemobjectex-gettext-.md) de l’instance créée à l’étape précédente, en utilisant 1 comme paramètre pour spécifier le format de texte qui correspond à la version DTD CIM 2,0, ou 2 pour spécifier le format de texte qui correspond à la version 2,0 du DTD WMI.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="c2d5a-164">Si vous avez créé l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) à l’étape 1, incluez-le dans la liste de paramètres comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="c2d5a-165">L’exemple de code suivant montre comment appeler la [**méthode \_ gettext**](swbemobjectex-gettext-.md) de l’instance.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="c2d5a-166">Si vous le souhaitez, vérifiez que le code XML généré à l’étape 3 est bien formé en XML, en créant et en initialisant un objet XML Document Object Model (DOM), puis en y chargeant le texte XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="c2d5a-167">L’exemple de code suivant montre comment créer et initialiser un objet DOM XML et y charger le texte XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="c2d5a-168">Sortie de la représentation XML de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="c2d5a-169">L’exemple de code suivant montre comment utiliser WScript pour générer le code XML.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="c2d5a-170">Si vous avez choisi d’utiliser le modèle DOM XML pour vérifier que le code XML généré est bien formé, remplacez la ligne précédente par ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="c2d5a-171">L’exemple de code VBScript suivant inclut toutes les étapes de la procédure précédente et encode la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, y compris les qualificateurs de classe, de propriété et de méthode, et en excluant les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="c2d5a-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a><span data-ttu-id="c2d5a-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2d5a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d5a-173">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="c2d5a-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

