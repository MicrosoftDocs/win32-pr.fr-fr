---
description: Fournit des fonctionnalités étendues pour SWbemObject. À l’instar de SWbemObject, les méthodes de cet objet étendu peuvent être utilisées par tous les objets WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Objet SWbemObjectEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 642b76cde4f4e27979dae0e930ec987dc9a02d36aa8d17c7dcdd9b8785204ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860149"
---
# <a name="swbemobjectex-object"></a>Objet SWbemObjectEx

L’objet **SWbemObjectEx** fournit des fonctionnalités étendues pour [**SWbemObject**](swbemobject.md). À l’instar de **SWbemObject**, les méthodes de cet objet étendu peuvent être utilisées par tous les objets WMI. Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membres

L’objet **SWbemObjectEx** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemObjectEx** a ces méthodes.



| Méthode                                      | Description                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Retourne un fichier texte qui affiche le contenu d’un objet en XML.<br/> |
| [**Générer\_**](swbemobjectex-refresh-.md) | Actualise les données d’un objet.<br/>                                  |
| **SetFromText\_**                           | Réservé pour un usage futur.<br/>                                      |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemObjectEx** a ces propriétés.



| Propriété                                                                 | Type d’accès           | Description                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemProperties\_**](swbemobjectex-systemproperties-.md)<br/> | Lecture/écriture<br/> | Objet [**SWbemPropertySet**](swbempropertyset.md) qui contient la collection de propriétés système qui s’appliquent à **SWbemObjectEx**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> <dt>

[**M**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

