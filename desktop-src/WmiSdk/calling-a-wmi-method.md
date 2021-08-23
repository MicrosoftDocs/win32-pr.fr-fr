---
title: Comment appeler une méthode WMI
description: L’objectif principal de WMI est de fournir l’accès aux classes et aux instances qui représentent des objets sur votre réseau.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1de14f06388454228528d5a419b551ae2ed0d72c82e3b78c9e04855db6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051047"
---
# <a name="how-to-call-a-wmi-method"></a>Comment appeler une méthode WMI

L’objectif principal de WMI est de fournir l’accès aux classes et aux instances qui représentent des objets sur votre réseau. Ces classes et instances sont prises en charge par les fournisseurs. Par exemple, toutes les instances qui représentent des périphériques matériels standard de votre entreprise, tels que [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) ou [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer), sont prises en charge par le fournisseur Win32. De même, vous pouvez accéder au journal des événements par le biais du fournisseur du journal des événements et du Registre par le biais du fournisseur de registre.

Les méthodes implémentées par WMI dans des interfaces telles que [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou des objets de script tels que [**SWbemServices**](swbemservices.md), sont principalement destinées à l’obtention et à la manipulation génériques des données fournies par n’importe quel fournisseur. Par exemple, utilisez [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) pour obtenir toutes les instances du [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) dans un sous-ensemble d’ordinateurs d’entreprise. Vous pouvez ensuite appeler la méthode du fournisseur Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) sur chaque objet de **\_ processus Win32** .

Dans l’exemple suivant, la méthode [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) est appelée en tant que méthode Automation sur l’objet Process. Une méthode WMI, telle que la [**méthode \_ path**](swbemobject-path-.md) définie pour [**SWbemObject**](swbemobject.md) , peut également être appelée sur l’objet **Process** .


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



le processus d’utilisation des méthodes WMI est identique à celui des autres Windows COM ou de l’interface d’automatisation. Pour plus d’informations, consultez [com](../cossdk/component-services-portal.md) et [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md). Pour plus d’informations sur les interfaces prises en charge par WMI, consultez [API com pour WMI](com-api-for-wmi.md) et [API de script pour WMI](scripting-api-for-wmi.md).

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
