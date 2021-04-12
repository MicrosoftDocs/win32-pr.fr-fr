---
title: Attributs de liste prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs de liste obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Attributs de liste prédéfinis (Text Services Framework)
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105385"
---
# <a name="predefined-list-attributes"></a>Attributs de liste prédéfinis

Les valeurs suivantes identifient les attributs de liste obtenus avec la méthode [ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Le format de données et le contenu de chaque type de propriété sont inclus.

## <a name="properties"></a>Propriétés



| Propriété                          | Description                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| \_Liste TSATTRID                    | Non utilisé.                                                                                       |
| TSATTRID \_ liste de \_ LevelIndel        | Contient le niveau d’index de la liste. 1 est le niveau le plus à l’extérieur, 2 est le niveau suivant, et ainsi de suite. |
| \_Type de liste TSATTRID \_              | Non utilisé.                                                                                       |
| \_Type de liste TSATTRID \_ \_ arabe      | Contient une valeur différente de zéro si la liste est une liste de chiffres arabes ou zéro dans le cas contraire.               |
| \_ \_ Puce type de liste TSATTRID \_      | Contient une valeur différente de zéro si la liste est une liste à puces ou zéro dans le cas contraire.                      |
| \_Type de liste TSATTRID \_ \_ LowerLetter | Contient une valeur différente de zéro si la liste est une liste avec des lettres minuscules ou zéro dans le cas contraire.            |
| \_Type de liste TSATTRID \_ \_ LowerRoman  | Contient une valeur différente de zéro si la liste est une liste de chiffres romains en minuscules ou zéro dans le cas contraire.       |
| \_Type de liste TSATTRID \_ \_ UpperLetter | Contient une valeur différente de zéro si la liste est une liste avec lettres majuscules ou zéro dans le cas contraire.          |
| \_Type de liste TSATTRID \_ \_ UpperRoman  | Contient une valeur différente de zéro si la liste est une liste de chiffres romains en majuscules ou zéro dans le cas contraire.      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                       |
| En-tête<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

