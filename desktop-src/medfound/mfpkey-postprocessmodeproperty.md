---
description: Spécifie le mode de traitement de la publication pour le décodeur.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535401"
---
# <a name="mfpkey_postprocessmode-property"></a>MFPKEY \_ propriété POSTPROCESSMODE

Spécifie le mode de traitement de la publication pour le décodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

**\_wszWMVCForcePostProcessMode g**

## <a name="data-type"></a>Type de données

**VT \_**

## <a name="remarks"></a>Notes

Définissez cette propriété sur l’une des valeurs suivantes.



| Valeur | Signification                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | Le décodeur définit le mode de traitement de publication de manière adaptative en fonction des ressources processeur disponibles. |
| 0     | Le décodeur n’exécute aucun traitement de validation.                                               |
| 1     | le décodeur récupère effectue un déblocage rapide.                                                 |
| 2     | Le décodeur effectue un déblocage complet.                                                  |
| 3     | Le décodeur effectue un déblocage rapide et une désonne.                                    |
| 4     | Le décodeur effectue un déblocage complet et une désonne.                                    |



 

Comme la valeur de cette propriété est comprise entre 0 et 4, la complexité du décodage, l’utilisation des ressources du processeur et la qualité de l’image augmentent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




