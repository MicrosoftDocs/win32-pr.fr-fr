---
description: Normalement, l’accès direct est suffisant pour appeler une méthode de fournisseur WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construction d’objets Parameters et analyse d’objets de paramètres de paramétrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952469"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Construction d’objets Parameters et analyse d’objets de paramètres de paramétrage

Normalement, l’accès direct est suffisant pour appeler une [*méthode de fournisseur*](gloss-p.md)WMI. L’accès direct implique l’exécution d’une méthode à l’aide de la syntaxe *Object. Method* . Toutefois, dans certains cas, l’accès direct ne peut pas être utilisé. En outre, l’appel d’une méthode de fournisseur de manière asynchrone à partir d’un script nécessite un type d’appel [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

L’ordre des paramètres d’entrée et de sortie de la méthode est défini dans le schéma format MOF (MOF) de la méthode. WMI n’empêche pas la modification de l’ordre des paramètres lorsque la classe est recompilée par [mofcomp](mofcomp.md). En utilisant un objet [**Parameters**](swbemmethod-inparameters.md) , vous pouvez éviter les problèmes qui résultent d’un schéma modifié, car les paramètres d’entrée sont identifiés par leur nom. Le paramètre correct peut être consulté en examinant le qualificateur d' **ID** de chaque paramètre d’entrée. Le premier paramètre a une valeur d' **ID** égale à 0 (zéro).

[**Les méthodes SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)et [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) offrent un autre moyen d’exécuter une méthode de fournisseur dans les cas où il n’est pas possible d’exécuter directement une méthode. Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

Pour plus d’informations sur les paramètres, consultez [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres de paramètres](parsing-outparameters-objects.md).

 

 



