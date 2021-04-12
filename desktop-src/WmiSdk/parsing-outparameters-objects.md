---
description: Un objet SWbemMethod. unmeters est créé et fourni avec les données par la méthode du fournisseur en cours d’exécution.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analyse d’objets de paramètres de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320534"
---
# <a name="parsing-outparameters-objects"></a>Analyse d’objets de paramètres de paramètres

Un objet [**SWbemMethod. Unmeters**](swbemmethod-outparameters.md) est créé et fourni avec les données par la méthode du fournisseur en cours d’exécution. Les propriétés de l’objet de **paramètres de paramètres** sont spécifiques à la méthode appelée. Par exemple, dans le script ci-dessous, *SD* (contenu dans l’en- *para*) est le paramètre de sortie défini pour la méthode **\_ \_ SystemSecurity.** La propriété **returnValue** est une propriété générique disponible pour tous les objets de **paramètres de paramètres** qui contiennent le résultat de l’opération.

L’exemple de code suivant illustre l’obtention de paramètres de sortie à partir [**de l’exécution de la méthode**](--systemsecurity-getsd.md) Unattended dans la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) pour le système local.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Pour plus d’informations, consultez [**SWbemMethod. inparamètres**](swbemmethod-inparameters.md).

 

 



