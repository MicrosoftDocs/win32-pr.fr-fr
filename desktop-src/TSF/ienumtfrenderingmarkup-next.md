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
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031489"
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



 

## <a name="remarks"></a>Notes

> [!Note]  
> Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

