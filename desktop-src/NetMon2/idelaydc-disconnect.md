---
description: IDelaydC ::D méthode éconnecter-la méthode Disconnect déconnecte le NPP du réseau.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110807"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC ::D méthode éconnecter

La **méthode Disconnect** déconnecte le NPP du réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                          | Description                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR**</dt> </dl>      | Le NPP capture des données. Vous ne pouvez pas déconnecter le NPP du réseau lors d’une capture.<br/>            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau.<br/>                                                               |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>   | Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode ne peut pas être appelée lorsque le NPP capture des données. Vous devez appeler la méthode **IDelaydC :: Stop** avant d’appeler **Disconnect**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC :: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC :: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




