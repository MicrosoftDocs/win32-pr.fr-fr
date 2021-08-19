---
description: La \_ méthode obtenir AlphaRamp récupère la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'IDxtAlphaSetter :: get_AlphaRamp, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9768ed96f0b40e074fd44de04ca44a8cc17d9de7ce4b75af948975e26b5e3077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952738"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>IDxtAlphaSetter :: \_ AlphaRamp, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_AlphaRamp` méthode récupère la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Reçoit la rampe alpha. Une valeur négative indique qu’aucune rampe alpha n’est définie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                               | Description                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null**<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Succès<br/>                   |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




