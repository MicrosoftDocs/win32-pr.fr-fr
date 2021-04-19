---
description: La méthode Persist de l’objet SummaryInfo met en forme et écrit les propriétés précédemment stockées dans le flux SummaryInformation standard.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. Persist, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530325"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo. Persist, méthode

La méthode **Persist** de l’objet [**SummaryInfo**](summaryinfo-object.md) met en forme et écrit les propriétés précédemment stockées dans le flux SummaryInformation standard. Elle génère une erreur si le flux ne peut pas être correctement écrit. Cette méthode ne peut être appelée qu’une seule fois après que toutes les valeurs de propriété ont été définies. Les propriétés peuvent toujours être lues après l’écriture du flux.

## <a name="syntax"></a>Syntaxe


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




