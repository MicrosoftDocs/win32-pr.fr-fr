---
description: Déplace un MDIForm, un formulaire ou un contrôle.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'IExtender :: Move, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002099"
---
# <a name="iextendermove-method"></a>IExtender :: Move, méthode

Déplace un MDIForm, un formulaire ou un contrôle.

## <a name="syntax"></a>Syntaxe


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

à *gauche* \[ dans\]
</dt> <dd>

Bord gauche du formulaire ou du contrôle.

</dd> <dt>

en *haut* \[ dans\]
</dt> <dd>

Bord supérieur du formulaire ou du contrôle.

</dd> <dt>

*largeur* \[ dans\]
</dt> <dd>

Largeur du formulaire ou du contrôle.

</dd> <dt>

*hauteur* \[ dans\]
</dt> <dd>

Hauteur du formulaire ou du contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll ; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




