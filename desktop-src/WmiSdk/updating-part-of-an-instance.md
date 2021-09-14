---
description: Il peut arriver que vous souhaitiez mettre à jour uniquement une partie d’une instance.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Mise à jour d’une partie d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915747"
---
# <a name="updating-part-of-an-instance"></a>Mise à jour d’une partie d’une instance

Il peut arriver que vous souhaitiez mettre à jour uniquement une partie d’une instance. Par exemple, certaines instances ont un grand nombre de propriétés. Si vous deviez mettre à jour un grand nombre de ces instances, vous risquez de réduire les performances du système. Par conséquent, vous pouvez choisir de mettre à jour une partie de l’instance et, par conséquent, réduire la quantité d’informations que vous devez envoyer et récupérer vers et à partir de WMI. Toutefois, WMI ne prend pas directement en charge les opérations d’instance partielle, ni la plupart des fournisseurs. Par conséquent, si vous écrivez une application qui utilise des opérations d’instance partielle, préparez-vous à ce que vos appels échouent avec le code d’erreur **WBEM \_ e \_ \_ non \_ compatible** ou **WBEM \_ e \_ non \_ pris en charge** en C++. Dans les langages de script, les codes d’erreur sont **wbemErrProviderNotCapable** ou **wbemErrNotSupported**.

Dans les scripts, cette opération n’est nécessaire que pour faciliter les performances lors de la mise à jour d’une ou de deux propriétés accessibles en écriture dans un très grand nombre d’objets au sein d’une entreprise. Dans le cas contraire, les appels classiques de VBScript à [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md), tout en semblant d’écrire l’objet entier, sont en fait uniquement des mises à jour des propriétés pour lesquelles le fournisseur est activé en écriture.

La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de PowerShell.

**Pour demander une mise à jour d’instance partielle à l’aide de PowerShell**

1.  Récupérez le chemin d’accès de l’objet que vous souhaitez mettre à jour.

    Vous pouvez décrire le chemin d’accès manuellement ou interroger l’objet, puis récupérer la propriété **\_ \_ path** .

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Configurez une table de hachage qui répertorie les noms des propriétés à mettre à jour et utilisez cette table de hachage dans un appel à [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de C#.

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

**Pour demander une mise à jour d’instance partielle à l’aide de C #**

1.  Créez un nouvel objet [ManagementObject](/dotnet/api/system.management.managementobject) qui représente l’instance spécifique à mettre à jour.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Définissez la valeur de la propriété avec un appel à [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de VBScript.

**Pour demander une mise à jour d’instance partielle à l’aide de VBScript**

1.  Créez un objet de contexte [**SWbemNamedValueSet**](swbemnamedvalueset.md) .

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Ajoutez les valeurs d’extension put « \_ \_ put \_ extensions » et « \_ \_ put \_ ext \_ client \_ Request » à l’objet Context à l’aide de la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Configurez un tableau répertoriant les noms des propriétés à mettre à jour et ajoutez ce tableau à l’objet de contexte [**SWbemNamedValueSet**](swbemnamedvalueset.md) avec la valeur d’extension put « \_ \_ put \_ ext \_ Properties ».

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Définissez le paramètre *IFlags* de l’appel [**SWbemObject. \_ put**](swbemobject-put-.md) sur **wbemChangeFlagUpdateOnly**. Sans cet indicateur, l’appel échoue avec un contexte non valide.

5.  Transmettez votre indicateur et l’objet de contexte au fournisseur dans le paramètre *objwbemNamedValueSet* de [**SWbemObject. \_ put**](swbemobject-put-.md) ou [**SWbemObject. \_ PutAsync**](swbemobject-putasync-.md).

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

La procédure suivante décrit comment demander une mise à jour d’instance partielle à l’aide de C++.

**Pour demander une mise à jour d’instance partielle à l’aide de C++**

1.  Créez un objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un objet de contexte est un objet que WMI utilise pour transmettre plus d’informations à un fournisseur WMI. Dans ce cas, vous utilisez l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) pour indiquer au fournisseur d’accepter les mises à jour de l’instance partielle.

2.  Ajoutez les \_ \_ \_ valeurs nommées « put extensions » et « \_ \_ put \_ ext \_ client \_ Request » à l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) à l’aide d’un appel à [**IWbemContext :: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    Le tableau suivant répertorie la signification des « \_ \_ put \_ extensions » et « \_ \_ put \_ ext \_ client \_ Request ».

    

    | Valeur nommée                     | Description                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | « \_ \_ Placer les \_ Extensions »           | **VT \_ BOOL** a la valeur **Variant \_ true**. Valeur indiquant qu’une ou plusieurs des autres valeurs de contexte ont été spécifiées. Cela permet une vérification rapide de l’objet de contexte dans le fournisseur pour déterminer si des mises à jour de l’instance partielle sont utilisées. |
    | « \_ \_ put \_ ext \_ client \_ Request » | **VT \_ BOOL** a la valeur **Variant \_ true**. Défini par le client lors de la demande initiale. Cette valeur est utilisée pour empêcher les erreurs de réentrance.                                                                                                                   |

    

     

3.  Ajoutez les \_ \_ \_ valeurs put ext \_ Strictly \_ , \_ \_ put \_ ext \_ ou \_ \_ put \_ ext \_ atomique dans n’importe quelle combinaison en fonction des besoins de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec un autre appel à [**IWbemContext :: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).

    Le tableau suivant répertorie la signification des valeurs nommées.

    

    | Valeur nommée                   | Description                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | « \_ \_ put \_ ext \_ Strictly \_ NULLS » | **VT \_ BOOL** a la valeur **Variant \_ true**. Indique que le client a défini intentionnellement des propriétés sur **VT \_ null** et s’attend à ce que l’opération d’écriture aboutisse. Si le fournisseur ne peut pas définir les valeurs sur **null**, une erreur doit être signalée. |
    | « \_ \_ Placer \_ les \_ Propriétés ext »    | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de chaînes contenant une liste de noms de propriétés à mettre à jour. Peut être utilisé seul ou en combinaison avec « \_ \_ put \_ ext \_ Properties ». Les valeurs se trouvent dans l’instance en cours d’écriture.                           |
    | « \_ \_ put \_ ext \_ atomique »        | **VT \_ BOOL** a la valeur **Variant \_ true**. Indique que toutes les mises à jour doivent être exécutées simultanément (sémantique atomique) ou que le fournisseur doit être restauré. Il ne peut pas y avoir de succès partiel. Peut être utilisé seul ou en combinaison avec d’autres indicateurs.     |

    

     

4.  Définissez le paramètre *IFlags* sur **la \_ \_ mise à jour \_ de l’indicateur WBEM uniquement**. Sans cet indicateur, l’appel échoue avec un contexte non valide.
5.  Transmettez l’objet de contexte [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) dans n’importe quel appel à [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) dans le paramètre *pctX* .

    Le passage de l’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) demande au fournisseur d’autoriser les mises à jour d’instance partielle. Dans une mise à jour d’instance complète, vous devez affecter à *pctX* la **valeur null**.

    Le fournisseur peut écrire toutes les propriétés nécessaires si l’objet de contexte présent dans l’appel ne contient pas d' \_ \_ \_ Extensions put. Si « \_ \_ Placer \_ des extensions » est présent dans l’objet de contexte, WMI requiert que le fournisseur obéit exactement à la sémantique de l’opération ou qu’il ne fasse pas échouer l’appel. Pour plus d’informations, consultez [gestion des messages d’accès refusé dans un fournisseur](impersonating-a-client.md).

 

 
