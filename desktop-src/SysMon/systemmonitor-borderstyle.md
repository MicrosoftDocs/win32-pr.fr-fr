---
title: SystemMonitor. BorderStyle, propriété
description: Récupère ou définit le style de bordure du contrôle.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propriété BorderStyle SysMon
- Propriété BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843473"
---
# <a name="systemmonitorborderstyle-property"></a>SystemMonitor. BorderStyle, propriété

Récupère ou définit le style de bordure du contrôle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Valeur de la propriété

Style de bordure du contrôle.

Vous pouvez définir cette propriété sur l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                                                                                                   | Signification                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt> </dl>                     | Aucune bordure. Il s’agit de la valeur par défaut.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt> </dl> | Fixe, bordure simple.<br/>                 |



 

## <a name="exceptions"></a>Exceptions



| Type d'exception               | Condition                                |
|------------------------------|------------------------------------------|
| **System.ArgumentException** | Le style de bordure spécifié n’est pas valide. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





