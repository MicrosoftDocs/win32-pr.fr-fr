---
description: Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'IContextNode :: GetStrokePacketDescriptionById, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517283"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>IContextNode :: GetStrokePacketDescriptionById, méthode

Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait.

</dd> <dt>

*pulStrokePacketDescriptionCount* \[ in, out\]
</dt> <dd>

Nombre de propriétés de paquet dans chaque paquet.

</dd> <dt>

*ppStrokePacketDescriptionGuids* \[ à\]
</dt> <dd>

Tableau contenant les identificateurs de propriété de paquet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppStrokePacketDescriptionGuids* lorsque vous n’avez plus besoin des informations.

 

\**ppStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point du trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

