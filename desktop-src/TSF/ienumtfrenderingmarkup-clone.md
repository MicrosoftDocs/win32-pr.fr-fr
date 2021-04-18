---
title: IEnumTfRenderingMarkup Clone (méthode)
description: La méthode Clone IEnumTfRenderingMarkup crée une copie de l’objet énumérateur.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Cloner la méthode Text Services Framework
- Cloner la méthode Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Clone, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512110"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>IEnumTfRenderingMarkup :: Clone, méthode

La méthode **IEnumTfRenderingMarkup :: Clone** crée une copie de l’objet énumérateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* \[ à\]
</dt> <dd>

\[\]pointeur vers une interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>          |
| <dl> <dt>**E \_ échec**</dt> </dl>       | Une erreur non spécifiée s'est produite.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 

