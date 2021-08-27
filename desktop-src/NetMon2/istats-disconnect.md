---
description: Déconnecte le NPP du réseau.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: eabba7b5cf234d48b2839074ec1ad07380a7ed14858f6bd43b07f7d2eaa033b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037189"
---
# <a name="istatsdisconnect-method"></a>IStats ::D méthode éconnecter

La **méthode Disconnect** déconnecte le NPP du réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR**</dt> </dl>        | Le NPP capture actuellement des données. Vous ne pouvez pas vous déconnecter du réseau pendant qu’une capture de données est en cours.<br/> |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau.<br/>                                                                         |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [**IStats :: Connecter**](istats-connect.md) .<br/>          |



 

## <a name="remarks"></a>Remarques

Cette méthode ne peut pas être appelée lorsque le NPP capture des données. Appelez d’abord la méthode **IStats ::D éconnecter** , puis appelez [**IStats :: Stop**](istats-stop.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats :: Connecter**](istats-connect.md)
</dt> <dt>

[**IStats :: Stop**](istats-stop.md)
</dt> </dl>

 

 




