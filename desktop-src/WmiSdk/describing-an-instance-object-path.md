---
description: Un chemin d’accès d’objet d’instance décrit l’emplacement d’une instance d’une classe donnée dans un espace de noms spécifique.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet d’instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319794"
---
# <a name="describing-an-instance-object-path"></a>Description d’un chemin d’accès d’objet d’instance

Un chemin d’accès d’objet d’instance décrit l’emplacement d’une instance d’une classe donnée dans un espace de noms spécifique.

Vous pouvez avoir plusieurs types différents de chemins d’accès d’objet d’instance :

-   Complète

    Un chemin d’accès complet à un objet d’instance ajoute le nom et la valeur de la propriété de clé pour la classe à un chemin d’accès d’objet de classe complet.

    L’exemple suivant illustre la définition du chemin d’accès complet à l’objet instance.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relatif

    Un chemin d’accès relatif à un objet fait référence à une instance située dans l’espace de noms actuel sur le serveur actuel. Le chemin d’accès relatif se compose du nom de la classe suivi des noms et des valeurs des propriétés de clé de cette instance.

    L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relative.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relatif avec une clé unique

    Pour les classes avec une seule propriété désignée comme clé, vous pouvez omettre le nom de la propriété de clé.

    L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relatif avec une clé unique.

    ``` syntax
    MyClass="e:"
    ```

-   Relatif à plusieurs clés

    Utilisez une virgule pour faire la distinction entre les clés d’une instance avec plusieurs clés.

    L’exemple suivant montre les définitions du chemin d’accès de l’objet d’instance relatif avec plusieurs clés.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relatif pour une classe singleton

    Le chemin d’accès relatif d’un objet pour une classe singleton se compose du nom de la classe suivi de la notation « = @ ».

    L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relative pour une classe singleton.

    ``` syntax
    MySingletonClass=@
    ```

La procédure suivante décrit comment récupérer une instance de classe.

**Pour récupérer une instance de classe**

1.  Initialisez une chaîne qui contient le chemin d’accès de l’objet avec un appel à la fonction [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .
2.  Initialise un objet qui recevra l’instance.
3.  Récupérez l’objet à l’aide d’un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Pour utiliser [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), vous devez implémenter l’interface [**IWbemSink**](swbemsink.md) .

L' \# instruction include suivante est requise pour le code qui est indiqué plus loin dans cette rubrique pour compiler correctement.


```C++
#include <wbemidl.h>
```



L’exemple de code suivant décrit comment récupérer une instance de classe à l’aide d’un chemin d’accès à un objet.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Pour les instances de classes qui spécifient plusieurs propriétés en tant que clé, WMI ne requiert aucun classement spécifique des propriétés de clé dans les chemins d’accès aux objets. Vous devez uniquement spécifier la valeur de chacune des propriétés dans le chemin d’accès de l’objet.

L’exemple de code suivant décrit deux descriptions de clé équivalentes.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
