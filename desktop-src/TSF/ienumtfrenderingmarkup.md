---
title: Interface IEnumTfRenderingMarkup
description: L’interface IEnumTfRenderingMarkup est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée par ITfContextRenderingMarkup GetRenderingMarkup et énumère les informations de balisage de rendu.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup interface Text Services Framework
- IEnumTfRenderingMarkup interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031651"
---
# <a name="ienumtfrenderingmarkup-interface"></a>Interface IEnumTfRenderingMarkup

L’interface **IEnumTfRenderingMarkup** est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée par [ITfContextRenderingMarkup :: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) et énumère les informations de balisage de rendu.



| Méthodes IEnumTfRenderingMarkup            | Description                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Répliqué](ienumtfrenderingmarkup-clone.md) | La méthode **IEnumTfRenderingMarkup :: Clone** crée une copie de l’objet énumérateur.                                                                  |
| [Next](ienumtfrenderingmarkup-next.md)   | La méthode **IEnumTfRenderingMarkup :: Next** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.          |
| [Réinitialiser](ienumtfrenderingmarkup-reset.md) | La méthode **IEnumTfRenderingMarkup :: Reset** réinitialise l’objet énumérateur en déplaçant la position actuelle jusqu’au début de la séquence d’énumération. |
| [Skip](ienumtfrenderingmarkup-skip.md)   | La méthode **IEnumTfRenderingMarkup :: Skip** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.          |



 

## <a name="members"></a>Membres

L’interface **IEnumTfRenderingMarkup** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="remarks"></a>Notes

> [!Note]  
> Cette interface n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

 