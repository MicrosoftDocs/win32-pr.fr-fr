---
title: IEnumTfRenderingMarkup méthode Next
description: La méthode Next IEnumTfRenderingMarkup obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Infrastructure des services de texte méthode suivante
- Méthode Next Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Next, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: deee2a2a65889739fd583e8752e37c3bdfeb66fb865494532374174b615335b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953205"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>IEnumTfRenderingMarkup :: Next, méthode

La méthode **IEnumTfRenderingMarkup :: Next** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulCount* \[ à\]
</dt> <dd>

\[out \] spécifie le nombre d’éléments à obtenir.

</dd> <dt>

*ppElement* \[ à\]
</dt> <dd>

\[pointeur de sortie \] vers un tableau de structures [ \_ RENDERINGMARKUP TF](/windows/desktop/TSF/tf-renderingmarkup) . Ce tableau doit avoir au moins *ulCount* éléments de taille.

</dd> <dt>

*pcFetched* \[ à\]
</dt> <dd>

\[\]pointeur vers une valeur ulong qui reçoit le nombre d’éléments réellement obtenus. Cette valeur peut être inférieure au nombre d’éléments demandés. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>                                                                               |
| <dl> <dt>**S \_ false**</dt> </dl>      | La méthode a atteint la fin de l’énumération avant que le nombre spécifié d’éléments puisse être obtenu.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/>                                                                      |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

