---
title: Autres attributs prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs divers obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Autres attributs prédéfinis Text Services Framework
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536917"
---
# <a name="other-predefined-attributes"></a>Autres attributs prédéfinis

Les valeurs suivantes identifient les attributs divers obtenus avec la méthode [ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Le format de données et le contenu de chaque type de propriété sont inclus.

## <a name="properties"></a>Propriétés



| Propriété                             | Description                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| **\_Application TSATTRID**                    | Non utilisé.                                                                         |
| **\_Application TSATTRID \_ IncorrectGrammar**  | Contient une valeur différente de zéro si le texte contient une erreur de grammaire ou zéro dans le cas contraire.  |
| **\_Application TSATTRID \_ IncorrectSpelling** | Contient une valeur différente de zéro si le texte contient une faute d’orthographe ou zéro dans le cas contraire. |
| **TSATTRID \_ autres**                 | Non utilisé.                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                       |
| En-tête<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 

