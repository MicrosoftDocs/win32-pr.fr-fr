---
description: La propriété SummaryInformation de l’objet de base de données retourne un objet SummaryInfo qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propriété Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf181b35457b8f4be5737bfa31cf284d86ed21f48800dcab6044cef444a5b640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947576"
---
# <a name="databasesummaryinformation-property"></a>Propriété Database. SummaryInformation

La propriété **SummaryInformation** de l’objet [**de base de données**](database-object.md) retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d' [informations de synthèse](summary-information-stream.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valeur de la propriété

Nombre maximal de propriétés à ajouter ou à modifier. Ce paramètre est obligatoire et utilisé pour allouer une quantité de mémoire de travail suffisante pendant la génération du flux. Il n’est pas nécessaire de stocker ce nombre de propriétés. La valeur zéro doit être utilisée si la base de données est ouverte en lecture seule pour empêcher la mise à jour du flux.

## <a name="remarks"></a>Remarques

Si une valeur de *maxProperties* supérieure à 0 est utilisée pour ouvrir un flux d’informations de résumé existant, la méthode [**Persist**](summaryinfo-persist.md) doit être appelée avant la fermeture de l’objet. Si vous ne le faites pas, les informations de flux existantes seront perdues.

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




