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
# <a name="representing-objects-in-xml"></a>Représentation d’objets en XML

Le composant XML encoder dans WMI génère des représentations XML des objets.

En C++, vous pouvez démarrer l’encodeur XML avec un appel à la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , en spécifiant l’objet à représenter en XML et le format texte à utiliser dans la représentation. Pour plus d’informations et pour obtenir un exemple de code, consultez pour encoder un objet en XML à l’aide de C/C++.

Dans VBScript ou Visual Basic, pour encoder les données d’une instance XML, appelez [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md). Pour plus d’informations et pour obtenir un exemple de code, consultez pour encoder un objet en XML à l’aide de VBScript.

Les sections suivantes sont présentées dans cette rubrique :

-   [Encoder un objet à l’aide de C ou C++](#encode-an-object-using-c-or-c)
-   [Encoder un objet à l’aide de VBScript](#encode-an-object-using-vbscript)
-   [Rubriques connexes](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Encoder un objet à l’aide de C ou C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

La procédure suivante décrit comment encoder un objet en XML à l’aide de C ou C++.

**Pour encoder un objet en XML à l’aide de C ou C++**

1.  Configurez votre programme pour accéder aux données WMI.

    Étant donné que WMI est basé sur la technologie COM, vous devez effectuer les appels requis aux fonctions [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accéder à WMI. Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).

2.  Si vous le souhaitez, créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) et initialisez-le.

    Vous n’avez pas besoin de créer l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , sauf si vous devez modifier l’opération par défaut. L’objet de contexte est utilisé par l’encodeur XML pour contrôler la quantité d’informations incluses dans la représentation XML de l’objet.

    Le tableau suivant répertorie les valeurs facultatives qui peuvent être spécifiées pour l’objet de contexte.

    

    <table>
    <thead>
    <tr class="header">
    <th>Valeur/type</th>
    <th>Signification</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</td>
    <td>Lorsque la <strong>valeur est true</strong>, seules les propriétés et les méthodes définies localement dans la classe sont présentes dans le XML résultant. La valeur par défaut est <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></td>
    <td>Quand la <strong>valeur est true</strong>, la classe, l’instance, les propriétés et les qualificateurs de méthode sont inclus dans le XML résultant. La valeur par défaut est <strong>FALSE</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></td>
    <td>Si la <strong>valeur est true</strong>, les propriétés système WMI sont filtrées en dehors de la sortie. La valeur par défaut est <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;PathLevel &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = un <CLASS> <INSTANCE> élément ou est généré.<br />
1 = un <VALUE.NAMEDOBJECT> élément est généré.<br />
2 = un <VALUE.OBJECTWITHLOCALPATH> élément est généré.<br />
3 = une <VALUE.OBJECTWITHPATH> est générée.<br />
    </dl> La valeur par défaut est 0 (zéro).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    L’exemple de code suivant montre comment l’objet de contexte est initialisé pour inclure des qualificateurs et exclure des propriétés système.

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

    

3.  Obtient une référence à la classe ou à l’instance à encoder en XML.

    Une fois que vous avez initialisé COM et que vous êtes connecté à WMI, appelez [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer une référence à la classe ou à l’instance spécifiée. Si vous avez utilisé un BSTR pour spécifier la classe ou l’instance, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée par [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).

    L’exemple de code suivant récupère une référence à une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

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

    

4.  Créez un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .

    Une fois que vous avez une référence à un objet, vous devez créer l’objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) à l’aide d’un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). L’objet **IWbemObjectTextSrc** est utilisé pour générer le texte XML réel.

    L’exemple de code suivant montre comment créer un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

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

    

5.  Appelez la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) pour récupérer une représentation XML d’un objet.

    Après avoir défini le contexte de la représentation de l’objet, obtenu une référence à l’objet et créé un objet [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , vous êtes prêt à générer une représentation XML de l’objet spécifié en appelant la méthode [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

    L’exemple de code C++ suivant génère une représentation XML de l’objet référencé par *pclass*. La représentation XML est retournée dans *strText*. Le troisième paramètre de [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) spécifie le format de texte à utiliser pour le code XML. il doit s’agir du texte \_ \_ DTD WMI \_ CIM \_ DTD \_ 2 \_ 0 (0x1) ou du \_ texte obj WMI \_ \_ \_ DTD WMI \_ 2 \_ 0 (0X2). Pour plus d’informations sur ces valeurs, consultez valeurs des paramètres [**IWbemObjectTextSrc :: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

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

    

L’exemple de code C++ suivant inclut toutes les étapes de la procédure précédente et encode la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, y compris les qualificateurs de classe, de propriété et de méthode, et en excluant les propriétés système.


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



## <a name="encode-an-object-using-vbscript"></a>Encoder un objet à l’aide de VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

La procédure suivante décrit comment encoder un objet en XML à l’aide de VBScript.

**Pour encoder un objet en XML à l’aide de VBScript**

1.  Si vous le souhaitez, créez un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) et initialisez-le afin de définir les valeurs de contexte requises pour la représentation XML.

    L’exemple de code suivant montre comment les valeurs indiquent à l’encodeur XML de générer une valeur <. OBJECTWITHLOCALPATH> élément, y compris tous les qualificateurs et exclusion des propriétés système lorsqu’il construit la représentation XML de l’objet.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Récupérez une instance de l’objet ou de la classe à représenter en XML.

    L’exemple de code suivant récupère une instance de l’objet.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Appelez la [**méthode \_ gettext**](swbemobjectex-gettext-.md) de l’instance créée à l’étape précédente, en utilisant 1 comme paramètre pour spécifier le format de texte qui correspond à la version DTD CIM 2,0, ou 2 pour spécifier le format de texte qui correspond à la version 2,0 du DTD WMI. Si vous avez créé l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) à l’étape 1, incluez-le dans la liste de paramètres comme troisième paramètre.

    L’exemple de code suivant montre comment appeler la [**méthode \_ gettext**](swbemobjectex-gettext-.md) de l’instance.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Si vous le souhaitez, vérifiez que le code XML généré à l’étape 3 est bien formé en XML, en créant et en initialisant un objet XML Document Object Model (DOM), puis en y chargeant le texte XML.

    L’exemple de code suivant montre comment créer et initialiser un objet DOM XML et y charger le texte XML.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Sortie de la représentation XML de l’objet.

    L’exemple de code suivant montre comment utiliser WScript pour générer le code XML.

    ```VB
    wscript.echo strText
    ```

    

    Si vous avez choisi d’utiliser le modèle DOM XML pour vérifier que le code XML généré est bien formé, remplacez la ligne précédente par ce qui suit.

    ```VB
    wscript.echo xml.xml
    ```

    

L’exemple de code VBScript suivant inclut toutes les étapes de la procédure précédente et encode la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, y compris les qualificateurs de classe, de propriété et de méthode, et en excluant les propriétés système.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

