---
title: Attributs de police prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs de police obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Attributs de police prédéfinis (Text Services Framework)
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21351d790a09c9364a101a62b7516698df154225
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317369"
---
# <a name="predefined-font-attributes"></a>Attributs de police prédéfinis

Les valeurs suivantes identifient les attributs de police obtenus avec la méthode [ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Le format de données et le contenu de chaque type de propriété sont inclus.

## <a name="properties"></a>Propriétés



| Propriété                                                 | Description                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **\_Police TSATTRID**                                       | Non utilisé.                                                                                                                   |
| **TSATTRID \_ police \_ FaceName**                             | Contient le nom de police de la police de texte.                                                                                    |
| **TSATTRID \_ police \_ SizePts**                              | Contient la taille en points de la police du texte.                                                                                   |
| **\_Style de police TSATTRID \_**                                | Non utilisé.                                                                                                                   |
| **\_Animation de \_ style de police TSATTRID \_**                     | Non utilisé.                                                                                                                   |
| **\_Animation de style de police TSATTRID \_ \_ \_ BlinkingBackground** | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ LasVegasLights**     | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ MarchingBlackAnts**  | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ MarchingRedAnts**    | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ vibrations**            | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ SparkleText**        | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ WipeDown**           | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **\_Animation de style de police TSATTRID \_ \_ \_ WipeRight**          | Contient une valeur différente de zéro si le texte a l’animation spécifiée ou zéro dans le cas contraire.                                         |
| **TSATTRID \_ style de police \_ \_ backgroundColor**               | Contient la valeur RVB de l’arrière-plan du texte. Contient 0xFF000000 si la couleur du texte est automatique.                          |
| **\_ \_ Clignotement du style de police TSATTRID \_**                         | Contient une valeur différente de zéro si le texte clignote ou zéro dans le cas contraire.                                                         |
| **\_Style de police TSATTRID \_ \_ gras**                          | Contient une valeur différente de zéro si le texte est gras ou zéro dans le cas contraire.                                                             |
| **\_ \_ Style \_ majuscule de la police TSATTRID**                    | Contient une valeur différente de zéro si le texte est en majuscule ou zéro dans le cas contraire.                                                      |
| **\_Couleur de \_ style de police TSATTRID \_**                         | Contient la valeur RVB de la couleur de texte. Contient 0xFF000000 si la couleur du texte est automatique.                               |
| **TSATTRID \_ style de police \_ \_ relief**                        | Contient une valeur différente de zéro si le texte est en relief ou zéro dans le cas contraire.                                                         |
| **\_Style de police TSATTRID \_ \_**                       | Contient une valeur différente de zéro si le texte est gravé ou zéro dans le cas contraire.                                                         |
| **\_Hauteur de \_ style de police TSATTRID \_**                        | Contient la hauteur de police. Pour plus d’informations, consultez le membre **lfHeight** de la structure LogFont.                       |
| **TSATTRID \_ style de police \_ \_ masqué**                        | Contient une valeur différente de zéro si le texte est masqué ou zéro dans le cas contraire.                                                           |
| **\_Style de police TSATTRID \_ \_ italique**                        | Contient une valeur différente de zéro si le texte est en italique ou zéro dans le cas contraire.                                                           |
| **\_Crénage de \_ style de police TSATTRID \_**                       | Contient la taille de crénage minimale. Pour plus d’informations, consultez ITextFont :: GetKerning.                                         |
| **\_Style de police TSATTRID \_ \_ minuscules**                     | Contient une valeur différente de zéro si le texte est en minuscule ou zéro dans le cas contraire.                                                        |
| **\_Style de police TSATTRID \_ \_ décrit**                      | Contient une valeur différente de zéro si le texte est entouré ou zéro dans le cas contraire.                                                         |
| **TSATTRID \_ style de police \_ \_ souligné**                      | Contient une valeur différente de zéro si le texte est en surlignage ou zéro dans le cas contraire.                                                        |
| **\_Double-ligne de style de police TSATTRID \_ \_ \_ double**              | Contient une valeur différente de zéro si le texte est double souligné ou zéro dans le cas contraire.                                                 |
| **TSATTRID \_ de \_ style de police \_ \_ simple**              | Contient une valeur différente de zéro si le texte est en surlignage simple ou zéro dans le cas contraire.                                                 |
| **\_Position du \_ style de police TSATTRID \_**                      | Contient la position de la police.                                                                                                 |
| **TSATTRID \_ style de police \_ \_ protégé**                     | Contient une valeur différente de zéro si le texte est protégé ou zéro dans le cas contraire.                                                        |
| **\_Ombre du \_ style de police TSATTRID \_**                        | Contient une valeur différente de zéro si le texte est occulté ou zéro dans le cas contraire.                                                         |
| **TSATTRID \_ style de police de la police \_ \_**                     | Contient une valeur différente de zéro si le texte est en minuscule ou zéro dans le cas contraire.                                                        |
| **\_ \_ Espacement du style de police TSATTRID \_**                       | Contient l’espacement de la police.                                                                                                  |
| **\_Style de police TSATTRID \_ \_ barré**                 | Non utilisé.                                                                                                                   |
| **\_Style de police TSATTRID \_ \_ \_ double barré**         | Contient une valeur différente de zéro si le texte est barré double ou zéro dans le cas contraire.                                             |
| **TSATTRID \_ style de police \_ \_ barré \_ simple**         | Contient une valeur différente de zéro si le texte est barré simple ou zéro dans le cas contraire.                                             |
| **TSATTRID \_ \_ indice de style de police \_**                     | Contient une valeur différente de zéro si le texte est un indice ou zéro dans le cas contraire.                                                        |
| **\_Exposant TSATTRID \_ style de police \_**                   | Contient une valeur différente de zéro si le texte est un exposant ou zéro dans le cas contraire.                                                      |
| **TSATTRID \_ style de police \_ \_ souligné**                     | Contient une valeur différente de zéro si le texte est souligné ou zéro dans le cas contraire.                                                       |
| **\_Style de police TSATTRID \_ \_ \_ double souligné**             | Contient une valeur différente de zéro si le texte est doublement souligné ou zéro dans le cas contraire.                                                |
| **TSATTRID \_ style de police \_ \_ souligné \_ simple**             | Contient une valeur différente de zéro si le texte est souligné sur une seule ligne ou zéro dans le cas contraire.                                                |
| **TSATTRID \_ style de police en \_ \_ majuscules**                     | Contient une valeur différente de zéro si le texte est en majuscule ou zéro dans le cas contraire.                                                        |
| **TSATTRID \_ \_ épaisseur du style de police \_**                        | Contient l’épaisseur de la police. Pour plus d’informations sur les valeurs possibles, consultez le membre **lfWeight** de la structure LogFont. |



 

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

 

