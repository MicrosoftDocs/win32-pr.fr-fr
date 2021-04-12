---
title: SystemMonitor. GraphTitle, propriété
description: Récupère ou définit le titre du graphique.
ms.assetid: 10a91b38-6963-4ef6-8b4f-9ecd1341f471
keywords:
- Propriété GraphTitle SysMon
- Propriété GraphTitle SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété GraphTitle
topic_type:
- apiref
api_name:
- SystemMonitor.GraphTitle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55918b67eb88b8c2c1aca99ce6e86f190ad1a395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508586"
---
# <a name="systemmonitorgraphtitle-property"></a>SystemMonitor. GraphTitle, propriété

Récupère ou définit le titre du graphique.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property GraphTitle As String
```



## <a name="property-value"></a>Valeur de la propriété

Titre du graphique. La longueur maximale du titre est de 128 caractères. Si le titre dépasse 128 caractères, le titre est tronqué.

**Windows XP et windows 2000 :** Il n’existe aucune limite à la longueur du titre.

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

 

 





