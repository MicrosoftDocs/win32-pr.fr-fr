---
description: 'IWiaUIExtension2 :: GetDeviceIcon, méthode-obtient une icône d’appareil personnalisé.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2 :: GetDeviceIcon, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116617"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>IWiaUIExtension2 :: GetDeviceIcon, méthode

Obtient une icône d’appareil personnalisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceId* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.

</dd> <dt>

*phIcon* \[ à\]
</dt> <dd>

Type : **HICON \***

Pointe vers un emplacement de mémoire qui reçoit un handle pour l’icône de l’appareil.

</dd> <dt>

*nSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie la taille d’icône souhaitée, en pixels. L’icône est supposée être carrée et nSize spécifie à la fois la largeur et la hauteur de l’icône demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **HRESULT**

Si la méthode est réussie, elle retourne la valeur \_ OK. Si la méthode échoue, elle retourne un code d’erreur approprié. Le tableau suivant présente certains des codes d’état de retour possibles.



| Code d'erreur    | Description                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Le paramètre bstrDeviceId ou phIcon a la **valeur null**, ou bstrDeviceId ne pointe pas vers une chaîne d’ID d’appareil WIA valide |
| E \_ échec       | Aucune ressource icône n’est disponible.                                                                               |
| \_NOTIMPL E    | Aucune icône de la taille demandée n’est disponible.                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




