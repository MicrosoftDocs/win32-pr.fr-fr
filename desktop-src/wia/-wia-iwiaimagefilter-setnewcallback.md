---
description: Définit un nouveau rappel d’application pour le filtre de traitement d’image à utiliser pour le transfert des appels.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter :: SetNewCallback, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752829"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>IWiaImageFilter :: SetNewCallback, méthode

Définit un nouveau rappel d’application pour le filtre de traitement d’image à utiliser pour le transfert des appels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWiaTransferCallback* \[ dans\]
</dt> <dd>

Type : **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Spécifie un pointeur vers l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

N’appelez pas cette méthode directement à partir de votre application.

Le filtre de traitement d’image est requis pour libérer l’interface de rappel d’application précédemment stockée avant de définir le nouveau rappel.

Si *pWiaTransferCallback* a la **valeur null**, le filtre de traitement d’image doit simplement libérer l’ancien rappel d’application et retourner la valeur \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




