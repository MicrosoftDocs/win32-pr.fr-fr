---
description: Remplit un tableau de pointeurs vers des interfaces IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2 :: Next, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201673"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2 :: Next, méthode

Remplit un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cElt* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie le nombre d’éléments de tableau dans le tableau indiqué par le paramètre *ppIWiaItem2* .

</dd> <dt>

*ppIWiaItem2* \[ à\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un tableau de pointeurs d’interface [**IWiaItem2**](-wia-iwiaitem2.md) . **IEnumWiaItem2 :: Next** remplit ce tableau avec des pointeurs d’interface.

</dd> <dt>

*pcEltFetched* \[ in, out\]
</dt> <dd>

Type : **ULong \** _

Lors de la sortie, ce paramètre reçoit le nombre de pointeurs d’interface réellement stockés dans le tableau indiqué par le paramètre _ppIWiaItem2 *. Lorsque l’énumération est terminée, ce paramètre contient la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le système d’exécution Windows Image Acquisition (WIA) 2,0 représente les périphériques matériels WIA 2,0 sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) . Les applications utilisent la méthode **IEnumWiaItem2 :: Next** pour obtenir un pointeur d’interface **IWiaItem2** pour chaque élément dans le dossier actif de l’arborescence d’objets **IWiaItem2** d’un périphérique matériel.

Pour obtenir la liste des pointeurs, l’application passe un tableau de pointeurs d’interface [**IWiaItem2**](-wia-iwiaitem2.md) qu’il alloue. Il passe également le nombre d’éléments de tableau dans le paramètre *cElt*. La méthode **IEnumWiaItem2 :: Next** remplit le tableau avec des pointeurs vers des interfaces **IWiaItem2** .

Tant que le processus d’énumération n’est pas terminé, la méthode **IEnumWiaItem2 :: Next** retourne S \_ OK. À chaque fois, il définit la valeur désignée par *pcEltFetched* sur le nombre d’éléments qu’il a insérés dans le tableau. Si **IEnumWiaItem2 :: Next** termine le processus d’énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) , il retourne S \_ false et définit l’emplacement de la mémoire désigné par *pcEltFetched* à zéro.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
