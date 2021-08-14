---
description: Retourne une chaîne qui décrit le code d’État.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler :: GetStatusDescription, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208301"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>IWiaErrorHandler :: GetStatusDescription, méthode

Retourne une chaîne qui décrit le code d’État.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punkItem* \[ dans\]
</dt> <dd>

Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Pointeur vers le [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’élément en cours de transfert. Cet objet implémente au minimum [**IWiaItem2**](-wia-iwiaitem2.md) et [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ dans\]
</dt> <dd>

Type : **HRESULT**

**HRESULT** qui correspond au code d’état reçu par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ dans\]
</dt> <dd>

Type : **long**

**Valeur de type long** qui correspond à la taille des données référencées par *pbData*.

</dd> <dt>

*pbData* \[ dans\]
</dt> <dd>

Type : **Byte \***

Pointeur vers la mémoire tampon de données telle qu’elle a été reçue par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*pbstrDescription* \[ à\]
</dt> <dd>

Type : **BSTR \***

**BSTR** qui reçoit une description de l’État ou de l’erreur rencontrée pendant le transfert de données. Ce paramètre ne peut pas être **null**. L’appelant doit libérer la chaîne à l’aide de [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), et l’implémenteur doit allouer la chaîne à l’aide de [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne l’une des valeurs suivantes.



| Code de retour                                                                             | Description                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | *pbstrDescription* contient un pointeur **BSTR** valide. <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *hrStatus* est inconnu et aucune description n’est disponible. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
