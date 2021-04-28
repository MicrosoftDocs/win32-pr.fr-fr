---
description: IRTC ::D méthode éconnecter-la méthode Disconnect déconnecte le NPP du réseau.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: IRTC ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110717"
---
# <a name="irtcdisconnect-method"></a>IRTC ::D méthode éconnecter

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



| Code de retour                                                                                          | Description                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR**</dt> </dl>      | Le NPP capture des données. Vous ne pouvez pas vous déconnecter du réseau pendant que la capture de données est en cours.<br/> |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau.<br/>                                                                 |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>  | Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .<br/>           |



 

## <a name="remarks"></a>Notes 

Cette méthode ne peut pas être appelée lorsque le NPP capture des données. Vous devez appeler la méthode [IRTC :: Stop](irtc-stop.md) avant d’appeler IRTC ::D éconnecter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC :: Connect](irtc-connect.md)
</dt> <dt>

[IRTC :: Stop](irtc-stop.md)
</dt> </dl>

 

 




