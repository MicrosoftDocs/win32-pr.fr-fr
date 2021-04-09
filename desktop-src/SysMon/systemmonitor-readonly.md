---
title: SystemMonitor. ReadOnly, propriété
description: Récupère ou définit une valeur qui détermine si un utilisateur peut modifier les valeurs de propriété du contrôle.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propriété ReadOnly SysMon
- Propriété ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942087"
---
# <a name="systemmonitorreadonly-property"></a>SystemMonitor. ReadOnly, propriété

Récupère ou définit une valeur qui détermine si un utilisateur peut modifier les valeurs de propriété du contrôle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True si vous ne souhaitez pas que l’utilisateur modifie les valeurs de propriété du contrôle ; Sinon, false. La valeur par défaut est false, ce qui signifie que les utilisateurs peuvent modifier les valeurs de propriété du contrôle.

## <a name="remarks"></a>Notes

Lorsque la valeur de cette propriété est true, les conditions suivantes sont appliquées :

-   L’utilisateur ne peut pas utiliser le menu contextuel.
-   Les boutons de barre d’outils suivants sont désactivés :
    -   Nouvel ensemble de compteurs
    -   Afficher l'activité actuelle
    -   Afficher les données du fichier journal
    -   Ajouter
    -   DELETE
    -   Coller la liste des compteurs
    -   Propriétés

Notez que cette propriété affecte uniquement la capacité de l’utilisateur à modifier les valeurs de propriété par le biais de l’interface utilisateur, mais elle ne vous empêche pas de modifier par programmation les valeurs de propriété ou les compteurs.

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

 

 





