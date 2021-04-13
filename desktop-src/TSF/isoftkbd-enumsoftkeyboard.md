---
title: Méthode ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd EnumSoftKeyboard énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Infrastructure des services de texte de méthode EnumSoftKeyboard
- EnumSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466163"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>ISoftKbd :: EnumSoftKeyboard, méthode

La méthode **ISoftKbd :: EnumSoftKeyboard** énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LangID* \[ dans\]
</dt> <dd>

Identificateur de langue.

</dd> <dt>

*lpdwKeyboard* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère les identificateurs des claviers logiciels disponibles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *LangID* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





