---
title: Composition des noms de principal du service pour un service avec SCP
description: L’exemple de code suivant compose un SPN pour un service qui utilise un point de connexion de service (SCP).
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Composition des noms de principal du service pour un service avec une publicité SCP
- Nom de principal du service AD, composition de SPN pour un service avec SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922068"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>Composition des noms de principal du service pour un service avec SCP

L’exemple de code suivant compose un SPN pour un service qui utilise un point de connexion de service (SCP). Le SPN retourné a le format suivant.


```C++
<service class>/<host>/<service name>
```



« &lt; classe de service &gt; » et « &lt; nom &gt; du service » correspondent aux paramètres *pszDNofSCP* et *pszServiceClass* . &lt; &gt; la valeur par défaut « Host » est le nom DNS de l’ordinateur local.


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




