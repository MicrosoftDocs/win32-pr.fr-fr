---
description: La propriété SummaryInformation de l’objet installer retourne un objet SummaryInfo qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse d’un package ou d’une transformation.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer. SummaryInformation, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541016"
---
# <a name="installersummaryinformation-property"></a>Installer. SummaryInformation, propriété

La propriété **SummaryInformation** de l’objet [**installer**](installer-object.md) retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse d’un package ou d’une transformation.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Si une valeur de *maxProperties* supérieure à 0 est utilisée pour ouvrir un flux d’informations de résumé existant, la méthode [**Persist**](summaryinfo-persist.md) doit être appelée avant la fermeture de l’objet. Si ce n’est pas le cas, les informations de flux existantes sont perdues.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




