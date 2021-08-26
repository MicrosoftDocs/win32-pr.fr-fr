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
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039599"
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



 

 




