---
description: L’objet SummaryInfo est utilisé pour lire, créer et mettre à jour des propriétés de document à partir du flux d’informations de synthèse d’un objet de stockage.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Objet SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535263"
---
# <a name="summaryinfo-object"></a>Objet SummaryInfo

L’objet **SummaryInfo** est utilisé pour lire, créer et mettre à jour des propriétés de document à partir du [flux d’informations de synthèse](summary-information-stream.md) d’un objet de stockage.

## <a name="members"></a>Membres

L’objet **SummaryInfo** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SummaryInfo** a ces méthodes.



| Méthode                                 | Description                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conserver**](summaryinfo-persist.md) | Met en forme et écrit les propriétés précédemment stockées dans le [flux d’informations de résumé](summary-information-stream.md)standard.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SummaryInfo** a ces propriétés.



| Propriété                                                                             | Description                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Property, propriété (objet SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Obtient ou définit la valeur de la propriété spécifiée dans le flux d’informations de synthèse.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indique le nombre actuel de valeurs de propriété dans l’objet d’informations de résumé.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriété SummaryInformation (objet Database)**](database-summaryinformation.md)
</dt> <dt>

[**Propriété SummaryInformation (objet installer)**](installer-summaryinformation.md)
</dt> <dt>

[Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




