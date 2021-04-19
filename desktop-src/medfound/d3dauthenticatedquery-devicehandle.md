---
description: Retourne un handle vers l’appareil associé à ce canal authentifié.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516806"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE

Retourne un handle vers l’appareil associé à ce canal authentifié. Vous pouvez utiliser ce handle pour vérifier si deux canaux authentifiés communiquent avec le même appareil.



| Condition requise | Valeur |
|-------------|----------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**                                                                        |
| Données d’entrée  | [**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                           |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a>Notes

Cette requête est valide pour tous les types de canaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Requêtes protection du contenu](content-protection-queries.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




