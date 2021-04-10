---
title: IEnumTfRenderingMarkup Skip (méthode)
description: La méthode IEnumTfRenderingMarkup Skip obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignorer la méthode Text Services Framework
- Ignorer la méthode Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Skip, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678314"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>IEnumTfRenderingMarkup :: Skip, méthode

La méthode **IEnumTfRenderingMarkup :: Skip** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulCount* \[ dans\]
</dt> <dd>

\[dans \] spécifie le nombre d’éléments à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                   | Description                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | La méthode a réussi.<br/>                                                                              |
| <dl> <dt>**S \_ false**</dt> </dl> | La méthode a atteint la fin de l’énumération avant que le nombre spécifié d’éléments puisse être ignoré.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

 





