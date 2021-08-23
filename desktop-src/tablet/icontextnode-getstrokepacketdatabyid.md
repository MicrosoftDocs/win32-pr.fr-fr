---
description: Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'IContextNode :: GetStrokePacketDataById, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f80ad2e4acc88f24a14e21f604eb17dbab51a5bdeca0fc90ffc3ca9beb99f1de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967377"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>IContextNode :: GetStrokePacketDataById, méthode

Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strokeId* \[ dans\]
</dt> <dd>

Identificateur du trait.

</dd> <dt>

*pStrokePacketDataCount* \[ in, out\]
</dt> <dd>

Longueur du tableau de données du paquet.

</dd> <dt>

*pplStrokePacketData* \[ à\]
</dt> <dd>

Pointeur vers les données du paquet pour le trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pplStrokePacketData* lorsque vous n’avez plus besoin des informations.

 

*plStrokePacketData* contient des données de paquet pour tous les points du trait. Pour obtenir les types de données de paquet inclus pour chaque point du trait, utilisez [**IContextNode :: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

